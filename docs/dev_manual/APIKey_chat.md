# 应用API

!!! Abstract ""
    MaxKB 支持提供系统应用 API 以及兼容 OpenAI 标准格式调用对话。

## 1 应用API

### 1.1 打开swagger文档

!!! Abstract ""
    在应用-概况-应用信息中复制并访问 swagger 地址。

![API doc](../img/dev/app_swaagger.png)

### 1.2 API Key 认证
  
![APIKEY](../img/dev/app_apikey.png)

### 1.3 获取应用信息

!!! Abstract ""
    调用 profile 接口，获取应用详细信息（应用 id、name等）。
  
![ profile](../img/dev/app_profile.png)

### 1.4 打开会话

!!! Abstract ""
    调用打开会话接口，输入上述步骤获取的应用 id，打开会话并获取会话 id。

![appid](../img/dev/chat_open.png)

### 1.5 进行对话

!!! Abstract ""
    调用对话接口，输入会话 id 进行对话。

![chatid](../img/dev/app_chat.png)

## 2 标准OpenAI 格式

!!! Abstract ""
    MaxKB 应用兼容 OpenAI API 格式，在OpenAI API 原有调用方式的基础上替换为 MaxKB 应用提供的 Base URL 以及 API Key 即可。

![API doc](../img/dev/openai_baseurl.png)

!!! Abstract ""

    ```
    # 将url 和 Authorization 替换为 MaxKB 应用实际真实的 Base URL 和 API Key。

    curl https://maxkb.fit2cloud.com/api/application/xxxxxxxx-8c56-11ef-a99e-0242ac140003/chat/completions_ \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer application-xxxxxxxxf00e21a7530d1177c20967"  \
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


