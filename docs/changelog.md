## 1 Version Information

!!! Abstract ""
    **Version Notes:** Like other excellent open-source projects, MaxKB will maintain a monthly release of new feature versions. If urgent or serious bugs are encountered in a feature version, a bug fix minor version will be released promptly.
    **MaxKB version naming rule:** v Major.Feature.Bug Fix, examples as follows:

    - v1.0.1 is a bug fix version after v1.0.0
    - v1.1.0 is a feature version after v1.0.0

## 2 Update Content

### v1.9.1

January 9, 2025

!!! Abstract "Feature Optimization :sunflower:"
    - Knowledge Base: Support vectorizing only non-successful segments during document vectorization.
    - Application: Conversation logs through third-party applications are optimized to record each user's conversation logs daily. (X-Pack)

!!! Abstract "Bug Fixes :palm_tree:"
    - Application: Fixed the issue of image loading failure in prompts during voice input.
    - Application: Fixed the issue where setting variable parameters in embedded application nodes would not take effect after saving.
    - Application: Fixed the "Connection aborted" prompt issue after ending a conversation using the image understanding model in certain network environments.
    - Application: Fixed the issue where the execution condition of the judgment node doesn't take effect when set to "any".
    - Application: Fixed the issue where custom input of base models is not possible when adding image understanding and generation models.
    - Application: Fixed the issue where execution nodes would be missing in execution details under certain circumstances.

### v1.9.0

January 2, 2025

!!! Abstract "New Features :star2:"
    - Application: Added image generation node.
    - Application: Support for uploading audio files, added speech-to-text node.
    - Application: Added text-to-speech node.
    - Application: Support for exporting and importing applications.
    - Application: Workflow nodes support setting execution conditions.
    - Application: Support for integrating with WeChat Work customer service. (X-Pack)
    - Application: Official accounts, WeChat Work, and WeChat customer service support voice questions and answers. (X-Pack)
    - Knowledge Base: Knowledge bases and documents support exporting ZIP packages with Excel files and offline images.
    - Knowledge Base: When uploading documents and selecting text file type, added XLS, XLSX, CSV, and ZIP file formats.
    - Knowledge Base: When uploading documents and selecting QA pairs type, added ZIP file format.
    - Model Settings: When creating models, support for setting model parameters.
    - Model Settings: Image understanding and image generation models support setting model parameters.
    - Model Settings: Image understanding models added support for Xinference, Ollama, Doubao, Alibaba Cloud Bailian, Azure OpenAI, and Gemini providers.
    - Model Settings: Image generation models added support for Xinference, OpenAI, Tencent Hunyuan, Tongyi Qianwen, Zhipu AI, Doubao, Alibaba Cloud Bailian, and Azure OpenAI providers.
    - Model Settings: Vector models added support for Azure OpenAI provider.
    - Model Settings: Speech recognition models added support for Azure OpenAI provider.
    - Model Settings: Speech synthesis models added support for Azure OpenAI provider.

!!! Abstract "Feature Optimization :sunflower:"
    - Application: In the basic information node, the "user input" parameter supports setting the "show default value" option when adding parameters.
    - Application: Parameters in the form collection node support setting the "show default value" option.
    - Application: Conversation URL supports carrying the "question=query" parameter to automatically send the question when opening the conversation page.
    - Application: Automatically generating "Please analyze the image content" question when uploading an image.
    - Application: Optimized the execution efficiency of workflow nodes.
    - Knowledge Base: Document list supports batch cancellation of vectorization and batch cancellation of question generation.
    - Model Settings: When adding large language models for Amazon Bedrock provider, supports ProxyURL parameter.

!!! Abstract "Bug Fixes :palm_tree:"
    - Security: Fixed remote command execution security vulnerability in the function library module (CVE-2024-56137).
    - Application: Fixed the issue where the "New Conversation" button is not displayed in the floating dialog box.
    - Application: Fixed the issue of inconsistent icon colors in the upper right corner of the floating dialog box.
    - Application: Fixed the issue where historical applications would prompt "missing context type" error during conversations.
    - Application: Fixed the error when using older browser versions for conversations.
    - Application: Fixed the issue where nodes would be missed when executing complex workflows under certain circumstances.

### v1.8.1

December 12, 2024

