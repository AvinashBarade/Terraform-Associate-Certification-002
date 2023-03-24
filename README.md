# Terraform-Associate-Certification-002-




# Variables 

1. String 
2. List 
3. Map
4. Number
5. bool 
6. null


## Count & Count Index

count.index 


count = 5 
will itterate till 4 resources 


condition ? true-value : false-value

count = var.istest == true ? 1:0


## Local Values

locals {

}
local.



## Terraform functions

Only functions build in to the language are we can use. 
No user-defined functions. 

test functions on terraform console 
max()
min()
element(list,inxdex)
file(path)
lookup(map,key,defalut)
formatdate(spec, timestamp)
timestamp() ${path.module}




## Data Sources 

data {}

just like var. use data.


## Debugging in terraform 

export TF_LOG = TRACE, DEBUG, INFO WARN, ERROR

TF_LOG_PATH = /TEMP/LOGS/LOG.LOG



## Terraform format

indentation 

terraform fmt

## terraform validate


## Load Order & Semantics


## Dynamic BLock


resource "" {

    // other things 
dynamic "" {

    for_each = var.ports
    content {

    }
}

}


## Tainting Resources 

terraform taint aws_instance.ec2

terraform plan

delete & create again 

## Splat expression

output "arns" {
    value = aws_iam_user.lb[*].arn
}

* is splat expression



## Terraform Graph 

terraform graph > graph.dot


terraform plan -out=demopath

## Terraform output


## Terrafomr settings 

REQUIRE_VERSION
required_providers

## 

-refresh= false
-target= resource 


## Zipmap function 

output mapping 

zipmap(key,values) 


## Comments in terraform 

#
//
/* */


## Data Type (Set)

list [] allow duplicate 

set {} uniqe

toset([list])



## Foreach 