 # Terraform module example that creates webservers cluster and load balancer

#### This folder contains Terraform code that deploys webservers cluster (using EC2 and Auto Scaling) and load balancer in AWS and returns "Hello World" text, database adress and port number.

-----------------------------------------------------------------------------------------------------------------------
### List of files in the repository:
- __main.tf__ - terraform configuration file that creates webservers cluster and load balancer.
- __variables.tf__ - terraform configuration file with input variables.
- __output.tf__ - terraform configuration file with output parameters.
- __user_data.sh__ - bash script that prints "Hello World", database adress and port number.
---------------------------------------------------------------------------------------------------------------

## Note: Terraform module is not supposed to be deployed directly and it should be used in other terraform code. 
All the code in this module is pulled in by the stage and production examples. 