!!! Abstract "New Features :star2:"
    - Application: Historical chat records in AI conversation nodes can be set as context for workflows and nodes.
    - Model Management: Support for Zhipu AI provider's image understanding model.

!!! Abstract "Feature Optimization :sunflower:"
    - Application: Filter form data during voice playback.
    - System: Optimized display styles of certain pages.

!!! Abstract "Bug Fixes :palm_tree:"
    - Application: Fixed the issue where data doesn't load after filtering results by name.
    - Application: Fixed the issue where floating icon would be covered by the guide image when too large.
    - Knowledge Base: Fixed the error in document filtering results by status.
    - Knowledge Base: Fixed the issue where members with view permissions could export documents.
    - Knowledge Base: Fixed the issue where members with view permissions could modify segment enable/disable status.
    - Knowledge Base: Fixed the issue where only the first page content could be identified when uploading PDF files without directory structure.
    - System Management: Fixed the missing parameter issue in the Web site knowledge base in Swagger documentation. (X-Pack)
    - System Management: Fixed the WeChat Work scan code login configuration error. (X-Pack)

### v1.8.0

December 5, 2024

!!! Abstract "New Features :star2:"
    - Application: Support for uploading documents and images when users ask questions.
    - Application: Added document content extraction node to workflow.
    - Application: Added image understanding node to workflow.
    - Application: Added form collection node to workflow.
    - Application: Support for embedded application nodes in workflow.
    - Application: Workflow canvas supports collapsing or expanding all nodes and one-click layout beautification.
    - Application: In basic node's user input parameters, support for checkbox and tab components.
    - Application: Welcome message supports HTML rendering.
    - Application: Support for batch adding conversation logs to knowledge base.
    - Application: Support for displaying applications by creator.
    - Knowledge Base: Support for displaying knowledge bases by creator.
    - Function Library: Support for displaying functions by creator.
    - Model Settings: Support for Tongyi Qianwen provider's image understanding model.
    - Model Settings: Support for OpenAI provider's image understanding model.
    - Model Settings: Support for Tencent Hunyuan provider's image understanding model.
    - Model Settings: Support for Alibaba Cloud Bailian provider's large language model.
    - System Management: Support for OAuth2 single sign-on method. (X-Pack)

!!! Abstract "Feature Optimization :sunflower:"
    - Knowledge Base: Optimized document status to display detailed progress of vectorization and question generation.
    - Application: In basic node's user input parameters, radio button component supports setting labels and option values.
    - Application: When annotating AI reply content on the conversation details page, retain the previously selected knowledge base document.
    - Application: Optimized the display order of conversation logs list, sorted by latest conversation time in descending order.
    - Application: Optimized opening conversation details to display the latest conversation record by default.

!!! Abstract "Bug Fixes :palm_tree:"
    - Knowledge Base: Fixed the error when uploading documents containing unrecognizable special characters in PDF documents.
    - Knowledge Base: Fixed the issue where tasks couldn't be dispatched when generating questions for documents in "Success" status under certain circumstances.
    - Knowledge Base: Fixed the issue where text content couldn't be obtained from website knowledge bases due to website encoding problems.
    - System Management: Fixed the issue where members with knowledge base management permissions couldn't view knowledge bases.
    - System Management: Fixed the issue where members with application view permissions could modify application access configuration. (X-Pack)

### v1.7.2

November 15, 2024

!!! Abstract "Bug Fixes :palm_tree:"
    - Application: Fixed the issue where custom uploaded user avatars and AI reply avatars were distorted in display settings.
    - Application: Fixed the issue where applications couldn't be published after collapsing the knowledge base retrieval node in the workflow.
    - Application: Fixed the issue where applications couldn't be published if temperature or maximum output tokens parameters were deleted in AI model parameter settings.
    - Application: Fixed the issue where tooltips occasionally wouldn't display when knowledge base names associated with applications were too long.
    - Application: Fixed the issue where query results were displayed incorrectly in the application list.

### v1.7.1

November 8, 2024

!!! Abstract "Feature Optimization :sunflower:"
    - Application: Save the collapse/expand state of nodes in advanced orchestration applications.

