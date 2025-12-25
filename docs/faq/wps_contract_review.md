!!! Abstract ""

    通过 MaxKB 开源智能体平台对接 WPS Office，打造一款“智能合同审核助手”的具体方法。
    
    将企业的合同知识库能力直接集成到日常办公环境中，让合同审核从原本需要数天的人工流程，转变为几分钟内就能完成的智能化操作，在保持审核标准统一的同时，大幅提升了合同审核的效率和准确性。

## 1 方案设计

!!! Abstract ""
    
    MaxKB WPS合同审核工作流的核心是实现分类选择知识库、文档预处理，以及利用SSE（‌即Server-Sent Events，服务器发送事件‌）技术实时推送审核结果。
    
    用户在MaxKB中预先配置合同审核工作流并发布，然后在WPS中安装MaxKB WPS插件，并接入合同审核工作流，即可在WPS内实现高效的合同审核。
    
    整体流程说明如下:

    (1) 配置管理：用户首次使用时，配置MaxKB服务地址、APP Key和销售人员姓名；

    (2) 分类选择：根据合同所属产品线（例如DataEase、JumpServer等）和类型（订阅、授权、维保等）选择对应的知识库；

    (3) 文档预处理：自动接受所有修订痕迹、删除批注，确保文档干净整洁；

    (4) 导出PDF：为文件名添加时间戳后缀，将Word文档转换为PDF格式；

    (5) 上传文件：将PDF文件上传至MaxKB文件服务；

    (6) 智能审核：MaxKB智能体根据选择的分类，调用对应的企业知识库进行合同分析；

    (7) 流式返回：采用SSE技术实时推送审核结果，用户可以看到分析过程；

    (8) 实时渲染：将返回的Markdown内容实时渲染，并展示在任务窗格中；

    (9) 导出报告：将审核结果生成专业的PDF报告，保存在原合同相同的目录中；

    (10) 恢复文档：删除临时文件，重新打开原始合同文档。
    
    MaxKB WPS合同审核助手的实现采用前后端分离的架构，前端负责文档处理和界面展示，后端提供AI审核服务。
    用户在前端上传文件后，文档在MaxKB中经过文档合并、PDF转换、解析及判断器分类等，随后交由AI结合知识库检索结果进行审核，最终将审核结果返回前端并将渲染的结果展现给用户。

![wps_contract](../img/FAQ/MaxKB WPS合同审核助手架构图.jpeg)
![wps_contract](../img/FAQ/MaxKB合同审核周手工作流.png)

## 2 插件安装

### 2.1 macOS操作系统

!!! Abstract ""

    打开终端，执行以下命令：
    '''
    curl -sSL https://east.dataease.cn/maxkb_wps_quick_start.sh | bash
    '''

    该脚本会自动下载并安装插件至WPS的插件目录：~/Library/Containers/com.kingsoft.wpsoffice.mac/Data/.kingsoft/wps/jsaddons。

![wps_contract](../img/FAQ/macOS_MaxKB WPS插件安装.png)

### 2.2 Windows操作系统

!!! Abstract ""
    
    在网页中下载插件：https://maxkb-tools-1323865188.cos.ap-guangzhou.myqcloud.com/maxkb-wps.exe。

    运行后，插件将被自动安装至：C:\Users\${Your_Name}\AppData\Roaming\kingsoft\wps\jsaddons。

![wps_contract](../img/FAQ/Windows_MaxKB WPS插件安装.png)

## 3 实现步骤与效果展示

!!! Abstract ""
    
    通过MaxKB WPS合同审核助手，用户几分钟内就可以搞定以往需要数小时的合同审核工作。以下是详细的操作步骤与效果说明：

    (1) 配置系统

    首次使用时，在WPS上方工具栏找到“MaxKB WPS插件”选项，然后点击“合同审核”按钮，在页面右侧的工具栏点击右上角的齿轮图标进行初始化配置，填入MaxKB服务的Base URL、APP Key以及销售姓名等审核信息。
    
    - Base URL：MaxKB服务地址
    - APP Key：应用级别的认证密钥
    - 销售姓名：审核人员信息

![wps_contract](../img/FAQ/MaxKB WPS插件菜单.png)
![wps_contract](../img/FAQ/MaxKB WPS初始化_01.png)
![wps_contract](../img/FAQ/MaxKB WPS初始化_02.png)

!!! Abstract ""

    (2) 选择合同分类   

    根据合同内容选择对应的知识库，先选择产品线（例如DataEase、MaxKB等），再选择合同类型（例如订阅、授权、维保等）。

    系统会根据所选分类自动匹配对应的知识库，确保审核逻辑与企业标准一致。

![wps_contract](../img/FAQ/WPS合同审核助手知识库选择.png)


!!! Abstract ""
   
    (3) 一键审核   

    上传一份合同文件，系统自动完成文档的预处理（例如接受修订、删除批注等）、导出PDF文件、调用智能体分析合同等操作，并实时展示审核结果。

![wps_contract](../img/FAQ/MaxKB WPS合同审核助手审核结果展示.png)


!!! Abstract ""
   
    (4) 查看审核报告

    审核完成后，系统会在任务窗格中展示完整的审核报告，内容包括：

    ■ 审核概览：合同的基本信息、审核人员、审核时间； 

    ■ 风险评估：高风险、中风险、低风险条款；

    ■ 条款分析：逐条审查合同条款，标注潜在问题； 

    ■ 合规性检查：与企业标准对照，指出不合规项；

    ■ 修改建议：具体的修改意见和参考文本。

![wps_contract](../img/FAQ/MaxKB WPS合同审核助手审核报告.png)

!!! Abstract ""
   
    (5) 导出PDF报告

    系统自动将审核报告导出为PDF文件，保存在原合同同目录下。PDF报告遵循的规范包括：

    ■ 文件名格式：原合同名_合同审查结果_20241210_153045.pdf

    ■ 格式完整保留：Markdown格式、表格、列表等； 

    ■ 智能分页：避免标题、表格、代码块被截断。

![wps_contract](../img/FAQ/MaxKB WPS合同审核助手审核报告导出.png)

