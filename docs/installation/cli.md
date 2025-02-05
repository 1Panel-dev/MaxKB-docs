## 1 mkctl 命令

!!! Abstract ""
    MaxKB 离线安装包默认内置了命令行运维工具 mkctl，通过执行 `mkctl help`，可以查看相关的命令说明。  

    **说明**：

    - 1.5.0 之前版本请使用 kbctl 命令。
    - 通过在线安装、1Panel方式安装，并没有内置 mkctl 命令。

    ```
    Usage:
    mkctl [COMMAND] [ARGS...]
    mkctl --help

    Commands: 
    status              查看 MaxKB 服务运行状态
    start               启动 MaxKB 服务
    stop                停止 MaxKB 服务
    restart             重启 MaxKB 服务
    reload              重新加载 MaxKB 服务
    uninstall           卸载 MaxKB 服务
    upgrade             升级 MaxKB 服务
    version             查看 MaxKB 版本信息
    clean-images        清理 MaxKB 旧版本的相关镜像
    ```
