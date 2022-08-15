# udulawscersoluarchiasso2022

## EC2 Fundamentals
### EC2 Instance Types Basics
[EC2 info](http://ec2instances.info)


## EC2 - solutions architect
### EC2 Placement Groups
You can specify
- Cluster: single AZ
- Spread: across underlying hardware

### S3 Security & Bucket Policies
Principal: The account or user to apply the policy to
### S3 Bucket Policies Hands On
|Principal|Effect|Action|Resource|Conditions|
|--|--|--|--|--|
|\*|Deny|s3:PutObject|arn| Null s3:x-amz-server-side-encryption;"true"|
|\*|Deny|s3:PutObject|arn| StringNotEquals s3:x-amz-server-side-encryption;"AES256"|

### S3 Websites
|Principal|Effect|Action|Resource|Conditions|
|--|--|--|--|--|
|\*|Allow|s3:GetObject|arn||



#### S3 CORS
##### Preflight Requeset
```
OPTIONS
Host B
Origin A
```
Preflight Response
```
Access-control-allow-origin: A
Access-control-allow-methods: GET, PUT, DELETE
```

#### S3 CORS Hands On
Permission -> CORS
```
[
  {
    "AllowedHeaders": [
    ],
    "AllowedMethods":[
    ],
    "AllowedOrigins":[
    ],
    "ExposedHeaders":[
    ],
    "MaxAgeSeconds": 3000
  }
]
```



## Section 25: Networking - VPC
### CIDR, Private vs public IP
classless inter-domain routing -a method for allocating IP address

### VPC Overview
You can have multiple VPCs in an AWS region (max 5 per region - soft limit)

##### Max CIDR per VPC is 5. For each CIDR
Min size is/28  (16 address)
Max size is/16  (65536 address)

### Internet Gateway and Route Tables

One VPC can only be attached to one IGW and vice versa

### Bastion Hosts
- We can use a Bastion Host to SSH into our private EC2 instances


### NAT Instances Hands On
HTTP
HTTPS
Source: 10.0.0.0/16
##### 04:48
Add All ICMP - IPv4   10.0.0.0/16




### NAT Gateways
- NAT Gateway is resilient within a single availablity zone
- Must create multiple NAT Gateways in multiple AZ for fault-tolerance


### DNS Resolution Options Route 53 Private Zones
DNS Resolution (enableDnsSupport)

##### DNS Hostnames
By default
- True => default VPC
- False => newly created VPCs
If true, assigns public hostname to EC2 instance if it has a public IPv4


### NACL & Security Groups
One NACL per subnet, new subnets are assigned the Default NACL
1-32766, higher precedence with a lower number