!!! Abstract "Bug Fixes :palm_tree:"
    - Application: Fixed the issue where authenticated official accounts wouldn't reply to questions.
    - Application: Fixed style issues on the official account configuration page for application access.
    - Application: Fixed the error that occurs during execution when non-required parameters are set in functions and those functions are referenced in applications without passing values.
    - Application: Fixed the issue where execution details couldn't be viewed when no return content was enabled for all nodes in the workflow.
    - Application: Fixed display issues with direct answer segment content.
    - Application: Fixed the issue where the latest published application configuration wasn't used when asking questions after application publication.
    - Knowledge Base: Fixed the issue where images couldn't be recognized when importing DOCX documents under certain circumstances.
    - Q&A Page: Fixed the issue where image content in returned Markdown tables would cause display misalignment in AI answers.
    - System Settings: Fixed the issue where clicking "Select All" after searching in team member permission settings would select all items instead of just the search results.
    - Model Management: Fixed the issue where adding Xinference vector models would prompt "API domain name invalid".

### v1.7.0

October 31, 2024

!!! Abstract "New Features :star2:"
    - [Knowledge Base] Support for auto-generating related questions for knowledge base documents.
    - [Application] Workflow nodes support multiple inputs and outputs.
    - [Application] Support for setting voice playback sound and speed.
    - [Application] Support for viewing and restoring historical versions.
    - [Application] Support for setting conversation log clearing policy.
    - [Application] Advanced orchestration applications support auto-save settings, disabled by default, saves every 5 minutes when enabled.
    - [Application] The workflow orchestration interface supports component name search when adding components.
    - [Model Settings] Support for customizing parameters for large language models and speech synthesis models.
    - [Model Settings] Support for querying models by model type, creator, and permissions.
    - [Model Settings] Added creator information in the model panel.
    - [Model Settings] Support for Alibaba Cloud Bailian vector models.
    - [Model Settings] Support for Amazon Bedrock vector models.
    - [Model Settings] Support for Tencent Hunyuan vector models.
    - [Model Settings] Support for Xunfei Sparkdesk vector models.
    - [Model Settings] Support for Baidu Qianfan vector models.
    - [Model Settings] Support for Alibaba Cloud Bailian speech recognition and speech synthesis models.
    - [Model Settings] Support for Xinference speech recognition and speech synthesis models.
    - [Q&A Page] Support for personalized display settings. (X-Pack)
    - [Q&A Page] Support for identity verification. (X-Pack)
    - [System Settings] Support for WeChat Work, DingTalk, and Feishu scan code login. (X-Pack)

!!! Abstract "Feature Optimization :sunflower:"
    - [Application] Basic node's global variables optimized into two parameter forms: user input and interface parameters.
    - [Application] Support for knowledge base name search when associating knowledge bases.
    - [Application] Hover display for overly long knowledge base association names.
    - [Application] Knowledge base retrieval results and direct answer segment content include segment titles.
    - [Application] Exporting advanced orchestration applications includes referenced segment data from knowledge base retrieval nodes.
    - [Application] No more debug information output in console during voice input.
    - [Function Library] Optimized Python editor component in functions for a more friendly function writing experience.
    - [Team Management] Added select all button when setting resource permissions.
    - [Model Settings] Support for filtering providers by model type when creating models.
    - [Model Settings] Optimized the display order and categorization of provider lists, dividing providers into public model providers and private model providers.
    - [System Settings] Optimized password modification logic to verify password consistency first, then send email verification code.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Fixed the issue where a license expiration notice would appear once after importing a License file.
    - [Knowledge Base] Fixed the error when opening an exported file after exporting an empty knowledge base.
    - [Knowledge Base] Fixed the abnormal display of AI reply content when images in knowledge base documents don't exist.
    - [Knowledge Base] Fixed the issue where images weren't properly imported after uploading DOCX files to the knowledge base in certain cases.
    - [Knowledge Base] Fixed the issue where segment length settings didn't take effect when uploading PDF files to the knowledge base with advanced segmentation.
    - [Knowledge Base] Fixed the issue where inserting MarkDown flowcharts in knowledge base segments wouldn't display text content.
    - [Application] Fixed the issue where questions in WeChat Work wouldn't receive replies when the application used Doubao intelligent agent models.
    - [Application] Fixed the UI disorder issue when referenced segment file names in knowledge sources were too long.
    - [Application] Fixed the issue where images couldn't be returned when text content appeared after images in replies to questions in the connected official account.
    - [Model Management] Fixed the issue where models couldn't be added when model name and ID were inconsistent when adding Xinference models.
    - [Model Management] Fixed the issue where no authentication parameters were passed causing "API domain name invalid" prompts when adding Xinference models.

