# AWS S3 Tutorial

Amazon S3 is an object storage service used to **store** and **retrieve** any amount of data at any time. It stores data as **objects** within **buckets**. Each object consists of:

- Data (the file content)
- Metadata (key-value pairs)
- A unique identifier (key)
- AWS gives 99.999..(11 9's) gurantee that object will not be deleted

---

## Use Cases

- Static website hosting  
- Backup and restore  
- Data lakes and analytics  
- Software delivery (e.g., storing binaries)  
- Media storage (images, videos, etc.)

---

## AWS CLI Setup

### Installation (macOS / Linux / Windows WSL)
```bash
pip install awscli --upgrade --user

Configure AWS CLI

aws configure

You will be prompted for:

AWS Access Key ID

AWS Secret Access Key

Default region (e.g., us-east-1)

Default output format (e.g., json)

Create a Bucket
aws s3 mb s3://my-first-bucket

Security and Permissions
Bucket Policy Example: Make Objects Public
{
  "Version": "2012-10-17",
  "Statement": [{
    "Sid": "PublicReadGetObject",
    "Effect": "Allow",
    "Principal": "*",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::my-first-bucket/*"
  }]
}
