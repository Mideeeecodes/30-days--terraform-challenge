AME: ODDI, MARYAM OLAMIDEAdd commentMore actions
## TASK: DAILY-UPDATE.MD
## DATE: 30TH JUNE,2025
## TIME:2:03PM

**### Set Up Process Activity**
   - Set up your AWS account.
   - Install Terraform locally.
   - Install AWS CLI and configure it.
   - Install Visual Studio Code (VSCode) and add the AWS plugin.
   - Configure your VSCode to work with AWS.

   **Set up your AWS account**
  - Go to the AWS site https://aws.amazon.com/ to sign up to the console
  - Sign up with a valid email account and a phone number. Also, a valid debit or credit card
  - After signing up, create an IAM account for security purpose instead of using your root user to sign in and allow permissions;amazonec2full instance and AdministratorAccess-AWS
  - Create a separate IAM  account for the terraform configuration.

  **Install Terraform locally**
  - Head over to your cli (anyone of your choice)
  - For mac book; use brew install terraform, for windows you use chocolatey and for linus you use sudo snap install terraform --classic

  **Install AWS CLI**
- For mac; brew install awscli
- For linux; sudo snap install aws-cli --classic

 **Configure AWS CLI**
-  aws configure to configure, it will ask for AWS Access Key ID and AWS AcceSecret Key
- head over to your AWS IAM account, go to users, click on the iam you are using, go to security, create access key, select cli, set description then it will be created. Download the .csv file

**Install Visual Studio Code (VSCode) and add the AWS plugin**
Install Visual Studio Code (VSCode) then at the right top corner you'd see a plus drop down sign, click on it and click on ubuntu and configure aws, put in the AWS Access Key ID and AWS AcceSecret Key from aws.