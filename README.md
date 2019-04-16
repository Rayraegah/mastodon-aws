# Mastodon on AWS
Terraform module to deploy Mastodon on AWS. This will deploy an ec2 instance with Mastodon and run the service.

## Requirements

- AWS account
    - EC2
    - domain with Route53
- Terraform

## Usage

```terraform
module "mastodon" {
  source            = "github.com/rayraegah/mastodon-aws"
  key_name          = "YOUR KEY"
  instance_type     = "SOME INSTANCE TYPE"
  instance_name     = "SOME NAME"
  smtp_server       = "SMTP SERVER"
  smtp_login        = "SMTP LOGIN"
  smtp_password     = "SMTP PASSWORD"
  smtp_from_address = "SMTP FROM ADDRESS"
  subnet_id         = "SOME SUBNET ID"
  security_group_id = "SOME SECURITY GROUP ID"
  zone_id           = "SOME ROUTE53 ZONE ID"
  domain            = "YOUR DOMAIN NAME" (example: yourdomain.com)
  subdomain         = "YOUR SUBDOMAIN NAME" (example: mastodon)
}
```

## License
MIT