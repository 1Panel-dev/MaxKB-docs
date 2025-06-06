# 安装部署以及启动问题

## 1 安装 MaxKB 过程报错 docker-compose--X.XX.X 无法启动或者访问服务

!!! Abstract ""
    Docker 版本太老可能会导致安装失败，建议环境建议使用安装包内的 Docker。安装包所使用的 Docker 版本为 27.2.0、Compose 版本为 v2.29.2。


## 2 离线部署提示 failed to cast to expected type: strconv.ParseInt: parsing "2G"

!!! Abstract ""
    在配置文件中内存设置格式存在问题。打开配置文件 docker-compose-pgsql.yml，找到 services.pgsql.mem_limit 的设置项。 将内存设置值从 "2G" 修改为小写的 "2g"，执行 mkctl reload 命令重新加载配置。

## 3 升级过程提示 ModuleNotFoundError: No module named 'XXX'

!!! Abstract ""
    某些旧版本的依赖包与新版本不兼容，导致系统无法正常运行。进入依赖包的存储目录：
    执行以下命令，创建模型：
    ```
    cd /opt/maxkb/python-packages
    ```
    找到导致依赖冲突的包，通常通过查看错误日志来确定具体冲突的包名。完成依赖包的清理后，重启服务 mkctl restart 以确保更改生效。

## 4 PostgreSQL 超过最大客户端连接数,提示 too many clients already 的错误

!!! Abstract ""
    这表明当前配置的客户端连接数已达到上限，需要调整配置以允许更多的连接。进入 PostgreSQL 配置文件所在的目录：
    ```
    cd /opt/maxkb/data
    ```
    找到 postgresql.conf 文件中找到 max_connections 参数，将其值设置为所需的连接数。例如，将最大连接数设置为 200
    ```
    max_connections = 200
    ```
    停止当前运行的 MaxKB 服务，删除 PostgreSQL 容器，：
    ```
    docker stop maxkb

    docker rm maxkb
    ```
    执行 mkctl reload 重新加载服务配置并启动服务。
