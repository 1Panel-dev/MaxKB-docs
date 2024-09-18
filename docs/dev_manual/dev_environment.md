# 开发环境搭建

## 1 项目结构

!!! Abstract "" 

    ```
    .          
    ├── LICENSE                 # License 申明        
    ├── README.md           
    ├── apps                    #  后端项目根目录        
    │ ├── common                # 项目公共资源目录         
    │ ├── smartdoc              # 项目主目录          
    │ ├── users                 # 用户相关          
    │ ├── manage.py             #  django项目入口         
    │ └── sdk                   # 项目通用的前后端依赖/网关的前端          
    ├── pyproject.toml          # 后端依赖 配置文件         
    └── ui                      # 前端项目根目录          
    ├── config_example.yml      # 项目配置示例             
    ├── main.py                 # 项目入口文件 python main.py start 启动项目             
    ```     

## 2 环境准备          

!!! Abstract "" 
    - **前端环境准备**       
      安装 [node](https://nodejs.org/)      
    - **后端环境准备**        
      安装 [python](https://www.python.org/downloads/release/python-3115/)        
      安装 [pycharm](https://www.jetbrains.com/pycharm/download/)

## 3 开发环境搭建

!!! Abstract "" 
    安装 poetry 包管理器
    ``` bash
    pip install poetry
    ```

## 4 本地配置

!!! Abstract "" 
      项目启动之前，需要准备配置文件及目录

      - 准备配置文件

      ```bash
      # 将config_example.yml配置文件 目录拷贝至 /opt/maxkb/conf目录下 如果是Windows D:\\opt\\maxkb\\conf
      cp config_example.yml /opt/maxkb/conf
      ```

      - 配置 /opt/maxkb/conf/config_example.yml 

      ```
      # 数据库配置 
      DB_NAME: maxkb
      DB_HOST: localhost
      DB_PORT: 5432
      DB_USER: root
      DB_PASSWORD: xxx
      DB_ENGINE: django.db.backends.postgresql_psycopg2
      
      # 模型相关配置
      # 模型路径:如果EMBEDDING_MODEL_NAME是绝对路径则无效,反之则会从https://huggingface.co/下载模型到当前目录
      EMBEDDING_MODEL_PATH: /opt/maxkb/model/
      # 模型名称:如果模型名称是路径,则会加载目录下的模型,如果是模型名称,则会在https://huggingface.co/下载模型 模型的下载位置为EMBEDDING_MODEL_PATH
      EMBEDDING_MODEL_NAME: /opt/maxkb/model/shibing624_text2vec-base-chinese
      ```

## 5 开发调试

### 5.1 启动前端项目

!!! Abstract "" 
      先在ui执行安装前端需要的依赖

      ```bash
      npm install
      ```

      启动项目
      ```bash
      npm run dev
      ```

### 5.2 启动后端项目

!!! Abstract "" 
      注意: 在项目根目录执行

      创建venv
      ```
      # win
      python -m venv venv

      # linux/mac
      python3 -m venv venv
      ```

      激活 venv
      ```
      # win  
      .\venv\Scripts\activate

      # linux/mac
      source venv/bin/activate
      ```

      安装后端需要的依赖

      ```
      poetry install
      ```

      启动项目

      ```
      python main.py start
      ```

## 6 常见问题

!!! Abstract "" 
      - 关于数据库版本
      ```
      postgresql:15.x
      ```
      - 关于 Python 版本
      ```
      python:3.11.x
      ```
      - database "maxkb" does not exist 

      数据库不存在需要创建一个与配置文件相同的数据库，默认名称为 maxkb。

      ```
      CREATE DATABASE "maxkb";
      \c "maxkb";
      CREATE EXTENSION "vector";
      ```