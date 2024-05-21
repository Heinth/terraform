To use multiple provier with specific version
---------------------------------------------

# vi provider.tf
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
    local = {
      source = "hashicorp/local"
      version = "2.4.1"
    }

  }
}

Apply without confirmation
---------------------------
# terraform apply -auto-approve

To check the terraform config is valid or not
---------------------------------------------
# terraform validate

To format the terraform configuration
-------------------------------------
# terraform fmt

To check the current state of the infrastructure
------------------------------------------------
# terraform show

To check the how many providers are using in current directory
--------------------------------------------------------------
# terraform providers

Update the state file as Real Infra
----------------------------------
# terraform refresh

Commands related with the terraform state
------------------------------------------
# terraform state show aws_s3_bucket.finance (terraform state <subcommand> [options] [args])
                                                                list
                                                                mv
                                                                pull
                                                                rm
                                                                show
                                                                push

To check terraform worksapce 
----------------------------
# terraform workspace list
Create new workspace 
--------------------
# terraform workspace new production
# terraform workspace new development
Change workspace
# terraform workspace select default