### v1.6.1

September 29, 2024

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application] Fixed the error when conversing using AWS models.
    - [Application] Fixed the blank display issue when entering the advanced orchestration application edit page for the first time after upgrading.
    - [Application] Fixed the issue where the debug dialog would close after selecting variables in the global variable settings of advanced orchestration applications.
    - [Application] Fixed the incomplete display of knowledge base names that are too long in knowledge base associations.
    - [Knowledge Base] Fixed the error when exporting when segment content exceeds the maximum length of a cell.

### v1.6.0

September 27, 2024

!!! Abstract "New Features :star2:"
    - [Application] Support for voice Q&A.
    - [Application] Support for multi-path retrieval using reranking models.
    - [Application] Support for custom global variables.
    - [Application] Support for standard OpenAI format conversations.
    - [Application] Support for rendering ECharts charts and HTML pages.
    - [Knowledge Base] Support for uploading Excel and CSV table documents.
    - [Knowledge Base] Support for batch re-vectorization of multiple documents.
    - [Knowledge Base] Support for batch association of questions with segments.
    - [Function Library] Support for custom function permission and status settings.
    - [Model Management] Support for speech recognition and speech synthesis models from Doubao, Xunfei Sparkdesk, and OpenAI providers.
    - [Model Management] Support for reranking models from Alibaba Cloud Bailian, Xinference, and local models.
    - [Application] One-click integration with WeChat Work, DingTalk, Feishu, and WeChat Official Accounts. (X-Pack)
    - [Appearance Settings] Support for customizing theme colors, project information, and other settings. (X-Pack)

!!! Abstract "Feature Optimization :sunflower:"
    - [Knowledge Base] PDF documents support segmentation by directory chapters.
    - [Application] The maximum value for tokens output in AI model parameter settings adjusted to 100,000, with size controlled by users.
    - [Application] Optimized simple application settings, with prompts divided into prompts without referenced knowledge base and prompts with referenced knowledge base.
    - [Application] Simple application questions optimized to knowledge base association parameter settings, with support for setting prompts.
    - [Application] Simple application multi-turn conversation adjusted to chat history, with customizable history record count.
    - [Application] Simple application debug preview's application logo can be customized with uploaded application avatars.
    - [Application] Advanced orchestration application nodes support expansion and collapse to save canvas space.
    - [Application] Clicking the "+" icon on the right side of nodes in advanced orchestration applications directly adds nodes.
    - [Application] Added system variables for chat history and conversation ID.
    - [Application] Support for Markdown style editing when modifying annotation content in conversation log details.
    - [Q&A Page] Optimized the icon for the "try another answer" button.
    - [User Management] Optimized username rules for creating users.
    - [System] Optimized dialog boxes to only exit via "Save" or "Close" options, preventing accidental exits during editing.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Fixed the issue where content is blank when uploading Word documents exported from Yuque to MaxKB.
    - [Knowledge Base] Fixed the error when uploading blank PDF files.
    - [Application] Fixed the issue where historical conversation records aren't carried when questions take more than 30 seconds with multi-turn conversation enabled.
    - [Application] Fixed the error in description of maximum output tokens in AI model parameter settings.
    - [Application] Fixed the error when conversing through an application's API Key with stream set to false.
    - [Application] Fixed the error in conversations when setting role configurations for called Tencent Hunyuan models in AI conversation nodes.
    - [Team Members] Fixed the issue where team members exceed boundaries when there are too many team members.

### v1.5.1

August 29, 2024

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application] Fixed the issue of temperature parameter not set prompt when clicking publish in application settings.
    - [Application] Fixed the error in obtaining tokens when asking questions using local models.

### v1.5.0

August 28, 2024

!!! Abstract "New Features :star2:"
    - [Function Library] Support for function features.
    - [Advanced Application] Workflow orchestration supports adding function nodes from the function library.
    - [Application] Support for copying applications.
    - [Application] Support for setting temperature and max_tokens parameters for AI models.
    - [Model Management] Support for integrating with Doubao large models.
    - [Model Management] Support for integrating with Amazon Bedrock large models.
    - [Model Management] Support for integrating with Tencent Hunyuan large models.
    - [Model Management] Support for integrating with vLLM large models.
    - [Model Management] Support for integrating with Xinference large models.
    - [System Settings] Support for CAS authentication method. (X-Pack)
    - [System Settings] Support for OIDC authentication method. (X-Pack)

