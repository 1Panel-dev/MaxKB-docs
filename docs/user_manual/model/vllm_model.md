## 1 添加模型

!!! Abstract ""
    选择模型供应商为`vLLM`，并在模型添加对话框中输入如下必要信息：

    * 模型名称：MaxKB 中自定义的模型名称。    
    * 权限：分为私有和公用两种权限，私有模型仅当前用户可用，公用模型即系统内所有用户均可使用，但其它用户不能编辑和删除。
    * 模型类型：大语言模型/向量模型/视觉模型。   
    * 基础模型：不同类型模型下的基础模型名称，下拉选项是常用的一些基础模型名称，支持自定义输入。      
    * API 域名：vLLM 服务地址， 如：http://192.168.20.242:8000/v1 。 
    * API Key：若没有 API Key，输入任意字符即可。

## 2 配置样例

!!! Abstract ""
    vLLM-大语言模型配置样例图示如下：

![vLLM LLM模型](../../img/model/vLLM_llm.png){ width="500px" }

!!! Abstract ""
    vLLM-向量模型配置样例图示如下：

![vLLM LLM模型](../../img/model/vllm_embedding.png){ width="500px" }

!!! Abstract ""
    vLLM-视觉模型配置样例图示如下：

![vLLM 视觉模型](../../img/model/vllm_version_gen.png){ width="500px" }