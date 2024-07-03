## 1 环境要求
!!! Abstract ""
    **安装前请确保您的系统符合安装条件：**

    * 操作系统：Ubuntu 22.04 / CentOS 7 64 位系统；
    * CPU/内存： 推荐 2C/4GB 以上；
    * 磁盘空间：100GB；
    * 浏览器要求：请使用 Chrome、FireFox、Safari、Edge等现代浏览器；
    * **可访问互联网**。


## 2 离线部署 （生产环境推荐使用该方式部署）

!!! Abstract ""
    **注意：离线包仅支持x86服务器。**

    打开社区网站下载 MaxKB 离线包
    [社区版离线包](https://community.fit2cloud.com/#/products/maxkb/downloads)

    上传至服务器后进行解压缩，执行以下命令：
    ```
    # maxkb-v1.2.0-offline.tar.gz替换成下载包的名字  
    tar -zxvf maxkb-v1.2.0-offline.tar.gz
    ```
    安装 MaxKB， 执行以下命令：
    ```
    # 进入安装包解压缩后目录  
    cd maxkb-v1.2.0-offline

    # 执行安装命令
    bash install.sh
    ```
    安装成功后，可通过浏览器访问 MaxKB：
    ```
    http://目标服务器 IP 地址:8080

    默认登录信息
    用户名：admin
    默认密码：MaxKB@123..
    ```



## 3 离线升级 
!!! Abstract ""
    与 **2 离线部署** 执行步骤一样. 

