# Development Environment Setup

## 1 Project Structure

!!! Abstract "" 

    ```
    .          
    ├── LICENSE                 #  declaration        
    ├── README.md           
    ├── apps                    # Backend project root directory        
    │ ├── application           # Applications
    │ ├── common                # Project common resources directory
    │ ├── dataset              # Knowledge base
    │ ├── embedding            # Vectorization
    │ ├── function_lib         # Function library
    │ ├── ops                  # 
    │ ├── settting             # Settings
    │ ├── smartdoc             # Project main directory          
    │ ├── users                # User related          
    │ └── manage.py            # Django project entry         
    ├── installer              # Installation related  
    ├── pyproject.toml         # Backend dependency configuration file         
    └── ui                     # Frontend project root directory          
    ├── config_example.yml     # Project configuration example             
    ├── main.py                # Project entry file              
    ```     

## 2 Environment Preparation          

!!! Abstract "" 
    - **Frontend Environment Preparation**       
      Install [node](https://nodejs.org/), v16 or above     
    - **Backend Environment Preparation**        
      Install [python](https://www.python.org/downloads/release/python-3115/), version v3.11.x  
      Install [pycharm](https://www.jetbrains.com/pycharm/download/)
    - **Database**   
      Install [PostgreSql](https://www.postgresql.org/), version v15.x

## 3 Configuration

### 3.1 Create Database

!!! Abstract "" 
    Manually create MaxKB application database named `maxkb` in PostgreSql.
    ```
    # Create database
    CREATE DATABASE "maxkb"; 
    # Switch to database
    \c "maxkb"; 
    # Create vector extension
    CREATE EXTENSION "vector";
    ```

### 3.2 Configuration File

!!! Abstract "" 
      Before starting the project, configuration files and directories need to be prepared

      - Prepare configuration file

      ```bash
      # Copy config_example.yml configuration file to /opt/maxkb/conf directory
      cp config_example.yml /opt/maxkb/conf
      ```

      - Configure /opt/maxkb/conf/config_example.yml 

      ```
      # Database configuration 
      DB_NAME: maxkb
      DB_HOST: localhost
      DB_PORT: 5432
      DB_USER: root
      DB_PASSWORD: xxx
      DB_ENGINE: django.db.backends.postgresql_psycopg2
      
      # Model related configuration
      # Model path: If EMBEDDING_MODEL_NAME is an absolute path then invalid, otherwise will download model from https://huggingface.co/ to current directory
      EMBEDDING_MODEL_PATH: /opt/maxkb/model/
      # Model name: If model name is a path, will load model from directory, if it's a model name, will download model from https://huggingface.co/. Download location is EMBEDDING_MODEL_PATH
      EMBEDDING_MODEL_NAME: /opt/maxkb/model/shibing624_text2vec-base-chinese
      ```

## 4 Development and Debugging

### 4.1 Start Frontend

!!! Abstract "" 

    ```bash
    # Execute in `ui` directory to install frontend dependencies
    npm install
    
    # Then start the project
    npm run dev
    ```

    After successful startup, it will display as shown below.

![Start Frontend](../img/dev/npm_run.png){width="500px"}


### 4.2 Start Backend

!!! Abstract "" 
    For the backend system, you need to start the web service, local model service, and asynchronous task queue service.
    Note: Execute in project root directory

!!! Abstract ""
    Execute the following commands in sequence under the MaxKB project root directory to start the Web service.

    ```
    # Install poetry package manager
    pip install poetry
    
    # Install backend dependencies
    poetry install
    
    # Start project
    python main.py start
    ```

![Start Web Service](../img/dev/main_start.png){width="500px"}

!!! Abstract ""
    Execute the following commands in sequence under the MaxKB project root directory to start the local model service.

    ```
    # Start project
    python main.py dev local_model
    ```

![Start Local Model Service](../img/dev/main_localmodel.png){width="500px"}

!!! Abstract ""
    Execute the following commands in sequence under the MaxKB project root directory to start the asynchronous task service.

    ```
    # Start project
    python main.py dev celery
    ```

![Start Async Task Service](../img/dev/main_celery.png){width="500px"}

## 5 Access Project

!!! Abstract ""
    After both frontend and backend are successfully started, you can access through the frontend route (access address shown when frontend starts) in the browser.

![Browser Access](../img/dev/maxkb_running.png)
