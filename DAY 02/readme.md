## NAME: ODDI, MARYAM OLAMIDE
## TASK: DAILY-UPDATE.MD
## DATE: 31ST JUNE,2025
## TIME: 3:35AM

**### Set Up Process Activity**
   - Set up your AWS account.
   - Install Terraform locally.
   - Install AWS CLI and configure it.
   - Install Visual Studio Code (VSCode) and add the AWS plugin.
   - Configure your VSCode to work with AWS.
   - Deploy and single server and a web server

## Set up your AWS account

Go to the AWS site https://aws.amazon.com/ to sign up to the console
Sign up with a valid email account and a phone number. Also, a valid debit or credit card
After signing up, create an IAM account for security purpose instead of using your root user to sign in and allow permissions; amazonec2full instance and AdministratorAccess-AWS
Create a separate IAM account for the terraform configuration.
Install Terraform locally

Head over to your cli (anyone of your choice)
For mac book; use brew install terraform, for windows you use chocolatey and for linux you use sudo snap install terraform — classic
However, there are several ways of installing terraform. Instead of going through the above process, you can install Terraform manually by going to the Terraform home page, clicking the download link, selecting the appropriate package for your operating system, downloading the ZIP archive, and unzipping it into the directory where you want Terraform to be installed. The archive will extract a single binary called terraform, which you’ll want to add to your PATH environment variable same goes for aws cli.

## Install AWS CLI

For mac; brew install awscli
For linux; sudo snap install aws-cli — classic
Configure AWS CLI

aws configure to configure, it will ask for AWS Access Key ID and AWS AcceSecret Key
head over to your AWS IAM account, go to users, click on the iam you are using, go to security, create access key, select cli, set description then it will be created. Download the .csv file

Install Visual Studio Code (VSCode) and add the AWS plugin
Install Visual Studio Code (VSCode) then at the right top corner you’d see a plus drop down sign, click on it and click on ubuntu and configure aws, put in the AWS Access Key ID and AWS Secret Key .
AWS Access Key ID [None]:
AWS Secret Access Key [None]:
Default region name [None]: us-east-1
Default output format [None]: json

Terraform commands:

Terraform init: this prepares your working directory for other commands
Terraform validate: this checks whether the configuration is valid
Terraform plan: this show changes required by the current configuration
Terraform apply: this creates or updates infrastructure
Terraform destroy: this destroys previously created infrastructure
Deploying a Single Server

Terraform Code Basics

Language: HashiCorp Configuration Language (HCL)
File Extension: .tf
Declarative Language: Describe desired infrastructure, and Terraform creates it.
Create an empty folder and put a file in it called main.tf
that contains the following contents:

provider "aws" {
region = "us-east-2"
}

In a terminal, go into the folder where you created main.tf and run the
terraform init command:

$ terraform init
When using Terraform, you need to run terraform init to tell Terraform to scan the code, figure out which providers you’re using, and download the code for them. By default, the provider code will be downloaded into a
.terraform folder, when it’s done, you do the terraform plan command.

$ terraform plan
Terrraform plan command lets you see what terraform will do before creating changes. Also, terraform is planning on creating
a single EC2 Instance. To create the Instance, run the terraform apply command:

$ terraform apply
The apply command will show the same plan output and
asks you to confirm whether you actually want to proceed with this plan. Type yes and enter to deploy the EC2 Instance.

You have just deployed an EC2 Instance in your AWS account using
Terraform! To verify this, go over to the EC2 console.
![image1](./image/)

## Deploying a Single Web Server

Run a Web Server on the Instance

Now that the instance is set up, the next step is to:

Install a web server: Choose a web server software (e.g., Apache, Nginx)
Configure the web server: Set up the web server to serve content
Start the web server: Launch the web server and make it accessible
#DevOps #Terraform #AWS #InfrastructureAsCode #CloudComputing #30DayChallenge #IaC