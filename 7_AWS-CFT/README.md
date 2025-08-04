#  AWS CloudFormation (CFT)

This guide covers everything you need to know to get started with **AWS CloudFormation**, from basic concepts to writing and deploying templates using the **AWS CLI**.

---



## 🔧 What is CloudFormation?

**AWS CloudFormation** is an Infrastructure as Code (IaC) tool that lets you define AWS resources in **YAML or JSON** templates. You can create, update, and delete entire environments using a single template.

CFT act as a middleware between user and cloud and it supports Json, yaml template and is for AWS cloud only. It converts declerative and versioned template to Api call that AWS compatible.
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


