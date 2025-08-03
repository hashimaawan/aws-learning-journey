## 🧩 1. What is AWS CLI?
The AWS Command Line Interface (CLI) lets you interact with AWS services (like S3, EC2, Lambda, etc.) directly from your terminal using simple commands.

You can create, configure, and manage AWS resources without logging into the AWS Management Console.


## Why AWS CLI over UI?
Because AWS UI is not automation friendly. Using API we can do the things programitically and thus reduce the need of doing things manually by going to UI.
<br>

### Various Tools used
- AWS CLI
- Terraform
- Cloud Formation
- CDK

<br>User submit commands through aws CLI which translates into API that aws understands. Terraform, CDK they all do same.
<br>Every tool has its own usecase like CLI for quick access and terraform, CFT for large infrastructure.

### To link account to aws CLI
First install AWS CLI on your Operating System. 
- macOS :-  brew install awscli
- For Linux :-  url "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
aws --version
- Windows :- 👉 https://awscli.amazonaws.com/AWSCLIV2.msi
Then open CLI,  you would need access key, Api tokens. To get them login to aws acount as an IAM user(recommended but for testing purpose you can use root user). then goto profile->security credentials and scroll down you will find access key. Don't share this key with anyone.
<br>
Once get the access key, goto terminal and write aws configure and provide the required information