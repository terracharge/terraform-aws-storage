<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | 1.2.3 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | 4.19.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 4.19.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_this_label"></a> [this\_label](#module\_this\_label) | terracharge/label/aws | 0.1.0 |

## Resources

| Name | Type |
|------|------|
| [aws_s3_bucket.this](https://registry.terraform.io/providers/hashicorp/aws/4.19.0/docs/resources/s3_bucket) | resource |
| [aws_s3_bucket_acl.this](https://registry.terraform.io/providers/hashicorp/aws/4.19.0/docs/resources/s3_bucket_acl) | resource |
| [aws_s3_bucket_cors_configuration.this](https://registry.terraform.io/providers/hashicorp/aws/4.19.0/docs/resources/s3_bucket_cors_configuration) | resource |
| [aws_s3_bucket_logging.this](https://registry.terraform.io/providers/hashicorp/aws/4.19.0/docs/resources/s3_bucket_logging) | resource |
| [aws_s3_bucket_public_access_block.this](https://registry.terraform.io/providers/hashicorp/aws/4.19.0/docs/resources/s3_bucket_public_access_block) | resource |
| [aws_s3_bucket_server_side_encryption_configuration.this](https://registry.terraform.io/providers/hashicorp/aws/4.19.0/docs/resources/s3_bucket_server_side_encryption_configuration) | resource |
| [aws_s3_bucket_versioning.this](https://registry.terraform.io/providers/hashicorp/aws/4.19.0/docs/resources/s3_bucket_versioning) | resource |
| [aws_s3_bucket_website_configuration.this](https://registry.terraform.io/providers/hashicorp/aws/4.19.0/docs/resources/s3_bucket_website_configuration) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_acl"></a> [acl](#input\_acl) | Default ACL to use when uploading files | `string` | `"private"` | no |
| <a name="input_context"></a> [context](#input\_context) | Default environmental context | <pre>object({<br>    organization = string<br>    environment  = string<br>    account      = string<br>    product      = string<br>    tags         = map(string)<br>  })</pre> | n/a | yes |
| <a name="input_cors_allowed_header"></a> [cors\_allowed\_header](#input\_cors\_allowed\_header) | Allowed headers for cors | `list(string)` | `[]` | no |
| <a name="input_cors_allowed_methods"></a> [cors\_allowed\_methods](#input\_cors\_allowed\_methods) | Allowed method for CORS access | `list(string)` | `[]` | no |
| <a name="input_cors_allowed_origins"></a> [cors\_allowed\_origins](#input\_cors\_allowed\_origins) | Allowed origins for CORS | `list(string)` | `[]` | no |
| <a name="input_cors_exposed_header"></a> [cors\_exposed\_header](#input\_cors\_exposed\_header) | Headers which are exposed through CORS requests | `list(string)` | `[]` | no |
| <a name="input_error_document"></a> [error\_document](#input\_error\_document) | Error page document in S3 bucket | `string` | `"404.html"` | no |
| <a name="input_index_document"></a> [index\_document](#input\_index\_document) | Index page document in S3 bucket | `string` | `"index.html"` | no |
| <a name="input_is_logging"></a> [is\_logging](#input\_is\_logging) | Determines if the bucket is intended for logging purposes | `bool` | `false` | no |
| <a name="input_kms_arn"></a> [kms\_arn](#input\_kms\_arn) | KMS Key to use | `string` | n/a | yes |
| <a name="input_logging_bucket"></a> [logging\_bucket](#input\_logging\_bucket) | Target bucket for logging | `string` | n/a | yes |
| <a name="input_name"></a> [name](#input\_name) | Name of the bucket to create | `string` | n/a | yes |
| <a name="input_origin_path"></a> [origin\_path](#input\_origin\_path) | Path in S3 bucket for hosted files, with leading slash | `string` | `"/"` | no |
| <a name="input_public_access"></a> [public\_access](#input\_public\_access) | Disables or enabled the public access block | <pre>object({<br>    block_public_acls       = bool<br>    block_public_policy     = bool<br>    restrict_public_buckets = bool<br>    ignore_public_acls      = bool<br>  })</pre> | <pre>{<br>  "block_public_acls": true,<br>  "block_public_policy": true,<br>  "ignore_public_acls": true,<br>  "restrict_public_buckets": true<br>}</pre> | no |
| <a name="input_routing_rules"></a> [routing\_rules](#input\_routing\_rules) | A json array containing routing rules describing redirect behavior and when redirects are applied | `map(string)` | <pre>{<br>  "/": "index.html"<br>}</pre> | no |
| <a name="input_versioning"></a> [versioning](#input\_versioning) | Enables or disables bucket versioning | `bool` | `true` | no |
| <a name="input_website_enabled"></a> [website\_enabled](#input\_website\_enabled) | Enables or disabled static website functionality | `bool` | `false` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_arn"></a> [arn](#output\_arn) | ARN of the created S3 bucket |
| <a name="output_domain_name"></a> [domain\_name](#output\_domain\_name) | Regional domain name of the created S3 bucket |
| <a name="output_id"></a> [id](#output\_id) | ID of the created S3 bucket |
| <a name="output_website_domain"></a> [website\_domain](#output\_website\_domain) | Website domain of the created S3 bucket if hosting is enabled |
| <a name="output_website_endpoint"></a> [website\_endpoint](#output\_website\_endpoint) | Website endpoint of the created S3 bucket if hosting is enabled |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
<!-- markdownlint-disable -->
<!-- prettier-ignore-end -->
