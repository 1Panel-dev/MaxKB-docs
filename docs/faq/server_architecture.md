## 1 s390x 架构

### 安装 MySQL

!!! Abstract ""
    **由于 MySQL 官方未提供 s390x 架构镜像，所以在应用商店启用 MySQL 前，需要手动修改 MySQL 镜像版本**

!!! Abstract "MySQL 5.7"

    - 1、下载 s390x 架构最新版本镜像

    ```shell
    docker pull ibmcom/mysql-s390x:5.7.34
    ```

    - 2、将镜像重命名为 1Panel 应用商店中使用的 MySQL 版本
    
    ```shell
    docker tag ibmcom/mysql-s390x:5.7.34 mysql:5.7.42
    ```

    - 3、在应用商店中安装 MySQL，版本选择 5.7.42

!!! Abstract "MySQL 8.0"

    - 1、下载 s390x 架构最新版本镜像

    ```shell
    docker pull ibmcom/mysql-s390x:8.0.25
    ```

    - 2、将镜像重命名为 1Panel 应用商店中使用的 MySQL 版本
    
    ```shell
    docker tag ibmcom/mysql-s390x:8.0.25 mysql:8.0.33
    ```

    - 3、在应用商店中安装 MySQL，版本选择 8.0.33

## 2 armv7l 架构

### 安装 MySQL

!!! Abstract ""
    **由于 MySQL 官方未提供 armv7l 架构镜像，所以在应用商店启用 MySQL 前，需要手动修改 MySQL 镜像版本**

!!! Abstract "MySQL 5.7"

    - 1、下载 armv7l 架构最新版本镜像

    ```shell
    docker pull biarms/mysql:5.7.33-beta-circleci
    ```

    - 2、将镜像重命名为 1Panel 应用商店中使用的 MySQL 版本
    
    ```shell
    docker tag biarms/mysql:5.7.33-beta-circleci mysql:5.7.42
    ```

    - 3、在应用商店中安装 MySQL，版本选择 5.7.42

!!! Abstract "MySQL 8.0"

    **1Panel 当前版本还不支持在 armv7l 架构服务器上安装 MySQL 8.0**

### 安装 OpenResty

!!! Abstract ""
    **由于 OpenResty 官方未提供 armv7l 架构镜像，所以在应用商店启用 OpenResty 前，需要手动修改 OpenResty 镜像版本**

!!! Abstract ""

    - 1、下载 armv7l 架构最新版本镜像

    ```shell
    docker pull imzcc/openresty:1.21.4.1-7-alpine
    ```

    - 2、将镜像重命名为 1Panel 应用商店中使用的 OpenResty 版本
    
    ```shell
    docker tag imzcc/openresty:1.21.4.1-7-alpine openresty/openresty:1.21.4.1-7-focal
    ```

    - 3、在应用商店中安装 OpenResty
