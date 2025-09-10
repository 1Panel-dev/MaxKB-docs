# 通过API KEY进行对话

!!! Abstract ""
    MaxKB 创建的应用支持通过 OpenAI SDK 格式以及提供系统 SDK 接入，专业版在社区版本基础上提供平台级别的完整 SDK，详细情况见：[系统API](https://maxkb.cn/docs/v2/user_manual/X-Pack/system_API/)。

## 1 标准OpenAI API格式

!!! Abstract ""
    MaxKB 应用兼容 OpenAI API 格式，在 OpenAI API 原有调用方式的基础上替换为 MaxKB 应用提供的 Base URL 以及 API Key 即可。
![api示例](../../img/system/api_example.png)

!!! Abstract ""
    ``` 
    # 将 url 和 Authorization 替换为 MaxKB 应用实际真实的 Base URL 和 API Key。

    curl https://maxkb.fit2cloud.com/chat/api/xxxxxxxx-3fdf-7941-a6f4-0572478f57f6 \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer application-xxxxxxxxxx987f1bc06ab16e0ef"  \
        -d '{
            "model": "gpt-3.5-turbo",
            "messages": [
                {
                  "role": "你是杭州飞致云信息科技有限公司旗下产品 MaxKB 知识库问答系统的智能小助手，你的工作是帮助 MaxKB 用户解答使用中遇到的问题，用户找你回答问题时，你要把主题放在 MaxKB 知识库问答系统身上。",
                  "content": "MaxKB 是什么？"
                }
            ]
        }'
    ```

## 2 系统 API

### 2.1 打开 API 文档
!!! Abstract ""
    在应用【概览】中，点击访问 MaxKB API 地址，在 API Key 中创建 API Key。
![打开文档](../../img/system/open_api_doc.png)
![打开文档](../../img/system/open_api_doc1.png)
### 2.2 API Key 认证
!!! Abstract ""
    点击【Authorize】，输入已创建的 API Key。
![API 认证](../../img/system/api_auth.png)

### 2.3 获取会话信息
!!! Abstract ""
    通过调用 open 接口，可以生成会话 id。
![会话ID](../../img/system/api_chatid.png)

### 2.4 进行会话
!!! Abstract ""
    调用对话接口，填入已获取的会话 id，输入问题等参数信息，即可进行对话。
![对话](../../img/system/api_chat.png)
![对话](../../img/system/api_chat1.png)

