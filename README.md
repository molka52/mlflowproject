## MLFLOW project

MLFLOW_TRACKING_URI=https://dagshub.com/molkabizid3/mlflowproject.mlflow \
MLFLOW_TRACKING_USERNAME=molkabizid3 \
MLFLOW_TRACKING_PASSWORD=ff7af3c8a4faa3be7b102d4e4c9c03b145a58804 \
python script.py

## README

# Environment Setup Guide

This README walks you through setting up a full development environment for MLOps / Data workflows across Windows.

## 1. Install Anaconda (Python Distribution)

Download Anaconda:
[https://www.anaconda.com/products/distribution](https://www.anaconda.com/products/distribution)

**Windows:** `.exe` installer

Launch Jupyter Notebook:

* **Windows:** via *Anaconda Prompt* → `jupyter notebook`

---

## 2. Create a Conda Environment

```bash
conda create -n mlops python=3.10.9
conda activate mlops
```

---

## 3. Install Project Dependencies

Make sure you’re in the activated environment, then:

```bash
pip install -r requirements.txt
```

---

## 4. Install Git

Download Git:
[https://git-scm.com/downloads](https://git-scm.com/downloads)

**Windows:** `.exe` installer
---

## 5. Create a DagsHub Account

DagsHub is used for dataset and model versioning:

[https://dagshub.com/](https://dagshub.com/)

---

## 6. Install Visual Studio Code (VSCode)

Download:
[https://code.visualstudio.com/download](https://code.visualstudio.com/download)

### Recommended Extensions

* **Python**
* **Jupyter**
* **Docker**

### Select Python Interpreter

In VSCode:

```
Ctrl + Shift + P → "Python: Select Interpreter"
```

---

## 7. Install Postman

Download:
[https://www.postman.com/downloads/](https://www.postman.com/downloads/)

---

## 8. Install Docker Desktop

Official downloads:
[https://docs.docker.com/](https://docs.docker.com/)

**Windows:** `.exe`

### Ubuntu – Install Docker Engine first

```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Verify installation:

```bash
sudo docker run hello-world
```

### Start Docker Desktop + run test container

```bash
docker run -d -p 80:80 docker/getting-started
```

