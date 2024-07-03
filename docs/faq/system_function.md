## 1 使用自建 Nginx 反向代理 1Panel，导致主机和容器终端均不能正常使用。

!!! Abstract ""
    **需要在 Nginx 配置文件中增加以下配置：**

    ```properties
    location / {
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
    }
    ```

> **或者直接在 1Panel 系统中新建反向代理网站也可以实现上述功能**
