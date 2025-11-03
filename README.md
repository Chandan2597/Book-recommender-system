# End-to-End-Book-Recommender-System

## Workflow

- config.yaml
- entity
- config/configuration.py
- components
- pipeline
- main.py
- app.py


# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/chandan2597/End-to-End-Book-Recommender-System.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n books python=3.7.10 -y
```

```bash
conda activate books
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


Now run,
```bash
streamlit run app.py
```


# Streamlit app Docker Image Deployment

## 1. Login with your AWS console and launch an EC2 instance
## 2. Run the following commands

Note: Do the port mapping to this port:- 8501

```bash
sudo apt-get update -y

sudo apt-get upgrade

#Install Docker

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

```bash
git clone "your-project"
```

```bash
docker build -t chandan2597/bookapp:latest . 
```

```bash
docker images -a  
```

```bash
docker run -d -p 8501:8501 chandan2597/bookapp 
```

```bash
docker ps  
```
### To stop docker container

```bash
docker stop container_id
```

### To remove docker container

```bash
docker rm $(docker ps -a -q)
```

### Push docker image to docker hub 

```bash
docker login 
``

```bash
docker push chandan2597/bookapp:latest 
```

### Remove docker image

```bash
docker rmi chandan2597/bookapp:latest
```

### Pull docker image

```bash
docker pull chandan2597/bookapp