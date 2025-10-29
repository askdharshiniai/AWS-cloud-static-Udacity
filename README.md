# AWS-cloud-static-Udacity
🌐 Deploy Static Website on AWS
🧠 Project Overview

This project demonstrates how to deploy a static website on AWS using the following key services:

Amazon S3 – to host the website files

Amazon CloudFront – to distribute content globally with low latency

AWS IAM – to manage access and permissions securely

The website showcases a travel-themed landing page built using HTML, CSS, Bootstrap, and Font Awesome.

```
📂 Project Structure
/
├── index.html          # The main HTML file (homepage)
├── /img                # Folder containing background and image assets
├── /vendor             # Bootstrap, Font Awesome, and JS library dependencies
├── /css                # Custom CSS styles for the website
└── README.txt          # Project description and setup guide

```
🚀 Deployment Steps
1. Create an S3 Bucket

Open the AWS S3 Console

Click Create bucket and enter a unique bucket name (e.g., my-travel-website-bucket)

Uncheck Block all public access

Enable Static website hosting under Properties

Set the index document to index.html

2. Upload Website Files

Upload all files and folders:

index.html
/img
/vendor
/css


Then make the files publicly readable (via permissions or bucket policy).

3. Set Bucket Policy

Add the following bucket policy to allow public read access:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
```
4. Configure CloudFront (Optional but Recommended)

Go to CloudFront Console → Create Distribution

Choose your S3 bucket as the origin

Enable Redirect HTTP to HTTPS for security

Deploy — you’ll get a CloudFront URL to access your site globally

5. Verify Your Website

Open your bucket or CloudFront URL in a browser — your static website should be live 🌍

👩‍💻 Technologies Used

```
HTML5

CSS3

Bootstrap (via /vendor/)

Font Awesome

Amazon S3

Amazon CloudFront

AWS IAM
```

🏁 Expected Outcome

```
By completing this project, you will:

Understand AWS S3 static website hosting

Learn how to configure CloudFront for global distribution

Manage IAM permissions and bucket policies securely

Successfully deploy and host a professional static website
```
## Website link
http://my-demo-bucket-531807.s3-website-us-east-1.amazonaws.com/

## Screenshots:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8d372e3e-4375-4a99-b31d-c47947493a94" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/069d32c0-0b2a-49db-b13b-c3554987f332" />







