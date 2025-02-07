
## 1 Operation Process

!!! Abstract ""
    MaxKB's operation process can generally be divided into four steps: adding models, creating knowledge bases, creating applications, and publishing applications.     
    In advanced orchestration applications, you can also create functions for data processing, logical judgment, information extraction, or other work scenario functions through the function library, providing more powerful and flexible capabilities.

![Tongyi Qianwen APIkey](img/model/maxkb_flow.png)

!!! Abstract ""
    Below we'll quickly create and publish an intelligent Q&A application using the Tongyi Qianwen large language model with a general knowledge base as an example.

## 2 Add Model

!!! Abstract ""
    After logging into the MaxKB system, select `Tongyi Qianwen` from the provider list, then click [Add Model] to enter the model configuration form with the following parameters:

    * Model Name: Custom model name in MaxKB.  
    * Permission: Two types - private and public. Private models are only available to the current user, while public models are available to all users in the system, but other users cannot edit.   
    * Model Type: LLM.   
    * Base Model: LLM model name supported by Tongyi Qianwen. The dropdown options are some commonly used large language model names, and custom input is supported.        
    * API Key: Created and viewed in Alibaba Cloud DashScope API Key Management.

![Tongyi Qianwen APIkey](img/model/tongyi_model.png)

## 3 Create Knowledge Base

!!! Abstract ""

    Open the [Knowledge] page, click [Create Knowledge ], enter the knowledge base name, description, select the general knowledge base type, then upload offline documents by dragging and dropping or selecting files.

### 3.1 Upload Documents

!!! Abstract ""
    Document upload requirements:  

    * File formats: Markdown, TXT, PDF, DOCX, HTML
    * Table formats: Excel, CSV
    * QA pairs: Excel, CSV  
    * Maximum 50 files per upload   
    * Each file not exceeding 100 MB
    * Support selecting folders to upload files meeting format requirements

    Document specification recommendations:

    * Standardized segment markers: Offline documents should have standardized segment markers, otherwise the split paragraphs will be irregular.   
    * Complete paragraphs: A segment should ideally describe a complete feature or issue.

![Create General Knowledge Base](img/dataset/create_offline_dataset.png)

### 3.2 Set Segmentation Rules
    
!!! Abstract ""
    Currently, MaxKB supports two segmentation methods: intelligent segmentation and advanced segmentation.

    **Intelligent Segmentation**

    (1) Intelligent segmentation rules for MarkDown files:<br />

    * Segments by drilling down through title levels, supporting up to 6 levels of titles, with maximum 4096 characters per segment.   
    * When the text paragraph at the last level exceeds the set segment length, it will look for line breaks within the segment length for cutting.

    (2) Intelligent segmentation rules for HTML and DOCX files:

    * Recognizes title formats and converts them to markdown styles.
    * Drills down through levels for segmentation, supporting up to 6 title levels, with maximum 4096 characters per segment.

    (3) Intelligent segmentation rules for TXT and PDF files:

    * Segments by # titles; if no # titles exist, segments by 4096 characters.
    * Looks for line breaks within segment length for cutting.  
      
![Intelligent Segmentation](<img/dataset/automatic_paragraphing.png>)

!!! Abstract ""
    **Advanced Segmentation**  

    Users can customize segment markers, segment length, and automatic cleaning according to document specifications.

    * Supported segment markers: #, ##, ###, ####, #####, ######, -, blank line, line break, space, semicolon, comma, period, and manual input of segment markers   
    * Segment length: Supports minimum 50 characters, maximum 4096 characters   
    * Automatic cleaning: When enabled, the system automatically removes redundant symbols like spaces, blank lines, tabs, etc.     

![Advanced Segmentation](<img/dataset/advanced_segmentation.png>)
!!! Abstract ""
    **Add "Related Questions" section for question-based pairs during import**  

    When checked, all segment titles will be set as related questions for the segments.
![Set Title as Related Question](img/dataset/titel_set_question.png)

