# Terraform
Terraform examples and modules

## Prerequisites
Configure AWS Cli access for all the AWS accounts you want to work with.

Example for configuring `dev` account. Repeat similarly for `qa`, `prod`,`tools` accounts. 
```
$ aws configure --profile aws-dev-account
AWS Access Key ID [None]: ACCESS_KEY
AWS Secret Access Key [None]: SECRET_KEY
Default region name [None]: us-east-1
Default output format [None]:
```
Once done, these profiles should be available for use with aws cli and terraform - `dev`, `qa`, `prod`,`tools`. We refer to these using profile under aws provider block.

## Templates subdirectories

### base
To create a S3 bucket for use as Terraform remote backend. Execute this first, to setup the resources that are required for other templates using the S3 backend. For details, please refer to the readme in the sub-directory.

### ecr
To create an AWS ECR repo, for use with the AWS ECS cluster. For details, please refer to the readme in the sub-directory.

### ecs
To create a ECS Fargate cluster with auto-scaling, application load balancer and other related resources. For details, please refer to the readme in the sub-directory.
