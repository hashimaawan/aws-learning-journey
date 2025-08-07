#  AWS CloudFormation (CFT)

This guide covers everything you need to know to get started with **AWS CloudFormation**, from basic concepts to writing and deploying templates using the **AWS CLI**.

---



## 🔧 What is CloudFormation?

**AWS CloudFormation** is an Infrastructure as Code (IaC) tool that lets you define AWS resources in **YAML or JSON** templates. You can create, update, and delete entire environments using a single template.

CFT act as a middleware between user and cloud and it supports Json, yaml template and is for AWS cloud only. It converts declerative and versioned template to Api call that AWS compatible.
<br>
CFT also provides Drift Detection, like unintentional changes happended, then you can go to CFT and there is option of detect drift.
<br>
How to transfer yaml files to AWS CFT? Well there is stack, "stack" refers to a collection of AWS resources that are managed as a single unit. These resources are defined in a CloudFormation template, which is a JSON or YAML file describing the desired state of the infrastructure.CloudFormation helps detect "drift," which occurs when changes are made to stack resources outside of the CloudFormation template. This helps maintain the integrity of your infrastructure.
For managing stacks across multiple AWS accounts and regions, CloudFormation provides "Stack Sets," allowing you to deploy and manage stacks in a centralized manner.  
---

## ✅ Prerequisites

- AWS CLI installed ([Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html))
- AWS credentials configured via `aws configure`
- Basic knowledge of services like S3, EC2, Lambda, IAM, etc.

---

## 🧱 Template Structure

Here’s a basic `ec2-template.yaml` example:

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Simple EC2 Template

Parameters:
  InstanceType:
    Type: String
    Default: t2.micro

Resources:
  MyEC2Instance:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: !Ref InstanceType
      ImageId: ami-0abcdef1234567890
      KeyName: MyKeyPair
      Tags:
        - Key: Name
          Value: MyInstance

Outputs:
  InstanceId:
    Description: EC2 Instance ID
    Value: !Ref MyEC2Instance


