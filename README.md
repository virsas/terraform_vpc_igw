# terraform_vpc_igw

Terraform module to create VPC internet gateway in AWS

## Variables

``` terraform
# name: the name of the VPC internet gatewa
variable "vpc_igw_example" { default = "example" }
```

## Dependency

VPC <https://github.com/virsas/terraform_vpc>

## Terraform example

``` terraform
######################
# VPC IGW variables
######################
variable "vpc_igw_default" { default = "DefaultGW" }

######################
# VPC internet gateway
######################
module "vpc_igw" {
  source = "git::https://github.com/virsas/terraform_vpc_igw.git?ref=v1.0.0"
  vpc    = module.vpc_main.id
  name   = var.vpc_igw_default
}
```
