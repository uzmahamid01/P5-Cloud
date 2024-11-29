# Build and Host a Website on AWS S3 with Automated Updates via CodePipeline and GitHub

**Author:** Uzma Hamid  
**Date:** November, 2024  

This README outlines the process to host a static website securely on AWS S3 with automated updates via AWS CodePipeline and GitHub. The setup includes domain registration, SSL configuration, and CI/CD automation for seamless website updates.

## Overview

### Part 1: Launch and Host the Website on AWS S3
1. **Purchase Domain:** Buy a domain from providers like Namecheap.
2. **Create Webpage:** Build your static website and organize the files in a local folder.
3. **AWS S3 Setup:**
   - Create an S3 bucket, enable static website hosting, and upload your website content.
   - Configure permissions to make content publicly accessible.
4. **Domain Binding:** Set up a CNAME record to link your domain to the S3 bucket.

### Part 2: Secure the Website with SSL Certificate
1. **Route 53 Setup:** Create a hosted zone and configure DNS to point to the S3 bucket.
2. **SSL Certificate:** Use AWS Certificate Manager to generate and associate an SSL certificate.
3. **CloudFront Setup:** Configure CloudFront for secure, fast content delivery and HTTPS redirection.
4. **DNS Records:** Update Route 53 to point to the CloudFront distribution for secure access.

### Part 3: Automate Website Updates with CodePipeline and GitHub
1. **GitHub Repository:** Create and push website files to a GitHub repository.
2. **AWS CodePipeline Setup:** 
   - Configure CodePipeline to monitor changes in the GitHub repo and deploy updates to S3.
   - Set up a source stage (GitHub), a build stage (if required), and a deploy stage (S3).
3. **Website Updates:** Any changes to the GitHub repository are automatically deployed to the live website.

## Services Used
- **Namecheap (Domain):** Provides a custom domain for easy website access.
- **Amazon S3:** Hosts the static website files.
- **Amazon Route 53:** Manages DNS settings for domain linking.
- **AWS Certificate Manager (ACM):** Issues SSL/TLS certificates for HTTPS.
- **AWS CloudFront:** Distributes content globally and ensures secure HTTPS access.
- **AWS CodePipeline:** Automates the CI/CD pipeline, deploying website updates from GitHub to S3.
- **GitHub:** Manages version control and triggers updates to the website.

## Live Website
- **Website URL:** [https://cs412uhamid.me](https://cs412uhamid.me)
- **S3 Endpoint:** [cs412uhamid.me.s3-website.us-east-2.amazonaws.com](http://cs412uhamid.me.s3-website.us-east-2.amazonaws.com)