!!! Abstract "Feature Optimization :sunflower:"
    - [Knowledge Base] Optimized document vectorization performance.
    - [Knowledge Base] Optimized intelligent segmentation effect for PDF documents.
    - [Application] Optimized filtering out leading and trailing spaces in application names.

!!! Abstract "Bug Fixes :palm_tree:"
    - [System] Fixed Django JSONField SQL injection vulnerability (CVE-2024-42005).
    - [Knowledge Base] Fixed the issue where setting direct answer similarity to 0.000 prompts successful setup but doesn't actually take effect.
    - [Knowledge Base] Fixed the error when a single segment exceeds 100,000 characters during intelligent segmentation.
    - [Application] Fixed the error when exporting conversation logs.
    - [Application] Fixed the issue where prompts in AI conversation nodes cannot be selected on the orchestration page.
    - [Application] Fixed the conflict between mouse zoom events and positioning in prompt fields in AI conversation nodes on the orchestration page.
    - [Model Management] Fixed inconsistency in model name validation between frontend and backend.
    - [Model Management] Fixed the issue where Zhipu AI models couldn't be added.
    - [Appearance Settings] Fixed the error when uploading large-sized images for login image settings. (X-Pack)
    - [Appearance Settings] Fixed the issue where default appearance is still displayed after customizing appearance settings. (X-Pack)

### v1.4.1

August 8, 2024

!!! Abstract "New Features :star2:"
    - [Application] Custom conversation avatars and floating entry icons in display settings support GIF format. (X-Pack)
    - [Application Orchestration] Specified reply and AI conversation nodes added return content settings.

!!! Abstract "Feature Optimization :sunflower:"
    - [Application Orchestration] Optimized welcome message and prompt editing boxes to support enlargement.
    - [Q&A Page] User questions display line breaks after asking.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application] Fixed the issue where answer content would be jumbled when multiple users asked questions simultaneously using the Xunfei Sparkdesk model.
    - [Application] Fixed the issue where multi-turn conversation settings don't take effect when asking questions on the settings page.
    - [Application] Fixed the continuous permission prompt issue on the advanced orchestration page when an application only has usage permissions.
    - [Knowledge Base] Fixed the error when modifying related questions.
    - [Knowledge Base] Fixed the error when uploading ultra-high-pixel graphics when adding segments.
    - [Knowledge Base] Fixed the issue of partial content loss after uploading PDF Q&A.
    - [Knowledge Base] Fixed the issue where vector model selection doesn't take effect when creating Web site knowledge bases.
    - [Knowledge Base] Fixed the issue of data retrieval failure when uploading QA pair files with only numbers in the table.
    - [Knowledge Base] Fixed the issue of documents still being vectorized after deletion.
    - [Model Management] Fixed the error when setting model names longer than 20 characters.

### v1.4.0

July 31, 2024

!!! Abstract "New Features :star2:"
    - [Knowledge Base] Support for creating empty knowledge bases.
    - [Knowledge Base] Support for selecting different vector models for vectorization when creating and setting up knowledge bases.
    - [Model Management] Support for adding OpenAI, Ollama, and local vector models.
    - [Model Management] Support for setting model permissions as public or private.
    - [Application] Specified reply nodes in advanced orchestration support quick question output: `<quick_question>Quick Question</quick_question>`.
    - [Application] Support for setting the dialog box entry icon in floating window mode. (X-Pack)
    - [Application] Support for customizing the AI reply avatar in the dialog box. (X-Pack)
    - [Application] Support for setting whether the dialog box in floating window mode can be dragged. (X-Pack)
    - [Application] Support for setting whether the dialog box displays history. (X-Pack)
    - [System Settings] Support for LDAP single sign-on. (X-Pack)
    - [System Settings] Support for customizing theme appearance, setting system website logo, login logo, theme color, login background image, website name, welcome message, etc. (X-Pack)
    - [System Settings] Open system API. (X-Pack)

