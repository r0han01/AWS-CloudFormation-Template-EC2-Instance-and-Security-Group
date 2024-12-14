# AWS CloudFormation Template for EC2 Instance and Security Group

This repository contains an AWS CloudFormation template for deploying an EC2 instance and a security group. The template is designed to demonstrate basic infrastructure creation using CloudFormation.

## Features
- Creates a **Security Group** that allows all inbound and outbound traffic.
- Deploys a **t2.micro EC2 instance** with a specified AMI.
- Outputs:
  - The **Instance ID** of the created EC2 instance.
  - The **Public IP** address of the EC2 instance.
  - The **Security Group ID**.

## Important Notes
1. **Random Placeholder Information**:
   - The VPC ID (`vpc-0123456789abcdef0`) and AMI ID (`ami-1234567890abcdef0`) in the template are **random placeholders** and do not correspond to any actual AWS resources.
   - Replace these placeholders with valid IDs from your AWS account before deploying the template.

2. **Sensitive Information**:
   - No sensitive information is included in this repository.
   - Parameters like VPC ID and AMI ID should be securely managed when deploying the stack.

## How to Use
1. **Update the Template**:
   - Replace the following placeholders with valid values:
     - `VpcId`: Your actual VPC ID.
     - `ImageId`: Your actual AMI ID.

2. **Deploy Using AWS CLI**:
   - Run the following command to deploy the stack:
     ```bash
     aws cloudformation create-stack --stack-name MyStackName \
       --template-body file://template.yaml \
       --parameters ParameterKey=VpcId,ParameterValue=<your-vpc-id> \
                    ParameterKey=AmiId,ParameterValue=<your-ami-id>
     ```

3. **Verify Outputs**:
   - After deployment, review the outputs to get the Instance ID, Public IP, and Security Group ID.

## Disclaimer
This template is for demonstration purposes only and is not intended for production use. Ensure you modify the security group rules as per your requirements before deploying in a real environment.
