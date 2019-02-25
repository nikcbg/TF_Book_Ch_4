 # Terraform module example that creates webservers cluster and load balancer
This folder contains Terraform code that deploys webservers cluster (using EC2 and Auto Scaling) and load balancer in AWS and returns "Hello World" text, database adress and port number.

-----------------------------------------------------------------------------------------------------------------------
### List of files in the repository:
- main.tf - terraform configuration file that creates webservers cluster and load balancer.
- variables.tf - terraform configuration file with input variables.
- output.tf - terraform configuration file with output parameters.
- user_data.sh - bash script that prints "Hello World", database adress and port number.
---------------------------------------------------------------------------------------------------------------
### Remote state storage using S3 bucket:
- terraform state file of this folder will be stored in the S3 bucket you created in the begining of this project

-------------------------------------------------------------------------------------------------------------

### Note:
Terraform module is not supposed to be deployed directly and it should be used in other terraform code. All the code in this module is pulled in by the stage and production examples. 

----------------------------------------------------------------------------------------------------------------------------