!!! Abstract "Feature Optimization :sunflower:"
    - [Knowledge Base] Optimized document indexing process to improve knowledge point recall rate.
    - [Knowledge Base] Adjusted maximum segment content length to 100,000 characters.
    - [Application] Adjusted to only allow selection of knowledge bases using the same vector model when associating knowledge bases.
    - [Application] Display knowledge source moved to display settings.
    - [Model Management] Optimized model list style.
    - [About] Optimized displayed information on the About page.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Fixed the issue where crawling tasks are interrupted when encountering inaccessible pages when crawling Web site documents.
    - [Knowledge Base] Fixed scrollbar display issue when there are too many related questions in segment details.
    - [Model Management] Fixed the issue where models from other providers also change to downloading status when Ollama provider has models downloading.
    - [Q&A Page] Fixed the issue where code content in answers doesn't expand and display.
    - [Q&A Page] Fixed the error when deleting a new conversation.

### v1.3.1

July 16, 2024

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application Overview] Opening API access credentials address shows 404.
    - [Application Orchestration] After deleting one condition branch in the judgment node and adding a condition branch again, the frontend sequence number is not updated.
    - [Application Orchestration] The scrollbar for selecting variables in the judgment node cannot be dragged.
    - [Application Orchestration] The order of knowledge base retrieval results in execution details is incorrect, not sorted by similarity in descending order.
    - [Application Orchestration] The content of specified replies returns empty when passed in the task flow.
    - [Q&A Page] When the application's associated knowledge base contains disabled documents, clicking "Try another answer" doesn't provide a new batch of hit segments after asking a question.
    - [Knowledge Base] Online knowledge base crawling reports an error when document names exceed 128 characters.

### v1.3.0

July 4, 2024

!!! Abstract "New Features :star2:"
    - [Application] Support for creating two types of applications: simple configuration and advanced orchestration, with advanced orchestration applications supporting custom workflows.
    - [Application] AI conversation nodes in advanced orchestration support role settings.
    - [Application] AI conversation nodes in advanced orchestration support custom settings for the number of historical chat records to carry.
    - [Application] Advanced orchestration applications support system variables for obtaining current time.
    - [Conversation Logs] Advanced orchestration applications support viewing execution details of each node.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Fixed blocking issue when uploading QA pairs.
    - [Knowledge Base] Fixed the issue where automatic cleaning in advanced segmentation would remove all line breaks.
    - [Application] Fixed the error when asking questions with JSON format content in prompts.

### v1.2.1

June 14, 2024

!!! Abstract "New Features :star2:"
    - [Q&A Page] Historical chat records support logical deletion.

!!! Abstract "Feature Optimization :sunflower:"
    - [Q&A Page] Text input box adapts height according to input text content during conversations.
    - [Application] Maximum reference character count adjusted to 100,000.
    - [Application] Maximum character count for questions during conversations adjusted to 100,000.
    - [Application] Details can be opened even when knowledge source referenced segments is 0.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application] Resolved the error issue when calling the application API documentation interface.
    - [Application] Resolved description error in embedded third-party full-screen mode.
    - [Knowledge Base] Resolved the issue of table format loss after segmenting imported md files with table styles.

### v1.2.0

May 30, 2024

!!! Abstract "New Features :star2:"
    - [Knowledge Base] Support for uploading Excel/CSV format QA pairs, automatic question association.
    - [Knowledge Base] Support for uploading HTML format text files.
    - [Knowledge Base] Support for re-vectorizing knowledge bases and documents.
    - [Knowledge Base] Support for exporting knowledge bases and documents.
    - [Q&A Page] Support for creating new conversations and viewing historical conversations.
    - [Q&A Page] Support for exporting conversation records.

!!! Abstract "Feature Optimization :sunflower:"
    - [Application] Referenced segments in knowledge sources support markdown style display.
    - [Application] Model exception returns should still be recorded in conversation logs after questions.
    - [Application] Questions can be modified when correcting answers in conversation log details.
    - [Application] Maximum number of referenced segments adjusted to 100.
    - [Application] Maximum welcome message character count adjusted to 4096.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application] Resolved the issue where markdown style tables can't be displayed in welcome messages.
    - [Q&A Page] Resolved the "This field cannot be an empty string" error for [User Question] when asking questions.
    - [Knowledge Base] Fixed the error when deleting the last segment.
    - [Knowledge Base] Error when uploading md format documents when a segment's content exceeds 4096 characters.
    - [About] Fixed the issue where version number isn't displayed after refreshing the browser.

### v1.1.3

May 15, 2024

