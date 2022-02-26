# tfmod_vpc_igw

Terraform module to create VPC internet gateway in AWS

## Variables

``` terraform
# name: the name of the VPC internet gatewa
variable "vpc_igw_example" { default = "example" }
```

## Dependency

VPC <https://github.com/virsas/tfmod_vpc>

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
  source = "github.com/virsas/tfmod_vpc_igw"
  vpc    = module.vpc_main.id
  name   = var.vpc_igw_default
}
```
