# FaaS-in-FaaS
Deploying a school presentation about Function as a Service inside a Function as a Service. In my case: I deployed it through AWS Lambda. 

Warning: this project is not secured in any way and may incur massive cloud cost in case of a DDOS-Attack or similar. Do not do this in a production environment. Set up cost alerts and learn more about DDOS-Protection [here](https://community.aws/content/2wCgfxx2OxWO5jt2TLTh2QEfOXS/application-security-ddos-protection). 

## Configuration 

### AWS Lambda
- Function URL=True
- AUTH_TYPE =None


### S3-Bucket

Bucket Settings:

```
Block Public Access: Off
```

Bucket-Policy: 

```
"Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "<Your Bucket ARN>/*"
        }
    ]

```