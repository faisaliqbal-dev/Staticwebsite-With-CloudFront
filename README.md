# Secure Static Website Delivery using AWS CloudFront and S3

## Project Overview
This project demonstrates how to deploy a static website using AWS S3 as the origin and AWS CloudFront as the Content Delivery Network (CDN) while maintaining security best practices by keeping the S3 bucket private.

## Architecture
- **AWS S3**: Private bucket serving as origin for static website files
- **AWS CloudFront**: Global CDN for fast content delivery
- **Origin Access Control (OAC)**: Secure connection between CloudFront and private S3 bucket

## Key Features
- ✅ Private S3 bucket with public access blocked
- ✅ CloudFront distribution for global content delivery
- ✅ Origin Access Control for secure S3 access
- ✅ No static website hosting enabled on S3
- ✅ Cost-effective and scalable solution

## Prerequisites
- AWS Account
- Basic understanding of AWS services
- Static website files (HTML, CSS, JS)

## Implementation Steps

### 1. Create S3 Bucket
```bash
# Create a private S3 bucket
- Keep all public access settings blocked
- Upload your static website files
- Do NOT enable static website hosting
```

### 2. Setup CloudFront Distribution
```bash
# Configure CloudFront
- Create new distribution
- Set S3 bucket as origin
- Configure Origin Access Control (OAC)
- Set default root object (index.html)
```

### 3. Configure Origin Access Control
```bash
# Create OAC policy
- Generate OAC in CloudFront
- Update S3 bucket policy to allow CloudFront access
- Ensure bucket remains private to public
```

## Benefits
- **Security**: S3 bucket remains completely private
- **Performance**: Global edge locations reduce latency  
- **Cost Optimization**: Pay only for data transfer and requests
- **Scalability**: Automatically handles traffic spikes
- **SSL/TLS**: HTTPS enabled by default

## File Structure
```
project/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── images/
│   └── assets/
└── README.md
```

## Technologies Used
- **AWS S3** - Object storage for static files
- **AWS CloudFront** - Content Delivery Network
- **Origin Access Control** - Secure access management

## Deployment
1. Upload website files to S3 bucket
2. Create CloudFront distribution with S3 as origin
3. Configure OAC for secure access
4. Update DNS (if using custom domain)
5. Test website through CloudFront URL

## Security Features
- Private S3 bucket with blocked public access
- Origin Access Control prevents direct S3 access
- CloudFront provides DDoS protection
- SSL certificate for HTTPS delivery

---

**Note**: This project maintains AWS security best practices by keeping the S3 bucket private while enabling global content delivery through CloudFront.
