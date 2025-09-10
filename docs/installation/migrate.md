# 迁移工具

## 1 迁移路线 
!!! Abstract ""
    **注意：v1 版本需先升级至 v1.10.10-lts，再使用迁移工具迁移到 v2.1.0，之后可升级到更高版本。**
![migrate](../img/index/migrate_route.png)

## 2 注意事项
!!! Abstract ""

    - **此工具是迁移工具，用以迁移 v1 的数据到 v2，并不是升级工具；**
    - **此工具只支持 v1.10.10-lts 的数据迁移到 v2.1.0；**
    - **迁移前，请务必检查磁盘空间是否足够，确保导出的数据不会超出磁盘存储空间；**
    - **v2.1.0 的环境必须是空环境。**

## 3 迁移工具包下载
!!! Abstract ""
    打开[MaxKB 迁移工具下载](https://github.com/1Panel-dev/MaxKB-v1-to-v2-migrator)页面，下载最新版本工具包，并上传至部署服务器。


## 4 迁移操作
### 4.1 Linux/macOS 系统
#### 4.1.1 导出数据
!!! Abstract ""
    在 v1 机器上下载 MaxKB-v1-to-v2-migrator-<version\>.zip，解压后进入目录，执行命令导出 v1 数据。

    - **由于数据量的原因，导出过程中需要一定的时间。** 
    - 导出完成后，MaxKB-v1-to-v2-migrator-<version\> 中会生成一个migrate.zip。
    - 将 MaxKB-v1-to-v2-migrator-<version\> 复制到 v2 所在的机器上。
    ```
    unzip MaxKB-v1-to-v2-migrator-<version>.zip 

    cd  MaxKB-v1-to-v2-migrator-<version>

    bash export_v1_data.sh <v1_container_name>
    ```

#### 4.1.2 导入数据
!!! Abstract ""
    在 v2 机器上，确保 v2.1.0 版本的容器已经启动且为空环境, 专业版和企业版需要在启动后手动导入 license，进入迁移工具目录，执行命令将数据导入 v2。
    ```
    cd MaxKB-v1-to-v2-migrator-<version>

    bash import_v2_data.sh <v2_container_name>
    
    ```
    ![导入linux](../img/index/migrate_linux_import.png)
    ![导入linux](../img/index/migrate_linux_import1.png)
    **提示：** 导入成功后，需重启容器。

### 4.2 Windows 系统
#### 4.2.1 操作要求
!!! Abstract ""
    支持的操作系统：

    - Windows 10
    - Windows 11
    - Windows Server 2016 及以上版本

!!! Abstract ""
    前置条件：

    - 已安装 Docker Desktop for Windows；
    - MaxKB v1 和 v2 容器正在运行；
    - 对于 PowerShell 脚本，需要 PowerShell 5.0 或更高版本。


#### 4.2.2 导出数据
!!! Abstract ""
    对于 Windows 系统，MaxKB 提供了 PowerShell 脚本(.ps1)来导出 v1 数据。下载迁移工具并解压，使用终端管理员进入迁移目录，执行命令导出 v1 数据。
    
    - **由于数据量的原因，导出过程中需要一定的时间。** 
    - 导出完成后，MaxKB-v1-to-v2-migrator-<version\> 中会生成一个migrate.zip。
    ```
    # PowerShell 版本
    .\export_v1_data.ps1 -ContainerName <v1_container_name>
    ```
    ![导出windows](../img/index/migrate_windows_export.png)

#### 4.2.3 导入数据
!!! Abstract ""
    确保 v2.1.0 版本的容器已经启动且为空环境, 使用终端管理员进入迁移工具目录，执行命令将数据导入 v2。
    ```
    #PowerShell 版本
    .\import_v2_data.ps1 -ContainerName <v2_container_name>
    ```
    ![导出windows](../img/index/migrate_windows_import.png)

#### 4.2.4 注意事项
!!! Abstract ""

    1. 确保在包含迁移工具的目录中运行脚本
    2. 导入前确保已成功导出数据（migrate.zip 文件存在）
     3. 导入完成后建议重启 v2 容器
     4. 备份重要数据，以防迁移过程中出现问题

#### 4.2.5 Windows 迁移常见问题
!!! Abstract ""
    
    1. 容器未运行
        - 使用 `docker ps` 检查容器状态。
    2. 权限不足
        - 确保 Docker Desktop 正在运行
        - 以管理员身份运行终端
        - 使用完整路径运行脚本
    3. 文件路径问题
        - 确保在包含迁移工具的目录中运行脚本
        - 检查 migrate.zip 文件是否存在


## 5 迁移说明
### 5.1 用户
!!! Abstract ""

    - admin 账户默认授予系统管理员、工作空间管理员、普通用户权限（X-Pack)；
    - 除 admin 外，系统用户或其他用户类型迁移后，默认角色为普通用户（X-Pack);
    - 用户的【姓名】为空，迁移后，自动将【用户名】作为【姓名】；
    - 工作空间内的资源查询依照【姓名】查询。

### 5.2 资源
!!! Abstract ""

    - v1 授权给其他成员的应用/知识库，迁移后授予相应的权限；
    - 资源创建者拥有管理资源的权限；
    - v1 函数库迁移后，在工具中，创建者有管理权限，其他用户默认都是不授权状态；
    - 公有模型迁移后，默认资源授权所有普通用户为查看权限，创建者为管理权限。


### 5.3 回调地址与接口
!!! Abstract ""

    - 回调地址发生变化，应用接入、登录认证（扫码登录）需重新配置（X-Pack)；
    - v1 与 v2 的接口文档不一致，如有接口调用，需重新配置。