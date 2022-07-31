# udulawscersoluarchiasso2022

#### S3 Security & Bucket Policies
Principal: The account or user to apply the policy to
#### S3 Bucket Policies Hands On
|Principal|Effect|Action|Resource|Conditions|
|--|--|--|--|--|
|\*|Deny|s3:PutObject|arn| Null s3:x-amz-server-side-encryption;"true"|
|\*|Deny|s3:PutObject|arn| StringNotEquals s3:x-amz-server-side-encryption;"AES256"|

#### S3 Websites
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
