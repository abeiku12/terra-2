# AWS Free Tier Infrastructure with Terraform and CloudFormation

## Overview
This repository contains sample infrastructure-as-code (IaC) scripts using Terraform and AWS CloudFormation to deploy AWS Free Tier resources. These scripts are designed to help users get started with AWS infrastructure management while keeping costs minimal.

## Prerequisites
- An active AWS Free Tier account
- AWS CLI installed and configured
- Terraform installed (for Terraform scripts)
- AWS CloudFormation enabled in your AWS account

## Features
- Deploys a basic AWS infrastructure using Free Tier resources
- Supports both Terraform and CloudFormation templates
- Creates an EC2 instance, S3 bucket, and an IAM role with minimal permissions
- Easily customizable for additional AWS services

## Setup Instructions
### Using Terraform
1. Navigate to the `terraform/` directory:
   ```sh
   cd terraform/
   ```
2. Initialize Terraform:
   ```sh
   terraform init
   ```
3. Plan the deployment:
   ```sh
   terraform plan
   ```
4. Apply the deployment:
   ```sh
   terraform apply
   ```
5. To destroy the resources:
   ```sh
   terraform destroy
   ```

### Using CloudFormation
1. Navigate to the `cloudformation/` directory:
   ```sh
   cd cloudformation/
   ```
2. Deploy the CloudFormation stack:
   ```sh
   aws cloudformation create-stack --stack-name MyFreeTierStack --template-body file://template.yaml --capabilities CAPABILITY_IAM
   ```
3. To delete the CloudFormation stack:
   ```sh
   aws cloudformation delete-stack --stack-name MyFreeTierStack
   ```

## Resources Created
- **EC2 Instance**: Free-tier t2.micro instance
- **S3 Bucket**: Storage for objects (default private access)
- **IAM Role**: Basic role for accessing S3 from EC2

## Notes
- Ensure that your AWS CLI is configured with credentials that have the necessary permissions.
- These scripts are designed to use AWS Free Tier, but always verify AWS billing to avoid unexpected charges.
- Modify variables in `terraform.tfvars` or `template.yaml` as needed.

## Contributing
Feel free to submit issues or pull requests to improve these scripts.

## License
This project is licensed under the MIT License.

