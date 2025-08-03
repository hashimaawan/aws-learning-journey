
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
First install AWS CLI on your Operating System, then open CLI,  you would need access key, Api tokens. To get them login to aws acount as an IAM user(recommended but for testing purpose you can use root user). then goto profile->security credentials and scroll down you will find access key. Don't share this key with anyone.