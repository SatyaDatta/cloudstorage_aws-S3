# cloudstorage_aws-S3

Task 
> - Create and configure cloud storage on AWS S3
> - Upload example files
> - Configure access permissions
> - Provide proof of setup and public access


S3 - Bucket Name - codetech-s3-bucket 

Files Uploaded 
| File Name                  | Type       | Description               |
|----------------------------|------------|---------------------------|
|  sample.txt                | Text File  | Simple sample text file   |
|  about_bg_1.jpg            | Image      | Sample image file         |
|  next-font-manifest.json   | JSON       | Sample Json File          |


Public Links 

https://codetech-s3-bucket.s3.us-east-1.amazonaws.com/about_bg_1.jpg  IMAGE 
https://codetech-s3-bucket.s3.us-east-1.amazonaws.com/next-font-manifest.json JSON
https://codetech-s3-bucket.s3.us-east-1.amazonaws.com/sample.txt    JSON 


BUCKET POLICY 
{
    "Version": "2012-10-17",
    "Id": "PublicAccessPolicy",
    "Statement": [
        {
            "Sid": "DenyInsecureConnections",
            "Effect": "Deny",
            "Principal": "*",
            "Action": "s3:*",
            "Resource": [
                "arn:aws:s3:::codetech-s3-bucket",
                "arn:aws:s3:::codetech-s3-bucket/*"
            ],
            "Condition": {
                "Bool": {
                    "aws:SecureTransport": "false"
                }
            }
        },
        {
            "Sid": "AllowPublicRead",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::codetech-s3-bucket/*"
        }
    ]
}

![Screenshot 2025-05-25 160353](https://github.com/user-attachments/assets/50d1870e-2c5a-43dd-ae04-772a80106e58)
![Screenshot 2025-05-25 160808](https://github.com/user-attachments/assets/b946c0cd-c089-4b25-811d-e21e94369752)
![Screenshot 2025-05-25 161411](https://github.com/user-attachments/assets/861d8df2-c3af-44e1-9643-3b4507db2cf2)





