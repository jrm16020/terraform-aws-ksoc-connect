# terraform-aws-ksoc-connect

Allows KSOC to connect to your AWS account to perform EKS/ECS/ECR discovery and pro-active monitoring of these resources.

## Usage

During sign-up, you will have been provided with an AWS IAM Role ARN - this should be passed into the module using the `ksoc_role_arn` variable:

``` terraform
module ksoc_connect {
  ksoc_role_arn = "arn:aws:iam::EXAMPLE:role/EXAMPLE"
}
```

Once applied, the module will then output a newly-created AWS IAM Role ARN in your account. This should be provided to KSOC to complete the connection process.
