# DevOps CI/CD Pipeline

This project demonstrates a simple DevOps workflow implementing a Continuous Integration (CI) pipeline using **GitHub Actions**, **Python tests**, and **Docker containerization**.

The objective of this project is to show how code can be automatically tested and built every time a change is pushed to the repository.

---

# Technologies

- Python
- Pytest
- Docker
- GitHub Actions
- Git

---

# Project Structure

devops-ci-cd-pipeline  
│  
├── app/  
│   └── app.py  
│  
├── tests/  
│   └── test_app.py  
│  
├── .github/workflows/  
│   └── pipeline.yml  
│  
├── Dockerfile  
├── requirements.txt  
├── pytest.ini  
└── README.md  

### Description

- **app/** → contains the Python application  
- **tests/** → automated tests executed with pytest  
- **.github/workflows/** → GitHub Actions CI pipeline  
- **Dockerfile** → containerizes the application  
- **requirements.txt** → Python dependencies  
- **pytest.ini** → pytest configuration  

---

# How the CI Pipeline Works

Each time code is pushed to the `main` branch, GitHub Actions automatically:

1. Checks out the repository  
2. Sets up Python  
3. Installs project dependencies  
4. Runs automated tests with pytest  
5. Builds the Docker image  

Pipeline flow:

git push  
↓  
GitHub Actions  
↓  
Install dependencies  
↓  
Run tests  
↓  
Build Docker image  

This ensures that every change in the repository is automatically validated.

---

# Running the Project Locally

### Install dependencies

pip install -r requirements.txt

### Run tests

pytest

### Run the application

python app/app.py

Expected output:

Result: 5

---

# Docker

Build the Docker image:

docker build -t devops-ci-cd-pipeline .

Run the container:

docker run devops-ci-cd-pipeline

---

# Learning Objectives

This project demonstrates:

- Continuous Integration (CI)
- Automated testing
- Docker containerization
- DevOps workflow automation
- Infrastructure reproducibility

---

# Possible Improvements

Future improvements could include:

- pushing the Docker image to a container registry
- adding deployment automation
- integrating Kubernetes
- implementing monitoring