!!! Abstract "New Features :star2:"
    - [Model Management] Support for integrating with Gemini provider models.
    - [Model Management] Support for integrating with DeepSeek provider models.
    - [Model Management] Added gpt-4o model to OpenAI provider's base models.

!!! Abstract "Feature Optimization :sunflower:"
    - [Knowledge Base] Optimized clickable range of checkboxes in document question lists.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Document character count not recalculated after deleting or migrating segments.
    - [Knowledge Base] Error when title is empty during batch import with add title as related question option.
    - [Model Management] Error when adding Ollama models in MaxKB when there are no downloaded models in Ollama.
    - [Model Management] Form not cleared after adding a model.

### v1.1.2

May 10, 2024

!!! Abstract "New Features :star2:"
    - [Knowledge Base] Support for adding titles as related questions when uploading documents (suitable for Q&A pairs where titles are questions).
    - [Knowledge Base] Support for segment migration and batch migration.
    - [Knowledge Base] Support for batch deletion of segments.
    - [Knowledge Base] Support for similarity settings in document direct answers.
    - [Application] Added cross-origin settings for API Keys.

!!! Abstract "Feature Optimization :sunflower:"
    - [Knowledge Base] Optimized uploaded document segment preview to lazy loading to prevent browser crashes with large data volumes.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Fixed inability to save when renaming documents.
    - [Knowledge Base] Fixed import failure in special cases when importing documents.
    - [User Management] Fixed validation failure when usernames contain 0 when creating new users.
    - [UI] Fixed UI file packaging errors.

### v1.1.1

April 30, 2024

!!! Abstract "Feature Optimization :sunflower:"
    - [Knowledge Base] Extended document upload timeout to 1 hour.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application] Fixed error when asking questions with question optimization enabled without selecting an AI model.
    - [Application] Fixed error with multi-turn conversations enabled without selecting an AI model.
    - [Knowledge Base] Fixed invalid retry button when document upload fails.
    - [Knowledge Base] Fixed inability to migrate documents between knowledge bases of the same type.

### v1.1.0

April 29, 2024

!!! Abstract "New Features :star2:"
    - [Knowledge Base] Added two retrieval modes: full-text retrieval and hybrid retrieval.
    - [Knowledge Base] Added hit handling method settings, supporting direct return of segment content or model-optimized answers when document segments are hit.
    - [Knowledge Base] Added document migration functionality.
    - [Knowledge Base] Support for uploading local images when uploading Word documents or adding/editing segment content.
    - [Application] Ability to specify reply content when user questions don't reference knowledge base content.
    - [Application] Added display knowledge source settings for user Q&A page.
    - [Application] Support for custom application logos, displaying custom logos and application names in user browser tabs.

!!! Abstract "Feature Optimization :sunflower:"
    - [Application] Support for not selecting a model when creating/editing applications.
    - [Q&A Page] Optimized streaming output during AI responses for faster data display.
    - [Search Box] Search boxes support one-click clearing of search criteria.
    - [Model Management] Optimized prompt text in add model form.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application] Fixed conversation log details not sorting by time.
    - [Application] Fixed repeated content returns when reaching maximum question limit on Q&A page.
    - [Application] Fixed issue with error content in answers due to inability to get token counts in offline environments.
    - [Application] Fixed issue where editing application information would cause Q&A page to enter 404.
    - [Model Management] Error when adding models when API Key character length is too long.
    - [Q&A Page] Error information appears after AI answers when questions are too long.

### v1.0.4

April 19, 2024

!!! Abstract "New Features :star2:"
    - [Model Management] Support for integrating with Zhipu AI development platform's general models.
    - [Model Management] Support for integrating with Xunfei Sparkdesk models.

!!! Abstract "Feature Optimization :sunflower:"
    - [Login] Current users logging in with default passwords must change their passwords first.
    - [Application] Knowledge bases and documents support search when saving segments during answer correction in conversation log details.

### v1.0.3

April 18, 2024

!!! Abstract "New Features :star2:"
    - [Knowledge Base] Support for selecting folders when uploading documents.
    - [Model Management] Compatible with models conforming to OpenAI format.
    - [Model Management] Support for integrating with Tongyi Qianwen models.
    - [Model Management] Support for integrating with Kimi models.

!!! Abstract "Feature Optimization :sunflower:"
    - [Q&A Page] Optimized efficiency of AI answer output.
    - [Hit Test] Optimized prompt content when no segments are hit.

