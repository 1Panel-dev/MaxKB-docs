# Quick Start

## Installing MaxKB

!!! info "Prerequisites"
    Before installing MaxKB, make sure your machine meets the following minimum system requirements:

    - CPU >= 4 Cores
    - RAM >= 8 GiB
    - Disk Space >= 100 GiB

    And ensure Docker is installed ([install Docker](https://docs.docker.com/get-started/get-docker/)).

Execute the script below to start a MaxKB container using Docker:

```bash
docker run -d --name=maxkb --restart=always -p 8080:8080 -v ~/.maxkb:/var/lib/postgresql/data -v ~/.python-packages:/opt/maxkb/app/sandbox/python-packages 1panel/maxkb
```

Access MaxKB web interface at `http://your_server_ip:8080` with default admin credentials:

- username: admin
- password: MaxKB@123..

Change the default password after logging in.

## Main Steps to Use MaxKB

The MaxKB operation process can be broadly categorized into four stages:

1. Adding models.
2. Creating knowledge bases.
3. Creating applications.
4. Publishing applications.

!!! info "Note"
    You can use custom functions for advanced orchestration applications, including data processing, logical judgment, information extraction, and more, providing enhanced capabilities and flexibility.

Now, let's swiftly build and release a smart Q&A app. We'll use ChatGPT from OpenAI and a general knowledge base as an example.
