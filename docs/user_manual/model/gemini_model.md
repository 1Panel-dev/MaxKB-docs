## 1 添加模型

!!! Abstract ""
    添加 Gemini 大模型之前，需要先在 [Google AI Studio](https://aistudio.google.com/) 创建 API Key。
![Gemini APIKEy](../../img/model/gemini_key.png)

!!! Abstract ""
    选择模型供应商为`Gemini`，并在模型添加对话框中输入如下必要信息：

    * 模型名称：MaxKB 中自定义的模型名称。    
    * 权限：分为私有和公用两种权限，私有模型仅当前用户可用，公用模型即系统内所有用户均可使用，但其它用户不能编辑和删除。     
    * 模型类型：大语言模型。   
    * 基础模型：不同类型模型下的基础模型名称，下拉选项是常用的一些基础模型名称，支持自定义输入。
    * API Key：获取 API Key。

    **注意：** 使用 Gemini API 需要确保程序所在服务器位于 [Gemini API 所支持的地区](https://ai.google.dev/gemini-api/docs/available-regions?hl=zh-cn) ，否则无法调用API，并且无法进入Google AI Studio。

## 2 配置样例

!!! Abstract ""
    Gemini-大语言模型配置样例图示：

![gemini 模型](../../img/model/gemini_llm.png){ width="500px" }