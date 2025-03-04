# Data-Science-wine-quality
This project is an end-to-end Machine Learning tutorial that predicts wine quality using the Wine Quality dataset available on kaggle. Built with Python, it follows a modular workflow, trains a model, and includes a web app deployed via AWS with CI/CD integration using GitHub Actions. The deployment was recorded and later decommissioned to avoid costs as i am just a student. This repo preserves the code, structure, and deployment process for learning purposes.

## Project Highlights
- **Dataset**: Wine Quality dataset which i got from kaggle.
- **Goal**: Predict wine quality using supervised learning.
- **Tools**: Python 3.8, scikit-learn, Flask (for `app.py`), Docker, AWS (EC2, ECR), GitHub Actions.
- **Outcome**: A trained ML model, a functional web app, and a recorded demo of the AWS deployment.
- **Status**: AWS deployment decommissioned to avoid further costs.

# How to run?
# STEPS:

- Clone the repository
https:https://github.com/iamshubhp/DS-wine-quality.git

# STEP 01- Create a conda environment after opening the repository
conda create -n mlproj python=3.8 -y
conda activate mlproj

# STEP 02- install the requirements
pip install -r requirements.txt
python app.py

# AWS-CICD-Deployment-with-Github-Actions
1. Login to AWS console.
2. Create IAM user for deployment

# with specific access
1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


# Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

# Policy:
1. AmazonEC2ContainerRegistryFullAccess
2. AmazonEC2FullAccess
3. Create ECR repo to store/save docker image
- Save the URI
4. Create EC2 machine (Ubuntu)
5. Open EC2 and Install docker in EC2 Machine:

#optinal
sudo apt-get update -y
sudo apt-get upgrade

#required
- curl -fsSL https://get.docker.com -o get-docker.sh
- sudo sh get-docker.sh
- sudo usermod -aG docker ubuntu
- newgrp docker

6. Configure EC2 as self-hosted runner:
setting>actions>runner>new self hosted runner> choose os> then run command one by one

7. Setup github secrets:
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = ca-central-1 / or any region you are working from /

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = simple-app

# Tutorial for the WebApp Deployment using AWS:

Just access the link to watch the training of the model and running of the WebApp, Thankyou!

https://github.com/user-attachments/assets/7f6e1c8e-a09e-4994-98f1-bae534708fa1

