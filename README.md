AWS Storage Services Project (Amazon S3)

In this project, I worked with Amazon S3 (Simple Storage Service) to create and manage a storage bucket, upload and manage objects, configure public access permissions, and host a static website using HTML files. I also used AWS CLI to perform S3 operations.


Objectives

In this project, I aimed to:

Create an S3 bucket
Upload, retrieve, and delete objects
Configure bucket permissions for public access
Host a static website using HTML files
Use AWS CLI to manage S3 operations
Upload frontend mentee files to S3

S3 Bucket Details

Bucket Name: mary-s3-12
Region: us-east-1
Static Website URL:

  http://mary-s3-12.s3-website-us-east-1.amazonaws.com
 
Mentee Work Uploaded

I uploaded frontend HTML files provided by a mentee as part of this project.

Mentee Name: Chinwedu Onyewezu
File Type: HTML (Frontend Web Page)
Purpose: Hosted as a static website using Amazon S3

AWS CLI Commands Used

1. Create S3 Bucket
aws s3 mb s3://mary-s3-12

I successfully created the S3 bucket.

2. Upload Object

aws s3 cp index.html s3://mary-s3-12/

I successfully uploaded the HTML file to the bucket.

3. List Objects in Bucket

aws s3 ls s3://mary-s3-12/

I confirmed that the uploaded file exists in the bucket.

4. Download Object

aws s3 cp s3://mary-s3-12/index.html .

I successfully retrieved the file to my local environment.

5. Delete Object

aws s3 rm s3://mary-s3-12/index.html

I successfully deleted the object from the bucket.

THEN manually uploaded the html file again to configure bucket permission

Bucket Permissions Configuration

To make my objects publicly accessible, I:

Disabled Block Public Access settings
Added a bucket policy allowing public read access:

json id="policy1"
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadAccess",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::mary-s3-12/*"
    }
  ]
}<img width="1335" height="664" alt="website page 2" src="https://github.com/user-attachments/assets/10543321-5fec-4f23-afa9-15596962314d" />
<img width="1335" height="657" alt="website page" src="https://github.com/user-attachments/assets/dce58fd0-5e5a-4129-bb3c-55d5e26711cc" />
<img width="1335" height="654" alt="CLI Output" src="https://github.com/user-attachments/assets/da6efbf8-ed54-4cf1-8a05-43e708cfa83d" />
<img width="1337" height="658" alt="S3 BUCKET CREATED" src="https://github.com/user-attachments/assets/7cef227d-c320-44e9-9e0d-2ecf8a9de3cf" />
<img width="1338" height="657" alt="s3 bucket config" src="https://github.com/user-attachments/assets/cad46667-656a-4cc0-be00-1b8b71ac85a3" />






Result:My objects became publicly accessible via URL.


Static Website Hosting

I enabled static website hosting in my S3 bucket and configured:

Index document: index.html

Website Endpoint:

http://mary-s3-12.s3-website-us-east-1.amazonaws.com

Result: I successfully hosted a static website and accessed it through the browser.

Conclusion

Through this project, I gained hands-on experience in using Amazon S3 for cloud storage, managing permissions, hosting static websites, and using AWS CLI for resource management. This strengthened my understanding of AWS storage services and cloud deployment workflows.

Skills I Demonstrated

Amazon S3 bucket management
AWS IAM and bucket policy configuration
Static website hosting on AWS
AWS CLI operations
Cloud storage fundamentals
