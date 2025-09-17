# 系统 API 

## 1 API Key 管理

!!! Abstract "" 
    在页面右上方登陆用户图标下拉菜单中，点击【API Key 管理】菜单，进入 API Key 管理窗口，可以创建、启用/关闭、删除、设置 API Key 等操作。

![API-key](../../img/system/apikey.png)  

!!! Abstract "" 
    创建 API Key 之后，点击【设置】下方可以配置是否允许跨域地址，默认不允许。

![API-key](../../img/system/apikey_setting.png)  

## 2 API 调试

!!! Abstract "" 
    打开 API 文档地址后，输入 API Key 进行授权，即可进行 API 在线调试。

![swagger](../../img/system/swagger_api.png)

!!! Abstract ""
    注意：当使用的接口涉及应用对话时，Authorize 需填写应用的 API Key（application-0d5722xxxxxxxxx），否则会出现如下报错：
![swagger](../../img/system/swagger_apinotice.png)



## 3 开启身份验证的 API 调用
!!! Abstract ""
    开启身份验证后的 API 调用使用的 Authorize 与[通过 API Key 进行对话](https://maxkb.cn/docs/v2/user_manual/chat_to_api/)的获取方式有所不同，以账号登录为例。
![登录认证](../../img/system/api_login.png)

### 3.1 登录 API 地址
!!! Abstract ""
    点击用户头像，选择【API Key 管理】。
![打开api key管理](../../img/system/api_open_apikey.png)

!!! Abstract ""
    创建 API Key，复制并打开【API 服务地址】。
![打开api文档](../../img/system/api_create_apikey.png)

!!! Abstract ""
    点击【Authorize】，在【value】中输入系统的 API Key。
![登录api文档](../../img/system/api_login_apikey.png)


### 3.2 获取 Authorize
!!! Abstract ""
    调用 captcha 接口，获取验证码，获取到的验证码是 Base64 编码的 PNG 图片数据。
    
    **注意：需自行将 Base64 数据解码并转换为图片文件。**
![登录api文档](../../img/system/api_captcha.png)

!!! Abstract ""
    在应用概览页面复制应用的 access_token。
![access_token](../../img/system/api_access_token.png)

!!! Abstract ""
    在 API 地址找到对话用户/登录，输入 access_token，填入账号密码等信息，生成登录的 token。
![access_token](../../img/system/api_authorize.png)
![access_token](../../img/system/api_authorize1.png)

### 3.3 API 调用
!!! Abstract ""
    进入应用【概览】的 API 文档地址，将获取的 token 填入【Authorize】中，即可根据：[通过 API Key 进行对话](https://maxkb.cn/docs/v2/user_manual/chat_to_api/)，正常进行 API 对话。
![API 登录](../../img/system/api_login_auth.png)
![API 登录](../../img/system/api_login_auth1.png)