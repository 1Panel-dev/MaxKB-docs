## 1 Deployment Requirements

### 1.1 Server Configuration

!!! Abstract ""

    **Server Requirements:**

    * Operating System: Ubuntu 22.04 / CentOS 7.6 64-bit system
    * CPU/Memory: 4 cores/8GB or higher
    * Disk Space: 100GB

### 1.2 Port Requirements

!!! Abstract ""

    The following ports need to be accessible for deployment:

| Port    | Purpose   | Description                                                |
|---------|:----------|:----------------------------------------------------------|
| 22      | SSH       | Used for installation, upgrades and management            |
| 8080    | Web Port  | Default web service access port, can be changed as needed |


## 2 Quick Online Deployment

!!! Abstract ""

    MaxKB supports one-click startup, just execute the following command:
    ```
    # For Linux
    docker run -d --name=maxkb --restart=always -p 8080:8080 -v ~/.maxkb:/var/lib/postgresql/data -v ~/.python-packages:/opt/maxkb/app/sandbox/python-packages cr2.fit2cloud.com/1panel/maxkb

    # For  Windows
    docker run -d --name=maxkb --restart=always -p 8080:8080 -v C:/maxkb:/var/lib/postgresql/data -v C:/python-packages:/opt/maxkb/app/sandbox/python-packages cr2.fit2cloud.com/1panel/maxkb
    ```
     
    Once all container statuses show as `healthy`, you can access MaxKB through a browser:
    ```
    http://IP:8080

    Default login credentials:
    Username: admin
    Password: MaxKB@123..
    ```

## 3 Online Upgrade

!!! Abstract ""

    Follow these steps to upgrade:

    (1) Download the latest image
    ```
    docker pull cr2.fit2cloud.com/1panel/maxkb
    ```
    (2) Check and confirm the previous data persistence directory, copy and save it for use in step (4)
    ```
    docker inspect maxkb
    ```

![Get pgsql directory](../img/index/mount_pgsqldir.png)

!!! Abstract ""

    (3) Remove the old running  version of MaxKB container

    ```
    docker rm -f maxkb 
    ```

    (4) Start and run the new version of MaxKB container

    **Note:** Make sure to confirm that the data persistence directory (the directory after -v in the command line) matches the directory viewed in step (2), otherwise the entire system data will be empty after startup.

    ```
    docker run -d --name=maxkb -p 8080:8080 -v /opt/maxkb/pgsql/data:/var/lib/postgresql/data -v /opt/maxkb/python-packages:/opt/maxkb/app/sandbox/python-packages cr2.fit2cloud.com/1panel/maxkb
    ```
