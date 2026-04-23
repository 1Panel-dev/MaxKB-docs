# 接入第三方


!!! Abstract "" 
    支持创建的智能体的与企业微信智能机器人、企业微信智能体、企业微信客服、公众号（服务号和订阅号）、钉钉智能体、飞书智能体接入，实现企业内部员工、外部公众进行对话。
    
### 1 企业微信智能机器人

!!! Abstract ""
    企业微信机器人支持在 **企业微信内部群聊** 中@智能机器人进行问答对话。
![对话演示](../../img/app/wechat_ai_asker.png)


!!! Abstract ""
    在智能体接入中点击【企业微信智能机器人】的配置按钮，配置信息中会自动生成回调 URL，并需要复制到企业微信智能机器人的 API 接收设置中的 URL 中。

![企微机器人配置](../../img/app/wechat_ai_add.png)

!!! Abstract ""
    创建机器人：在[企业微信管理后台](https://work.weixin.qq.com/wework_admin/frame#apps)，点击 【安全与管理】-【管理工具】-【智能机器人】-【创建机器人】。

![创建企微机器人](../../img/app/wechat_ai_create.png)
![创建企微机器人](../../img/app/wechat_ai_create1.png)


!!! Abstract ""
    选择【API 模式创建】。

![API模式创建](../../img/app/wechat_ai_API.png)

!!! Abstract ""
    填写基本信息后，在 URL 中，写入 MaxKB 智能体配置中的回调地址，同时，将随机生成的 Token 和 Encoding-AESKey 填写在 MaxKB 智能体配置中，并保存智能体配置。保存后，回到企业微信管理后台创建机器人。


    **注意：** 在企业微信智能体API接收消息配置保存之前，一定要在 MaxKB 中完成企业微信智能体配置并保存，不然保存时将报错`openapi回调地址请求不通过`。


![回调地址](../../img/app/wechat_ai_recall.png)

!!! Abstract ""
    创建完成后，即可在 **企业微信内部群聊** 中@智能机器人，进行提问。

![对话演示](../../img/app/wechat_ai_asker.png)


### 2 企业微信智能体

!!! Abstract ""
    企业微信智能体对接后，可在【企业微信】-【工作台】的智能体中找到对应的智能体并进行对话

![企业微信对话](../../img/app/enter_wechat_dialog.png)

!!! Abstract ""
    在智能体接入中点击【企业微信智能体】的【配置】按钮，配置信息中会自动生成回调 URL，并需要复制到企业微信智能体的 API 接收设置中，除此之外的其它信息，将在企业微信管理后台中生成并获取。 

![显示设置](../../img/app/ent_wechat_setting.png)

!!! Abstract ""
    获取企业ID: 在[企业微信管理后台](https://work.weixin.qq.com/wework_admin/frame#apps)，点击 【我的企业】菜单，在最下方可以看到企业ID 信息。

![企业ID](../../img/system/obtain_wxid.png)


!!! Abstract "" 
    创建企业微信智能体：在【智能体管理】中点击【创建智能体】，选择智能体logo，设置智能体名称和智能体介绍以及可见范围。


![企业微信智能体设置](../../img/app/robot_info.png)


!!! Abstract ""
    获取 Agentid 和 Secret:进入创建的智能体，获取 AgentId 和 Secret。点击【查看】Secret 将通过企业微信进行查看。 

![企微智能体信息](../../img/system/qiwei_appinfo.png)

!!! Abstract ""
    获取 Token 和 EncodingAESKey：进入企业微信智能体设置的【接收消息】-【设置 API 接收】，随机获取 Token 和 EncodingAESKey。

    在 MaxKB 企业微信智能体配置输入对应的参数并保存，回到企业微信智能体设置【接收消息】-【设置API接收】企业微信智能体接入配置中自动生成的回调 URL，最后点击【保存】。

    **注意：** 在企业微信智能体API接收消息配置保存之前，一定要在 MaxKB 中完成企业微信智能体配置并保存，不然保存时将报错`openapi回调地址请求不通过`。

![设置API接收](../../img/app/recmsg_api.png)


!!! Abstract ""
    **注意：** 在企业微信智能体API接收消息配置保存之前，一定要在 MaxKB 中完成企业微信智能体配置并保存，不然保存时将报错`openapi回调地址请求不通过`。

![设置API接收](../../img/app/recmsg_api_setting.png)



!!! Abstract ""
    配置企业可信 IP：进入企业微信智能体设置的【企业可信 IP】中，把 MaxKB 服务的 IP 地址设置为可信 IP。

![配置可信IP](../../img/system/qiwei_ip.png)

!!! Abstract "" 

    以上步骤配置完成后，并在企业微信智能体接入配置中输入企业微信智能体信息后保存，便可在企业微信智能体中找到机器人进行对话。

![企业微信对话](../../img/app/enter_wechat_dialog.png)


### 3 企业微信客服

!!! Abstract ""
    企业微信客服对接后，可以在群聊中 @微信客服，通过跳转连接，实现客服一对一问答。

![企业微信客服账号](../../img/app/dialog_cs.png){ width="500px" }
    
!!! Abstract ""
    MaxKB 智能体接入企业微信智能体后，在此基础上，还可以将此智能体接入到微信客服，对外部用户提供服务。   
    创建客服账号：在企业微信管理后台的【智能体管理】中，点击【微信客服】，并创建账号,客服账号的接待方式选择：机器人+人工接待

![企业微信客服账号](../../img/app/weichat_customservice.png)

![企业微信客服账号](../../img/app/create_cs_account.png)

!!! Abstract ""
    客服账号与智能体关联：在微信客服中配置【可调用接口的智能体】，并配置客服账号。

![企业微信客服账号](../../img/app/cs_app.png)

![企业微信客服账号](../../img/app/config_cs_account.png)

!!! Abstract ""
    开启客服助理：在企业的外部群设置中开启【客服助理】，微信客服便会加入群中，群里的任何用户仅需要@客服助理，即可发起咨询，并微信客服进行一对一的对话。

![企业微信客服账号](../../img/app/enable_cs.png){ width="500px" }
![企业微信客服账号](../../img/app/dialog_cs.png){ width="500px" }



### 4 微信公众号

!!! Abstract ""
    对接后，可直接通过微信公众号实现问答对话。
![公众号对话](../../img/app/public_account_dialog.png){ width="500px" }

!!! Abstract "" 
    在智能体接入中点击【公众号】的【配置】按钮，配置信息中会自动生成回调 URL,并需要复制到【微信公众平台-设置与开发-基本配置-服务器配置】服务器地址 URL 中，除此之外的其它信息，将在微信公众平台中生成并获取。
![公众号配置](../../img/app/public_account_setting_empty.png)

!!! Abstract "" 
    获取 APP ID、APP Secret、Token 和消息加解密密钥：在微信公众平台-设置与开发-基本配置中获取 APP ID、APP Secret 信息，并启动服务器配置，生成 Token 和消息加解密密钥。
![公众号信息](../../img/app/public_account_basicinfo.png)
![公众号信息](../../img/app/public_account_setting1.png)

!!! Abstract "" 
    将生成的 APP ID、APP Secret、Token 和消息加解密密钥信息输入到 MaxKB 公众号配置窗口中，并保存。
![公众号信息](../../img/app/public_account_setting2.png)

!!! Abstract ""
    将【公众号-基本配置-服务器配置】中的 URL 设置为 MaxKB 公众号配置窗口中的回调地址 URL，然后提交，并启用服务器配置。

![公众号信息](../../img/app/public_account_setting_url.png)

!!! Abstract "" 
    开启客服接口权限。
![客服接口权限](../../img/app/public_account_enable_api.png)

!!! Abstract "" 
    设置 IP 白名单：进入公众号基本配置的【IP 白名单】中，添加 MaxKB 服务器的 IP 地址。
![公众号IP白名单](../../img/app/public_account_ip.png)

!!! Abstract "" 
    根据以上步骤完成配置后，即可在公众号中发送消息进行对话。

![公众号对话](../../img/app/public_account_dialog.png){ width="500px" }


### 5 钉钉智能体

!!! Abstract ""
    接入钉钉后，可在群聊中@机器人，进行问答对话。
![钉钉机器人对话](../../img/app/ding_dialog1.png)

!!! Abstract ""
    在智能体接入中点击【钉钉智能体】的【配置】按钮，配置信息中会自动生成回调 URL,并需要复制到钉钉-机器人设置-消息接收地址中，其它信息，将在钉钉开放平台中生成并获取。

![钉钉机器人创建](../../img/app/dingding_setting.png)

!!! Abstract ""
    创建机器人：在 [钉钉开放平台](https://open-dev.dingtalk.com/)的【智能体开发】-【钉钉智能体】中，点击【创建智能体】，填写智能体信息后，点击【保存】。

![钉钉机器人创建](../../img/app/dingding_robot_create.png)

!!! Abstract ""
    获取 Client ID 和 Client Secret：进入创建好的钉钉智能体，打开【凭证与基础信息】页面，获取 Client ID 和 Client Secret。

![钉钉智能体信息](../../img/app/dingding_info.png)

!!! Abstract ""
    在 MaxKB 钉钉智能体配置窗口中输入步骤获取的 Client ID 和 Client Secret 智能体凭证，并保存。

![钉钉智能体信息](../../img/app/dingding_setting2.png)

!!! Abstract ""
    点击【添加智能体能力】，选择 【机器人】能力，点击 【添加】，输入机器人基本配置信息后，将【消息接收模式】设置为 HTTP 模式，并将 MaxKB 钉钉智能体配置中的回调地址的URL填写到消息接收地址中，然后点击【发布】。
![钉钉机器人添加](../../img/app/dingding_robot_add.png)
![钉钉机器人息接收模式](../../img/app/dingding_msg_recvmode.png)

!!! Abstract ""
    根据以上步骤完成配置后，就可以群里@机器人中进行对话，或与机器人智能体一对一对话。

![钉钉对话](../../img/app/dingding_dialog.png){ width="500px" }


### 6 飞书智能体
!!! Abstract ""
    接入飞书后，可在智能体中找到对应智能体，进行问答对话。
![飞书对话](../../img/app/feishu_dialog1.png){width="500px"}

!!! Abstract ""
    在智能体接入中点击【飞书智能体】的【配置】按钮，配置信息中会自动生成回调 URL，并需要复制到【飞书开放平台-事件与回调-事件配置-配置订阅方式】的请求地址中，除此之外的其它信息，将在飞书开放平台中生成并获取。

![飞书智能体配置](../../img/app/feishu_setting.png)

!!! Abstract ""
    创建飞书机器人：首先在 [飞书开发平台](https://open.feishu.cn/app/)的【企业自建智能体】中，点击【创建企业自建智能体】，填写智能体信息。
![飞书添加机器人](../../img/app/feishu_create_app.png)

!!! Abstract ""
    点击【添加智能体能力】，选择 【按能力添加-机器人】，点击【添加】
![飞书添加机器人](../../img/app/feishu_add_robot.png)

!!! Abstract ""
    添加权限：打开【权限管理】，复制下面的权限配置并粘贴到【API 权限-权限配置】输入框，全选筛选出来的权限项，点击【批量开通】，最后点击【确认】。

    ```
     contact:contact.base:readonly,contact:user.base:readonly,im:message.group_at_msg:readonly, im:message.p2p_msg:readonly,im:message:send_as_bot,im:resource
    ```

![飞书权限](../../img/app/feishu_app_auth.png)

!!! Abstract ""
    获取 APP ID、APP Secret 和 Verification Token：进入创建好的飞书智能体，打开【凭证与基础信息】页面，获取 APP ID 和 APP Secret。
![飞书智能体信息i](../../img/app/feishu_app_info.png)


!!! Abstract ""
    打开【事件与回调-加密策略】，获取 Verification Token。

![飞书token](../../img/app/feishu_verify_token.png)

!!! Abstract ""
    在 MaxKB 飞书智能体配置窗口输入上述信息，并保存。

![飞书事件与回调](../../img/app/maxkb_feishu_config.png)


!!! Abstract ""
    配置回调URL：在飞书开放平台中打开【事件与回调】-【回调配置】的订阅方式中，将MaxKB中飞书智能体的回调地址的URL填写到【请求地址】中。
![飞书事件与回调](../../img/app/feishu_event_config1.png)

![飞书事件与回调](../../img/app/feishu_event_config2.png)


!!! Abstract ""
    发布智能体：点击【创建版本】，填写版本信息后，点击【保存】。
![飞书智能体发布](../../img/app/feishu_app_create1.png)

![飞书智能体发布](../../img/app/feishu_app_create2.png)

!!! Abstract ""
    确认发布后，智能体状态将更新为`已启用`。
![飞书智能体发布](../../img/app/feishu_app_enabled.png)

!!! Abstract ""
    根据以上步骤完成配置后，即可打开飞书客户端搜索`MaxKB小助手`，点击【添加】后进行一对一对话。

![飞书对话](../../img/app/feishu_app_search.png){width="500px"}   ![飞书对话](../../img/app/feishu_dialog.png){width="500px"}

