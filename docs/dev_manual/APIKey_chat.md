!!! Abstract ""
    The MaxKB community edition provides system application APIs and supports conversation in a format compatible with the OpenAI standard. The professional edition offers system-level APIs. For more details, refer to: [System API](../user_manual/X-Pack/system_API.md).

## 1 Application API

### 1.1 Open API Documentation

!!! Abstract ""
    Copy and access the swagger address from the application information.

![API doc](../img/dev/app_swagger.png)

### 1.2 API Key Authentication

![APIKEY](../img/dev/app_apikey.png)

### 1.3 Retrieve Application Information

!!! Abstract ""
    Call the profile interface to get detailed application information (such as application ID, name, etc.).

![profile](../img/dev/app_profile.png)

### 1.4 Open a Session

!!! Abstract ""
    Call the open session interface, enter the application ID obtained in the steps above, open a session, and obtain a session ID.

![appid](../img/dev/chat_open.png)

### 1.5 Conduct a Conversation

!!! Abstract ""
    Call the conversation interface, and enter the session ID to conduct a conversation.

![chatid](../img/dev/app_chat.png)

## 2 Standard OpenAI Format

!!! Abstract ""
    The MaxKB application is compatible with the OpenAI API format. You can replace the original OpenAI API Base URL and API Key with those provided by the MaxKB application.

![API doc](../img/dev/openai_baseurl.png)

!!! Abstract ""

    ```
    # Replace the URL and Authorization with the actual Base URL and API Key from the MaxKB application.

    curl https://maxkb.fit2cloud.com/api/application/xxxxxxxx-8c56-11ef-a99e-0242ac140003/chat/completions \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer application-xxxxxxxxf00e21a7530d1177c20967"  \
        -d '{
            "model": "gpt-3.5-turbo",
            "messages": [
                {
                  "role": "You are the intelligent assistant of MaxKB, a product under Hangzhou Fit2Cloud Technology. Your job is to assist MaxKB users in solving problems they encounter during usage. When users come to you with questions, make sure to focus on the MaxKB Q&A system.",
                  "content": "What is MaxKB?"
                }
            ]
        }'
    ```
