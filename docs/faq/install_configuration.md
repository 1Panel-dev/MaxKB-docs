# 安装部署以及启动问题

## 1 安装 MaxKB 过程报错 docker-compose--X.XX.X 无法启动或者访问服务

!!! Abstract ""
    Docker 版本太老可能会导致安装失败，建议环境建议使用安装包内的 Docker。安装包所使用的 Docker 版本为 27.2.0、Compose 版本为 v2.29.2。

## 2 如何将内置的 pgsql 通过指定的主机端口提供对外访问？

!!! Abstract ""
    默认配置进行安装时，为了安全性，pgsql 容器只对宿主机提供 5432 的访问端口，其它地址都无法访问。

![pgsl默认访问规则](../img/FAQ/lcoal_pgsql.png)

!!! Abstract ""
    如果需要将 pgsql 暴露给其它服务器访问，可在 /opt/maxkb/.env 中配置，然后执行`mkctl reload`，重新加载配置即可。

![pgsl默认访问规则](../img/FAQ/expose_pgsql_config.png)

![pgsl默认访问规则](../img/FAQ/expose_pgsql.png)


## 3 升级过程提示 ModuleNotFoundError: No module named 'XXX'

!!! Abstract ""
    某些旧版本的依赖包与新版本不兼容，导致系统无法正常运行。进入依赖包的存储目录：
    执行以下命令，创建模型：
    ```
    cd /opt/maxkb/python-packages
    ```
    找到导致依赖冲突的包，通常通过查看错误日志来确定具体冲突的包名。完成依赖包的清理后，重启服务 `mkctl restart` 以确保更改生效。

## 4 PostgreSQL 超过最大客户端连接数，提示 too many clients already 的错误

!!! Abstract ""
    这表明当前配置的客户端连接数已达到上限，需要调整配置以允许更多的连接。进入 PostgreSQL 配置文件所在的目录：
    ```
    cd /opt/maxkb/data/postgresql/pgdata/
    ```
    在 postgresql.conf 文件中找到 max_connections 参数，将其值设置为所需的连接数。例如，将最大连接数设置为 200
    ```
    max_connections = 200
    ```
    停止当前运行的 MaxKB 服务，删除 PostgreSQL 容器：
    ```
    docker stop maxkb

    docker rm maxkb
    ```
    执行 `mkctl reload` 重新加载服务配置并启动服务。

## 5 迁移常见问题
### 5.1 无法执行 PowerShell 脚本
![无法执行powershell脚本](../img/FAQ/error1.png)
!!! Abstract ""
    如果无法执行 PowerShell 脚本，可能需要修改执行策略：

    - 临时修改（推荐）
    ```
    Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process       
    ```
    - 永久修改（需管理员权限）
    ```
    Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine     
    ```

### 5.2 执行脚本后出现乱码报错
![执行powershell脚本乱码](../img/FAQ/error2.png)
!!! Abstract ""
    用记事本打开文件，将文件另存为 ANSI 格式的文本。
![解决方法](../img/FAQ/solution1.png)
!!! Abstract ""
    重新执行 PowerShell 即可正常执行迁移命令。
![解决方法](../img/FAQ/solution2.png)

### 5.3 Docker Desktop 安装的 MaxKB 迁移后目录路径内容为空，但 MaxKB 能正常运行
!!! Abstract ""
    Docker Desktop 安装的 MaxKB 迁移后挂载路径内容为空，但 MaxKB 能正常运行。
![解决方法](../img/FAQ/Path missing.png)
!!! Abstract ""
    安装 MaxKB V2 时，容器数据的挂载目录为 /opt/maxkb，修改挂载目录即可。
    
    ```
    V1:/var/lib/postgresql/data
    V2:/opt/maxkb
    ```

![解决方法](../img/FAQ/solution3.png)