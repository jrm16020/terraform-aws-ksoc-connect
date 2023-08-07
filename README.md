# terraform-aws-ksoc-connect

Allows KSOC to connect to your AWS account to perform pro-active monitoring of your AWS resources.

## Terraform Registry

This module is available in the [Terraform Registry](https://registry.terraform.io/) see [here](https://registry.terraform.io/modules/ksoclabs/ksoc-connect/aws/latest).

## Contributing

The most important thing to be aware of when contributing is that we leverage the [Semantic Release Action](https://github.com/cycjimmy/semantic-release-action) to automate our changelog, see [here](CHANGELOG.md).

This requires us to use [conventional git commits](https://www.conventionalcommits.org/en/v1.0.0/) when committing to this repository.

Each PR merge into the `main` branch will execute the release process defined [here](.github/workflows/release.yml).

## Usage

This module requires you to obtain a set of API credentials from KSOC (access_key/secret) and also needs your Ksoc account id.

When running the module you need to be authenticated against your target AWS account. See examples directory for more information.

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0.8 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 3.62.0 |
| <a name="requirement_ksoc"></a> [ksoc](#requirement\_ksoc) | >= 0.0.1 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | >= 3.62.0 |
| <a name="provider_ksoc"></a> [ksoc](#provider\_ksoc) | >= 0.0.1 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_iam_instance_profile.this](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_instance_profile) | resource |
| [aws_iam_role.this](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role) | resource |
| [aws_iam_role_policy_attachment.readonly](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [ksoc_aws_register.this](https://registry.terraform.io/providers/ksoclabs/ksoc/latest/docs/resources/aws_register) | resource |
| [aws_caller_identity.current](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/caller_identity) | data source |
| [aws_iam_policy_document.assume_role](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/iam_policy_document) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_ksoc_access_key_id"></a> [ksoc\_access\_key\_id](#input\_ksoc\_access\_key\_id) | Ksoc API key | `string` | n/a | yes |
| <a name="input_ksoc_account_id"></a> [ksoc\_account\_id](#input\_ksoc\_account\_id) | Ksoc Account Identifier | `string` | n/a | yes |
| <a name="input_ksoc_secret_key"></a> [ksoc\_secret\_key](#input\_ksoc\_secret\_key) | Ksoc API secret | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_role_arn"></a> [role\_arn](#output\_role\_arn) | AWS IAM Role ARN which Ksoc uses to connect |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## License
Apache 2 Licensed. See [LICENSE](LICENSE) for full details.
