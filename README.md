# udulawscersoluarchiasso2022


#### S3 Bucket Policies Hands On
|Principle|Effect|Action|Resource|Conditions|
|--|--|--|--|--|
|\*|Deny|s3:PutObject|arn| Null s3:x-amz-server-side-encryption;"true"|
|\*|Deny|s3:PutObject|arn| StringNotEquals s3:x-amz-server-side-encryption;"AES256"|
