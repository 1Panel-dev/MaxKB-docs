# 文档

!!! Abstract ""
    MaxKB 知识库文档支持同步、重新向量化、标签设置、生成问题、迁移、设置、导出以及删除操作。

![上传文档](../../img/dataset/document_action.png)

## 1 文档上传

!!! Abstract ""
    对于通用型知识库，点击【上传文档】进入上传文档页面，可以拖拽文件或选择文件/文件夹进行上传。
    支持的文件格式包括：TXT、Markdown、PDF、DOCX、HTML、XLS、XLSX、CSV、ZIP。如果选择文件夹，将通过文件后缀进行自动过滤，每次最多上传 50 个文件，且单个文件不超过 100 MB。

![上传文档](../../img/dataset/upload_document.png)

!!! Abstract "" 
    对于 Web 站点知识库，点击【导入文档】打开对话框，输入文档链接 URL 地址和选择器，即可同步对应内容。

![导入Web文档](../../img/dataset/upload_web_doc.png)

## 2 文档同步 

!!! Abstract ""     
    Web 站点知识库支持对选中文档进行同步操作。同步时会先删除当前文档下的所有分段，并重新获取文档地址的文本数据后重新分段。   

![同步文档](../../img/dataset/sysn_dataset.png)
    

## 3 设置

!!! Abstract ""
    命中处理方式：

    * 模型优化：提问时命中该文档下面的分段后，会按照智能体的提示词生成 prompt 发送给模型优化后返回答案。
    * 直接回答：提问时命中该文档下面的分段后，若相似度符合设置则直接返回分段内容。对于需要将图片、链接等信息返回要求，建议使用此方式。     
!!! Abstract ""    
    允许在知识库来源中下载： 通用知识库和飞书知识库的文档支持选择是否【允许在知识来源中下载】的设置功能，勾选后，包含该知识库文档的智能体，回答内容将支持下载知识来源。

![文档设置](../../img/dataset/doc_setting.png)

## 4 生成问题

!!! Abstract ""   
    选中文档，点击【生成问题】按钮或执行生成问题操作，将通过 AI 模型（支持设置模型参数），根据文件内容总结生成对应的问题，并自动关联。

![生成问题](../../img/dataset/gen_question.png)

![生成问题](../../img/dataset/gen_question2.png)

## 5 文档迁移

!!! Abstract ""  
    选中文档，点击【迁移】按钮，将文档迁移到其它知识库。

![迁移文档](../../img/dataset/move_web_doc.png)

## 6 标签

!!! Abstract ""
    标签管理：每个知识库都拥有独立的标签管理体系。点击【标签管理】即可创建标签，一个知识库可设多个标签，每个标签可设置多个标签值。

![标签管理](../../img/dataset/Tag_Manage1.png)
![标签管理](../../img/dataset/Tag_Manage.png)

!!! Abstract ""
    添加标签：选中文档，点击【添加标签】，即可为文档批量添加已创建的标签，每个文档支持添加多个标签。

![添加标签](../../img/dataset/add_tag.png)
![添加标签](../../img/dataset/add_tag1.png)

!!! Abstract ""
    标签设置：点击【标签设置】，即可查看、添加或删除文档已绑定的标签。

![标签管理](../../img/dataset/tag_setting.png)
![标签管理](../../img/dataset/tag_setting1.png)

## 7 导出 Excel/ZIP

!!! Abstract ""  
    选中文档，执行导出 Excel/导出 Zip 操作，将文档下载到本地客户端。

![文档导出](../../img/dataset/dataset_file_export.png)

## 8 下载原文档

!!! Abstract ""
    选中文档，点击【下载原文档】，可以将原文档下载到本地，保留原始文件。

    **注意**：下载原文档功能仅允许手动在【上传文档】中上传的文件，否则会出现报错：`文件不存在，仅支持手动上传的文档`。

![文档下载原文件](../../img/dataset/doc_down.png)

## 9 替换原文档

!!! Abstract ""
    通用型知识库支持替换原文档。点击【替换原文档】，可以手动上传文件，替换原文档的内容。

    注意：

    - 替换原文档仅更新文档本身，已向量化和分段的内容保持不变；
    - 替换后，智能体开启显示知识来源时，引用分段中显示的文档将是更新后的文档。

![文档替换原文件](../../img/dataset/replay_doc.png)
![文档替换原文件](../../img/dataset/replay_doc1.png)

## 10 文档删除

!!! Abstract ""  
    选中文档，点击删除按钮或执行删除操作，对选中文档进行删除。

![文档删除](../../img/dataset/doc_delete.png)

## 11 文档启用与禁用

!!! Abstract ""    
    在文档列表中的状态列，可对文档执行启用或禁用操作。文档禁用后，当用户提问时系统不会检索该文档下的分段内容，需要重新启用后系统才会检索。  

![文档启用](../../img/dataset/doc_enable.png)

## 12 分段管理

!!! Abstract ""
    导入文档后，系统根据分段规则进行分段操作。点击文档列表中的文档，进入文档分段管理页面，可启用/禁用分段、编辑、上方插入、迁移、移动位置、删除以及为分段添加关联问题。 

![分段管理](<../../img/dataset/segmentation_management.png>)

### 12.1 添加分段 

!!! Abstract "" 
    点击【添加分段】，弹出添加分段对话框，填写分段标题、分段内容（支持 Markdown 样式编辑分段内容）和关联问题，点击【提交】后则新增一个分段。           
    **建议：** 为了能准确匹配到分段，建议为分段设置关联问题，这样会优先匹配关联问题，然后再映射分段内容，从而提高匹配效率和准确度。 

![添加分段](../../img/dataset/add_segmentation.png)

### 12.2 编辑分段

!!! Abstract ""    
    点击分段面板，在分段详情页面对已分段的信息进行编辑和关联问题操作。

![分段详情](../../img/dataset/edit_segmentation.png)


### 12.3 迁移分段

!!! Abstract ""  
    在分段面板中可以对选中分段迁移到其它知识库的文档中。

![迁移分段](../../img/dataset/move_segmentation.png)

### 12.4 移动位置
!!! Abstract ""  
    在分段面板中可以对选中分段进行上移或下移操作。
![移动位置](../../img/dataset/upanddown_segmentation.png)

### 12.5 删除分段

!!! Abstract ""  
    在分段面板中可以对选中分段进行删除。

![删除分段](../../img/dataset/del_segmentation.png)