!!! Abstract ""
    **Preview** 

    After setting segmentation rules, click [Generate Preview] to check the segmentation effect of the latest rules.

![Segmentation Preview](<img/dataset/preview_segmentation.png>)

!!! Abstract ""
    You can edit unreasonable segments in the segmentation preview.

![Edit Segments](img/dataset/view_edit.png)

 
!!! Abstract ""
    After clicking [Start Import], the system backend will automatically perform segmentation -> storage -> vectorization operations on the documents. When completed, each file's status in the knowledge base document list will show as `Success`.

![Document List](img/dataset/doc_list.png)

## 4 Create Application

!!! Abstract ""
    Click [Create APP], enter the application name and description, select [Simple Configuration Application], click [Create]

![Select Application Type](img/app/selectAppType.png)

!!! Abstract ""
    After the application is created, enter the simple configuration application settings page, with application information on the left and debug preview interface on the right.

    * Application Name: Title and name of the chat box when users ask questions    
    * Application Description: Description of application scenarios and uses    
    * AI Model: Large language model added in [System Settings]-[Model Management]    
    * Prompt: System has default prompts for intelligent knowledge base, users can customize by adjusting prompt content to guide the large model chat direction. Different prompts can be set for cases with and without knowledge base references
    * Chat History: Submit the last N conversations in the current session to the large model, otherwise only submit the current question
    * Associated Knowledge Base: After user questions, segments will be retrieved from associated knowledge bases   
    * Opening Message: Greeting message when users open the dialogue. Supports Markdown format; content after [-] are quick questions, one per line 
    * Voice Input: When enabled, supports voice questions, requires speech recognition model support
    * Voice Playback: When enabled, answers can be played through voice, either through browser playback or by selecting a voice synthesis model

    After setting application information, you can preview questions in the debug preview on the right. Questions in debug preview are not counted in conversation logs.
![Application Settings](img/app/app_setting.png)


  
!!! Abstract "" 
    ** Knowledge Base Parameter Settings**

    (1) **Retrieval Mode**

    * Vector Retrieval: Uses vector model to calculate text segments most similar to user questions through vector distance        
    * Full-text Retrieval: Retrieves text segments containing the most keywords through keyword search           
    * Hybrid Retrieval: Executes both full-text and vector retrieval, then reranks to select best results matching user questions from both query types    

    (2) **Similarity:** Higher similarity indicates stronger relevance between questions and segments 

    (3) **Reference Segment Count:** Carries N segments by similarity to generate prompts when asking LLM model 

    (4) **Maximum Reference Characters:** Sets maximum character count for referenced segment content, truncates if exceeded     

    (5) **When there are no knowledge references**

    * Continue Asking: Can customize prompt settings, needs `{question}` placeholder for user questions to send to model       
    * Specify Reply Content: Can specify reply content when no knowledge base segments are matched   
    
    (6) **Question Optimization:** When enabled, user questions first undergo LLM optimization processing, then optimized questions are vector-searched in knowledge base, improving retrieval accuracy but increasing response time due to additional model query

![Knowledge Base Parameter Settings](<img/app/app-parameter-setting.png>)

!!! Abstract "" 
    After debugging, save settings and publish. On the application list page, click demo buttonin the overview page or copy the Public Access Linker in browser to interact.
![Preview](img/app/app_view.png)

## 5 Application Integration

!!! Abstract "" 
    MaxKB applications support quick  embedding into third-party Web systems with zero-code.

    On the application overview page, click [Embed Third-party] to copy fullscreen mode code or floating window mode code for embedding into third-party systems. After embedding, Q&A can be conducted in third-party systems.

![Embed Third-party](<img/app/embed.png>)

!!! Abstract "" 
    In the Professional Edition, you can also integrate with WeChat Work, WeChat Official Accounts, DingTalk, and Feishu applications. For detailed instructions, see: [X-Pack Features-Application Integration](./user_manual/X-Pack/app_integrate.md).

