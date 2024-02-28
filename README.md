# **Project: Chicken Disease Classification**

## **Procedures**

1. Update config.yaml <br/>
2. Update secrets.yaml [Optional] <br/>
3. Update params.yaml <br/>
4. Update the entity <br/>
5. Update the configuration manager in src config <br/>
6. Update the components <br/>
7. Update the pipeline <br/>
8. Update the main.py <br/>
9. Update the dvc.yaml

## **How to run?**
### **Steps**
Clone the repository: <br/>
```
https://github.com/animeshg27/Chicken-Disease-Classification.git
```

### STEP 01- Create a conda environment after opening the repository
`conda create -n chicken python=3.8 -y` <br>
`conda activate chicken`

### STEP 02- install the requirements
`pip install -r requirements.txt`


`# Finally run the following command` <br>
`python app.py`

Now, 

open up you local host and port

# AWS-CICD-Deployment-with-Github-Actions
### 1. Login to AWS console.
### 2. Create IAM user for deployment
```
#with specific access

1. EC2 access : It is virtual machine 

2. ECR: Elastic Container registry to save your docker image in aws1


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
```

### 3. Create ECR repo to store/save docker image
```
- Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken
```

### 4. Create EC2 machine (Ubuntu)
### 5. Open EC2 and Install docker in EC2 Machine:
```
#optional

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```
### 6. Configure EC2 as self-hosted runner:
```
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```
### 7. Setup github secrets:
```
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = simple-app
```
## AZURE-CICD-Deployment-with-Github-Actions
### Save pass:
s3cEZKH5yytiVnJ3h+eI3qhhzf9q1vNwEi6+q+WGdd+ACRCZ7JD6

### Run from terminal:
docker build -t chickenapp.azurecr.io/chicken:latest<br>

docker login chickenapp.azurecr.io<br>

docker push chickenapp.azurecr.io/chicken:latest<br>
### Deployment Steps:
1. Build the Docker image of the Source Code<br>
2. Push the Docker image to Container Registry<br>
3. Launch the Web App Server in Azure<br>
4. Pull the Docker image from the container registry to Web App server and run<br>

