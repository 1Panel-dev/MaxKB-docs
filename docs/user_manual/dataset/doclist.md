
## 1 Document Upload

!!! Abstract ""
    For general knowledge bases, click Upload Document button to enter the document upload page. You can drag and drop files or select files/folders to upload. Supported file formats include: TXT, Markdown, PDF, DOCX, HTML, XLS, XLSX, CSV, ZIP. When selecting folders, files will be automatically filtered by extension. Maximum 50 files can be uploaded at once, with each file not exceeding 100 MB.

![Upload Document](../../img/dataset/create_offline_dataset.png)

!!! Abstract ""
    Click Next to set segmentation rules. You can select segmentation rules for uploaded documents, with intelligent segmentation as the default. After changing segmentation rules, click Apply button to display segmentation according to the latest rules. After clicking Start Import button, the system will process documents in the background following the workflow: automatic segmentation, storage, vectorization.

![Intelligent Segmentation](<../../img/dataset/auto_paragraph.png>)

!!! Abstract ""
    For Web site knowledge bases, click Import Document button to open a dialog box where you can enter document links and selectors. Multiple online Web documents can be entered line by line.

![Import Document](../../img/dataset/upload_web_doc.png)

## 2 Sync Knowledge Base

!!! Abstract ""
    Web site knowledge bases support synchronization updates in two ways:

    * Sync and Replace: Re-fetch web site documents and replace documents with matching addresses in the local knowledge base.
    * Full Sync: First delete all documents in the local knowledge base, then re-fetch all documents from the web site.

![Sync Knowledge Base](../../img/dataset/sysn_dataset.png)

## 3 Document Synchronization

!!! Abstract ""
    Web site knowledge bases support synchronization of selected documents. During synchronization, all segments under the current document will be deleted, and text data will be re-fetched from the document address and re-segmented.

![Sync Document](../../img/dataset/sysn_web_doc.png)

## 4 Hit Processing Settings

!!! Abstract ""
    Currently, the document settings support various ways of processing document hits:

    * Model Optimization: When segments under this document are matched during questioning, prompts will be generated according to the application's prompt templates and sent to the model for optimization before returning answers.
    * Direct Answer: When segments under this document are matched during questioning and similarity meets the threshold, segment content is returned directly. This method is recommended when images, links and other information need to be returned.

![Document Settings](../../img/dataset/doc_setting.png)

## 5 Generate Questions

!!! Abstract ""
    Select files and click Generate Questions button or execute generate questions operation. The AI model will summarize the file content to generate corresponding questions and automatically associate them.

![Generate Questions](../../img/dataset/gen_question.png)

## 6 Moving documents

!!! Abstract ""
    Select documents and click [Move] button to move documents to other knowledge bases.

![Moving documents](../../img/dataset/move_web_doc.png)

## 7 Export EXCEL/ZIP

!!! Abstract ""
    Select documents and execute Export Excel/Export Zip operation to download documents to local client.

![Document Export](../../img/dataset/dataset_file_export.png)

## 8 Delete Document

!!! Abstract ""
    Select documents and click delete button or execute delete operation to delete selected documents.

![Delete Document](../../img/dataset/doc_delete.png)

## 9 Enable and Disable Documents

!!! Abstract ""
    In the status column of the document list, you can enable or disable documents. When a document is disabled, the system will not search segments under that document when users ask questions. The system will only search after re-enabling.

![Enable Document](../../img/dataset/doc_enable.png)

## 10 Segment Management

!!! Abstract ""
    After importing, the system segments them according to segmentation rules. Click a document in the document list to enter the document segment management page, where you can add, edit, migrate, delete, enable/disable segments and add related questions to segments.

![Segment Management](<../../img/dataset/segmentation_management.png>)

### 10.1 Add Segment

!!! Abstract ""
    Click Add Segment button to open the add segment dialog box. Fill in segment title, segment content (supports markdown style editing) and related questions, then click Submit button to add a new segment.
    **Recommendation:** To accurately match segments, it's recommended to set related questions for segments. This will prioritize matching related questions before mapping segment content, thereby improving matching efficiency and accuracy.

![Add Segment](../../img/dataset/add_segmentation.png)

### 10.2 Edit Segment

!!! Abstract ""
    Click the segment panel to edit segment information and related questions on the segment details page.
![Segment Details](../../img/dataset/edit_segmentation.png)

### 10.3 Moving section

!!! Abstract ""
    In the segment panel, you can move selected segments to documents in other knowledge bases.

![Moving section](../../img/dataset/move_segmentation.png)

### 10.4 Delete Segment

!!! Abstract ""
    In the segment panel, you can delete selected segments.

![Delete Segment](../../img/dataset/del_segmentation.png)
