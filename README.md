# udulawscersoluarchiasso2022

#### S3 Security & Bucket Policies
Principal: The account or user to apply the policy to
#### S3 Bucket Policies Hands On
|Principal|Effect|Action|Resource|Conditions|
|--|--|--|--|--|
|\*|Deny|s3:PutObject|arn| Null s3:x-amz-server-side-encryption;"true"|
|\*|Deny|s3:PutObject|arn| StringNotEquals s3:x-amz-server-side-encryption;"AES256"|
