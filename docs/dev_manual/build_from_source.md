# Building from Source

## Source Code Structure

```txt
.          
├── LICENSE                #  declaration        
├── README.md           
├── apps                   # Backend project root directory        
│ ├── application          # Applications
│ ├── common               # Project common resources directory
│ ├── dataset              # Knowledge base
│ ├── embedding            # Vectorization
│ ├── function_lib         # Function library
│ ├── ops                  # 
│ ├── setting             # Settings
│ ├── smartdoc             # Project main directory          
│ ├── users                # User related          
│ └── manage.py            # Django project entry point
├── installer              # Installation related  
├── pyproject.toml         # Backend dependency configuration file         
└── ui                     # Frontend project root directory          
├── config_example.yml     # Project configuration example             
├── main.py                # Project entry file              
```

## Setting Up the Development Environment

### Environment Preparation

- **Frontend**
  - Install [node](https://nodejs.org/), v16 or above
- **Backend**
  - Install [python](https://www.python.org/downloads/release/python-3115/), version v3.11.x  
  - Install [pycharm](https://www.jetbrains.com/pycharm/download/)
- **Database**
  - Install [PostgreSql](https://www.postgresql.org/), version v15.x

### Initial Configuration

#### Create Database

Manually create a database named `maxkb` in PostgreSql for the MaxKB project.

```SQL
# Create database
CREATE DATABASE "maxkb"; 
# Switch to database
\c "maxkb"; 
# Create vector extension
CREATE EXTENSION "vector";
```

#### Configuration File

Before starting the project, configuration files and directories need to be prepared.

- Prepare configuration file

```bash
# Copy config_example.yml configuration file to /opt/maxkb/conf directory
cp config_example.yml /opt/maxkb/conf
```

- Configure /opt/maxkb/conf/config_example.yml.

```yaml
# Database configuration 
DB_NAME: maxkb
DB_HOST: localhost
DB_PORT: 5432
DB_USER: root
DB_PASSWORD: xxx
DB_ENGINE: django.db.backends.postgresql_psycopg2

# Model related configuration
EMBEDDING_MODEL_PATH: /opt/maxkb/model/
EMBEDDING_MODEL_NAME: /opt/maxkb/model/shibing624_text2vec-base-chinese
```

## Development and Debugging

### Running the Frontend

!!! note "Note"
    All commands below should be executed in the `ui` directory of the MaxKB project.

```bash
# Install dependencies
npm install

# Start the project
npm run dev
```

### Running the Backend

For the backend system, you need to start the web service, local model service, and asynchronous task queue service.

!!! note "Note"
    All commands below should be executed in the root directory of the MaxKB project.

#### Web Service

```bash
# Install poetry package manager
pip install poetry

# Install backend dependencies
poetry install

# Start project
python main.py start
```

#### Local Model Service

```bash
# Start project
python main.py dev local_model
```

#### Asynchronous Task Service

```bash
# Start project
python main.py dev celery
```

## Accessing MaxKB via Browser

Once both the frontend and backend are successfully started, you can access MaxKB through the frontend route (the access address is displayed when the frontend starts) in your browser.
