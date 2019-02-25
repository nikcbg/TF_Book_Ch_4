# Createing MySQL database in AWS

This folder contains terraform code that creates MySQL database in AWS.

--------------------------------------------------------------------------------------------------------------
### List of files in this folder:
- main.tf - terraform configuration file that creates MySQL datavase.
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
### Commands needed to build the MySQL database.
- execute `terraform init` - to initialize the provider and download the neccesery plugins.
  
- execute `terraform plan` - to create execution plan for changes to be applied, the output should diplay the following:  
```

```
  
- execute `terraform apply` - to apply the desired changes, the output should diplay the following:

```

```
  
