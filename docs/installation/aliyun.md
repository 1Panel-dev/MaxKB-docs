# Alibaba Cloud Marketplace Deployment Guide

!!! Abstract ""

    This guide will explain how to purchase, deploy and use MaxKB images through Alibaba Cloud Marketplace, and provide discounted links for purchasing servers.

## 1 Purchase Image

!!! Abstract ""

    - MaxKB is available on Alibaba Cloud Marketplace. You can purchase the image directly through this link:
    [MaxKB Cloud Marketplace Purchase Link](https://market.aliyun.com/products/53690006/cmjj00067609.html?userCode=kmemb8jp)
    
    - You can also purchase an Alibaba Cloud server separately and search for **MaxKB** when selecting an image for quick deployment.

    **Note:** Please select an appropriate instance specification when purchasing, recommended 4 cores/8GB RAM or higher.

!!! Abstract "Server Discounts"

    If you don't have a server yet, you can purchase Alibaba Cloud servers through this discount link:

    - [Exclusive Alibaba Cloud Special Price Link - 45% Off](https://market.aliyun.com/common/dashi/maxkb?userCode=kmemb8jp)

## 2 Start Service

!!! Abstract ""

    After the image starts, you can access MaxKB through your browser at:

    ```
    Service Access Address: http://SERVER-IP:8080
    Default Username: admin
    Default Password: MaxKB@123..
    ```

    After first login, it is recommended to change the password immediately and configure other security settings.

## 3 Open Ports

!!! Abstract ""

    - To ensure external access to MaxKB services, you need to open port `8080` in your Alibaba Cloud server's security group rules.

    - For detailed steps on opening ports, please refer to Alibaba Cloud's [Port Opening Tutorial](https://help.aliyun.com/document_detail/25471.html).
