# Creating S3 bucket.

### Why you need S3 bucket and its purpose.
S3 bucket is needed to store Terraform state file of MySQL database. The database talks to the webservers cluster. Webservers cluster also needs to read the state file of MySQL database to make sute it reads data from the right database. 
--------------------------------------------------------------------------------------------------------------
### List of files in the repository:
- __main.tf__ - terraform configuration files to create S3 bucket.
- __variables.tf__ - terraform configuration file with variables parameters.
- __output.tf__ - terraform configuration file with output parameters.

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
- go into the subfolder which is this example `cd global/s3`.

------------------------------------------------------------------------------------------------------------------
### Commands needed to create the S3 bucket. 

- execute `terraform init` - to initialize the provider and download the neccesery plugins.
  
- execute `terraform apply` - to apply the desired changes.

- execute `terraform destroy` - to destroy the resource that you just created.
