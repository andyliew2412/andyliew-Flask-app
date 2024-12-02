**CE7 Module 3 Assignment 3.5**

**How to create docker image contain app and deploy to private ECR using Terraform**

Tools: AWS ECS, ECR, Docker, Flask, and Terraform.

1) Create a new github repository and Clone the github repository locally.

2) Under your local git folder create terraform" folder to store all TF files (backend.tf, main.tf, provider.tf, variable.tf and compute.tf) use to setup private ECR repository.

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

5) To push docker image to AWS ECR, enter the command below (You can get this command form AWS->Private ECR repository-> View push commands). Make sure you have AWS CLI installed and AWS Configure on your local computer. Run all the command one by one, you should able to see your docker image uploaded into AWS ECR.

ECR Image
![Screenshot 2024-12-02 at 11 21 33 PM](https://github.com/user-attachments/assets/ffbac4ae-ee1c-4d1e-9edc-e1e072d12384)

ECR Repository Created
![Screenshot 2024-12-02 at 11 17 04 PM](https://github.com/user-attachments/assets/aee908b9-2d7e-4f6c-bd1c-00f04e5c7931)

ECS Cluster Created
![Screenshot 2024-12-02 at 11 12 38 PM](https://github.com/user-attachments/assets/236a661d-7484-44fd-8218-1aef38f4bcc6)

Resource Link :
Guide for creating private ECR using terraform https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ecr_repository
