## 1 1Panel 和宝塔有什么区别？

!!! Abstract ""
    **宝塔是一款被广泛使用的 Linux 面板。与宝塔 Linux 面板相比，1Panel 的特色是开源和现代化。**  

    - 开源：1Panel 强调开源开放，广泛获取社区使用反馈，并快速迭代。
    - 现代化：一方面，1Panel 采纳最新的前端技术，并通过精心设计的 UX 交互，为用户提供更好的用户使用体验；另一方面，1Panel 采用主流的容器技术，让 Linux 服务器的运维管理更简单、更安全。

## 2 是否考虑增加多主机管理？

!!! Abstract ""
    **1Panel 会关注在单机 Linux 的运维管理。**  

    多主机管理推荐使用 [JumpServer 堡垒机](jumpserver) 来实现。尤其现在 JumpServer 也支持 Web 资产，可以通过Web 可视化连上 1Panel，实现多主机管理。

[jumpserver]:https://github.com/jumpserver/jumpserver

## 3 1Panel 安装包多大？运行时占用系统资源多吗？会影响其他应用吗？

!!! Abstract ""

    - 1Panel 基于 Golang 语言编写，可执行文件大小约 40MB、运行时占用系系统内存约 150MB。
    - 1Panel 基于 Docker 来部署管理其他应用，对系统的侵入影响非常小。

[jumpserver]:https://github.com/jumpserver/jumpserver
