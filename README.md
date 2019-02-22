# TF_Book_Ch_4

### The purpose of the repository is to explain what is terraform modules, module basics and examples of terraform modules configuration code.

### What is terraform module:

```
Terraform module is any set of terraform configurantion files in a folder. 
```

#### Check the links below for terraform module examples code and explanation on what the code does:
 
 ##### [global/s3](https://github.com/nikcbg/TF_Book_Ch_4/tree/master/global/s3)
 - S3 bucket is where terraform state file for the module and MySQL database is stored. 
--------------------------------------------------------------------------------------------------------
 ##### [module_example/modules/services/webserver_cluster](https://github.com/nikcbg/TF_Book_Ch_4/tree/master/module_example/modules/services/webserver_cluster)
 - terraform configuration code for module that creates webservers cluster and load balancer.
------------------------------------------------------------------------------------------------------------------
 ##### [module_example/prod/data_stores/mysql](https://github.com/nikcbg/TF_Book_Ch_4/tree/master/module_example/prod/data_stores/mysql)
 - terraform configuration code in prod folder that creates MySQL database which talks to webservers cluster.
------------------------------------------------------------------------------------------------------
 #### [module_example/prod/services/webserver_cluster](https://github.com/nikcbg/TF_Book_Ch_4/tree/master/module_example/prod/services/webserver_cluster)
 - terraform configuration code in prod folder that uses the code in module folder to create webservers cluster and load balancer.
 
 
      
  
