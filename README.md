# AWS-cloud-static-Udacity
🌐 Deploy Static Website on AWS
🧠 Project Overview

This project demonstrates how to deploy a static website on AWS using the following key services:

Amazon S3 – to host the website files

Amazon CloudFront – to distribute content globally with low latency

AWS IAM – to manage access and permissions securely

```
📂 Project Structure
/
├── index.html          # The main HTML file (homepage)
├── /img                # Folder containing background and image assets
├── /vendor             # Bootstrap, Font Awesome, and JS library dependencies
├── /css                # Custom CSS styles for the website
└── README.txt          # Project description and setup guide
└── /Screenshots        # Project screenshots


```
🚀 Deployment Steps
1. Create an S3 Bucket

- Open the AWS S3 Console

- Click Create bucket and enter a unique bucket name (e.g., my-demo-bucket-531807)
  <img width="1920" height="1080" alt="Screenshot (73)" src="https://github.com/user-attachments/assets/4ae53efa-4eea-4947-9602-dd0104e47ec7" />

- Uncheck Block all public access
  <img width="1920" height="1080" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/7032e11d-30ce-4b56-80ee-d351ed33f431" />

- Enable Static website hosting under Properties

- Set the index document to index.html
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/beed01b1-5068-4f55-a166-90b52b7d14bc" />

2. Upload Website Files

Upload all files and folders:

index.html
/img
/vendor
/css


Then make the files publicly readable (via permissions or bucket policy).
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/30c0ad5d-9496-499f-9180-d79f8d1fa1ad" />

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
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e1a886c2-dfac-4f1e-9694-0d2a13bcbd8a" />

4. Configure CloudFront 

- Go to CloudFront Console → Create Distribution

- Go to origin → Choose your S3 bucket
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ded6b6c4-7511-4a2f-bec1-440407994b55" />

- Go to Behaviors → Enable Redirect HTTP to HTTPS for security
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7996ccbf-95b5-4d39-b943-2cfc47467e30" />

- Deploy — you’ll get a CloudFront URL to access your site globally
  <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f21f963d-f498-456c-b5b9-7d8f7a3691d9" />

5. Verify Your Website
Open your CloudFront URL or S3 website endpoint in a browser.Your static website should now be live

Live S3 Website URL: http://my-demo-bucket-531807.s3-website-us-east-1.amazonaws.com/

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/942f689d-5936-468c-9516-5571660a12f3" />

Live CloudFront URL: https://d2b29ywfrwec1n.cloudfront.net/

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f7fed52f-5a0b-4728-a175-67312012f3e7" />



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



