
## 1 环境要求

!!! Abstract ""
    **安装前请确保您的系统符合安装条件：**

    * 操作系统：Ubuntu 22.04 / CentOS 7.6 64 位系统；
    * CPU/内存： 2C/4GB 以上；
    * 磁盘空间：100GB。

    生产环境推荐使用离线部署。


## 2 安装部署 

!!! Abstract ""
    打开社区网站下载 MaxKB 离线包
    [社区版离线包](https://community.fit2cloud.com/#/products/maxkb/downloads) (社区版本仅提供 x86架构安装包，如需 arm 架构安装包，可以[申请专业版](https://jsj.top/f/wQsdOJ))。

    上传至服务器后执行以下命令进行解压缩：
    ```
    # maxkb-v1.2.0-offline.tar.gz替换成下载包的名字  
    tar -zxvf maxkb-v1.2.0-offline.tar.gz
    ```
    解压完成后，执行以下命令进行安装：
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

