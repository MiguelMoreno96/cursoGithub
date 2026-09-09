# File Analysis API with FastAPI

![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Python](https://img.shields.io/badge/Python-3.9+-blue?style=for-the-badge&logo=python)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker)

API for file processing and analysis integrated with VirusTotal and other services.

## Project Structure.

the proposed structure of the project was planned in this way due to its scalability and organization: 
1. leaving the drivers folder where the endpoint will remain.
2. The models folder is to organize request response structures (respect for our own services or external services) and database model.
3. utils is being considered for consultations with services external to projects.

```
    api_py/
    ├── main.py
    ├── src/
    │ ├── controllers/ 
    │ │ └── Fileprocess.py
    │ ├── models/ 
    │ │ └── fileschema.py
    │ └── utils/ 
    │ └── api.py 
    ├── Dockerfile 
    ├── docker-compose.yml
    ├── requirements.txt 
    └── .env.example 
```

## Requirements 

- Python 3.9+
- Docker 20.10+
- Docker Compose 2.0+

##  Initial Configuration . 

1. Clone repository: 
   ```bash
   git clone https://github.com/MiguelMoreno96/file_Malware_Scanner_With_FastAPI.git
   cd file_Malware_Scanner_With_FastAPI

2. cp .env.example .env

# Edit .env with your credentials

# Execution in local environment

1. generate the virtual environment
    ```bash
    python -m venv [folder_name] 

    uvicorn src.main:app --reload --port 5030
# Execution in Docker environment 

1. Running with Docker
    ```bash
    docker-compose up --build

    docker-compose logs -f