### v1.0.2

April 17, 2024

!!! Abstract "Feature Optimization :sunflower:"
    - [Knowledge Base] Improved appearance of dropdown component when questions are long when adding related questions in segments.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Fixed error when uploading documents containing null characters (\0) in text files.
    - [Knowledge Base] Error when searching segment titles when the document is empty when associating segments with questions.
    - [Application] Fixed misalignment issue in answers when users only input spaces in questions on the Q&A page.
    - [Application] Stop answer button doesn't work when AI is responding with "...".

### v1.0.1

April 15, 2024

!!! Abstract "Feature Optimization :sunflower:"
    - [Knowledge Base] Case-insensitive queries for document lists, segment titles, segment content, and question lists.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Fixed error in overall knowledge base synchronization.
    - [Knowledge Base] Fixed error when associating questions when adding segments.
    - [Knowledge Base] 404 error when clicking associate segments in the question list when document list is empty.
    - [Application] Fixed "no permission to access" error when clicking segment content in application hit tests.

### v1.0.0

April 11, 2024

!!! Abstract "New Features :star2:"
    - [Knowledge Base] Support for uploading DOCX and PDF format documents.
    - [Knowledge Base] Added question database, support for organizing user questions into the question database and associating them with segments in documents for more precise matching of relevant knowledge points.
    - [Application] Added usage statistics function, supporting statistics on question user data, new question users, number of questions, consumed tokens, and user satisfaction for each application.
    - [Application] Support for exporting conversation logs.
    - [Model Management] Support for integrating with OpenAI models.

!!! Abstract "Feature Optimization :sunflower:"
    - [Application] Added confirmation prompt when regenerating public access links in overview would invalidate embedded third-party scripts.
    - [Application] Updated entry logo for floating mode embedded in third parties.
    - [Knowledge Base] Retained pagination information when returning from document segment details page.
    - [Knowledge Base] Uploaded document limit adjusted to 100 MB.

!!! Abstract "Bug Fixes :palm_tree:"
    - [Knowledge Base] Fixed garbled content issue when getting online knowledge base update logs.
    - [Knowledge Base] Fixed inability to modify knowledge base after creation when entering settings page.
    - [Knowledge Base] Fixed error when uploading documents in unsupported formats.
    - [Application] Fixed unhandled issue when optimized questions return empty strings with question optimization enabled.
    - [Application] Fixed error when adding annotation content from conversation log details.
    - [Application] Fixed misalignment of maximize and close buttons in floating mode.
    - [User Management] Fixed incorrect rule prompt when creating users with default password MaxKB@123...

### v0.9.1

March 27, 2024

!!! Abstract "New Features :star2:"
    - [Model Management] Support for automatic download when adding/modifying Ollama provider models.
    - [About] Added display of project address, user manual, and forum help entry.

!!! Abstract "Feature Optimization :sunflower:"
    - [Model Management] Azure OpenAI base models support custom settings, requiring api-version when customizing.
    - [Model Management] Qianfan large models support custom input of official standard large models (not self-deployed).

!!! Abstract "Bug Fixes :palm_tree:"
    - [Application] Limit to only one quick question at a time during Q&A.
    - [Application] Fixed error issue when large models don't return optimization results with question optimization enabled.
    - [Knowledge Base] Fixed empty content issue due to encoding format problems in uploaded TXT documents.
    - [Knowledge Base] Fixed automatic deselection of documents after checking them in document list.
    - [User Management] Fixed error when deleting users.
    - [User Management] Prevented username modification when editing users.
    - [User Management] Fixed disabled users being able to log in.
    - [User Management] Incorrect error prompt when modified username exceeds length.
    - [User Management] Fixed inability to modify admin user information.
    - [User Management] Fixed user position change after modifying user status.

### v0.9.0

March 20, 2024

!!! Abstract "New Features :star2:"
    - **Ready to Use**: Support for directly uploading documents, automatically crawling online documents, automatic text splitting, vectorization, RAG (Retrieval Augmented Generation), and intelligent Q&A with good interactive experience.
    - **Seamless Integration**: Support for zero-code quick embedding into third-party business systems, enabling existing systems to quickly have intelligent Q&A capabilities, improving user satisfaction.
    - **Multi-model Support**: Support for large language models from Ollama, Baidu Qianfan, and Azure OpenAI.
