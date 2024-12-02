andyliew CE7 Module 3 Assignment 3.5

How to create docker image contain app and deploy to private ECR using Terraform

Tools: AWS ECS, ECR, Docker, Flask, and Terraform.

1) Create a new github repository and Clone the github repository locally.

2) Under your local git folder create terraform" folder to store all TF files (backend.tf, compute.tf, provider.tf and variable.tf) use to setup private ECR repository.

3) Create Terraform resource to deploy private ECR Repository. Change Directory to folder containing terraform files. Run the following commands one after another:
   a. terraform init
   b. terraform plan
   c. terraform apply
Above to create the private ECR repository in AWS. Check console.

4) Create a folder to store Dockerfile, with the following commands:
   a. docker build -t andyliew-ce7-3.5-container 
   b. docker images
   c. docker run -dp 8080:8080 andyliew-ce7-3.5-container 
   d. docker ps
   e. curl localhost:8080
![Screenshot 2024-12-03 at 12 49 06 AM](https://github.com/user-attachments/assets/a8471680-a406-4901-aa89-3c03e6d4216f)
