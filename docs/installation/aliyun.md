# 云市场部署指南

!!! Abstract ""

    本指南将介绍如何通过阿里云云市场购买、部署和使用 **MaxKB** 镜像，并提供购买服务器的优惠链接。

## 1 购买镜像

!!! Abstract ""

    - MaxKB 已经上架到阿里云云市场，您可以通过以下链接直接购买镜像：
    [MaxKB 云市场购买链接](https://market.aliyun.com/products/53690006/cmjj00067609.html?userCode=kmemb8jp)
    
    - 您也可以自行购买阿里云服务器，并在选择镜像时搜索 **MaxKB**，即可快速选择镜像进行部署。

    **注意：** 购买时请选择合适的实例规格，建议 4C/8G 及以上。

!!! Abstract "服务器优惠"

    如果您还没有服务器，可以通过以下优惠链接购买阿里云服务器：

    - [专属阿里云特价链接 5.5 折优惠](https://market.aliyun.com/common/dashi/maxkb?userCode=kmemb8jp)

## 2 启动服务

!!! Abstract ""

    镜像启动后，您可以通过浏览器访问以下地址登录 MaxKB：

    ```
    服务访问地址: http://服务器IP:8080
    默认用户名: admin
    默认密码: MaxKB@123..
    ```

    首次登录后，建议及时更改密码并进行其他安全设置。

## 3 开放端口

!!! Abstract ""

    - 为了确保外部能够正常访问 MaxKB 服务，您需要在阿里云服务器的安全组规则中开放 `8080` 端口。

    - 具体的开放步骤可以参考阿里云的 [端口放行教程](https://help.aliyun.com/document_detail/25471.html)。
