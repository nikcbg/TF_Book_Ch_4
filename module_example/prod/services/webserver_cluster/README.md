# Creating webservers cluster and load balancer in AWS using the module you created earlier in this project

This folder contains terraform code that pulls code form module folder you created earlier in this project and it creates webservers cluster and load balancer in AWS.

--------------------------------------------------------------------------------------------------------------
### List of files in this folder:
- main.tf - terraform configuration file that pulls code form module folder which module creates webserver cluster and load balancer.
- variables.tf - terraform configuration file with input variables.
- output.tf - terraform configuration file with output parameters.
----------------------------------------------------------------------------------------------------------------------
### How to use this part of the repository:
- install `terraform` from [here](https://www.terraform.io/downloads.html).
- setup Amazon Web Services (AWS) account [here](https://aws.amazon.com/).
- configure your AWS access keys [here](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html#access-keys-and-secret-access-keys).
- configure your AWS access keys as environment variables so you can authenticate to your AWS account:

```
export AWS_ACCESS_KEY_ID="your access key id here"
export AWS_SECRET_ACCESS_KEY="your secret access key here"
```
   
- clone the repository to your local computer: `git clone https://github.com/nikcbg/TF_Book_Ch_4`.
- go into the cloned repo on your computer: `cd TF_Book_Ch_4`.
- go into the subfolder which is this example `cd module_example/prod/data_stores/mysql`.

------------------------------------------------------------------------------------------------------------------

### Configure remote state storage using S3 bucket:
- terraform state file of this folder will be stored in the S3 bucket you created in the begining of this project  
- add the below code to your `main.tf` file:

```
terraform {
  backend "s3" {
    bucket  = "name-of-your-S3-bucket"
    region  = "us-east-1"
    key     = "path to the state file inside the bucket"
    encrypt = true
  }
}

```

-------------------------------------------------------------------------------------------------------------------

### Commands needed to build the MySQL database.
- execute `terraform init` - to initialize the provider and download the neccesery plugins.
  
- execute `terraform plan` - to create execution plan for changes to be applied, the output should diplay the following:

```
Terraform will perform the following actions:

  + aws_db_instance.example
  
Plan: 1 to add, 0 to change, 0 to destroy.
```
  
- execute `terraform apply` - to apply the desired changes, the output should diplay the following:

```
Terraform will perform the following actions:

  + aws_db_instance.exampl
  
aws_db_instance.example: Creating...  

Apply complete! Resources: 1 added, 0 changed, 0 destroyed.

Outputs:

address = address-of-MySQL-database-in-AWS
port = XXXX

```
  
