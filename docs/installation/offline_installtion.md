## 1 Deployment Requirements

!!! Abstract ""
    For production environments, offline installation is the officially recommended.

### 1.1 Server Configuration

!!! Abstract ""

    **Server Requirements:**

    * Operating System: Ubuntu 22.04 / CentOS 7.6 64-bit system
    * CPU/Memory: 4 cores/8GB or higher
    * Disk Space: 100GB

### 1.2 Port Requirements

!!! Abstract ""
    The following ports should be accessible:

| Port    | Purpose   | Description                                                |
|---------|:----------|:----------------------------------------------------------|
| 22      | SSH       | Used for installation, upgrades and management            |
| 8080    | Web Port  | Default web service access port, can be changed as needed |

## 2 Download Installation Package

!!! Abstract ""
    Open the [FIT2CLOUD Open Source Community MaxKB Community Edition Downloads](https://community.fit2cloud.com/#/products/maxkb/downloads) page to download the latest version installation package and upload it to the deployment server (using v1.2.0 as an example).

## 3 Installation and Deployment

### 3.1 Extract Installation Package

!!! Abstract ""

    Log in to the deployment server as root user via SSH protocol and extract the installation package:
    ```
    tar -zxvf maxkb-v1.2.0-offline.tar.gz
    ```

### 3.2 Installation Configuration (Optional)

!!! Abstract ""

    MaxKB installation directory, service running port, database configuration and other parameter can be configured in the install.conf file within the installation package.

    ```
    ## Installation directory
    MAXKB_BASE=/opt
    ## Service port
    MAXKB_PORT=8080
    ## Docker subnet settings
    MAXKB_DOCKER_SUBNET=172.19.0.0/16
    # Database configuration
    ## Whether to use external database
    MAXKB_EXTERNAL_PGSQL=false
    ## Database host
    MAXKB_PGSQL_HOST=pgsql
    ## Database port
    MAXKB_PGSQL_PORT=5432
    ## Database name
    MAXKB_PGSQL_DB=maxkb
    ## Database username
    MAXKB_PGSQL_USER=root
    ## Database password
    MAXKB_PGSQL_PASSWORD=Password123@postgres
    ```

    **Note**: Parameters can be modified in the install.conf file before first installation, and the installation will be executed according to the modified parameters. If you need to modify configuration parameters after installation is complete, you need to make changes in the ${MAXKB_BASE}/maxkb/.env file and execute the `mkctl reload` command to reload the configuration file.

### 3.3 Execute Installation Script

!!! Abstract ""

    ```
    # Enter the extracted installation package directory
    cd maxkb-v1.2.0-offline

    # Execute installation Script
    bash install.sh
    ```

![Installation](../img/index/install.jpg)

## 4 Login Access

!!! Abstract ""

    Once all container statuses show as `healthy`, you can access the address `http://IP:8080` through a browser and log in to MaxKB using the default administrator credentials.

    ```
    Username: admin
    Password: MaxKB@123..
    ```

![Login](../img/index/login.jpg)

## 5 Offline Upgrade

!!! Abstract ""

    Following the above instructions, download and upload the new version installation package, extract and execute the installation command again to upgrade.

    ```
    # Enter new version directory
    cd maxkb-v1.x.x-offline

    # Run installation script
    /bin/bash install.sh

    # Check MaxKB running status
    mkctl status
    ```

    **Note:** Please backup the database before upgrading.
