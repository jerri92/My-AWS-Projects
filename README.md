# Load Balancer Configuration

This repository contains resources and configurations related to setting up a Load Balancer across multiple availability zones, enabling secure access to a website.

## Overview
The load balancer is configured in all three availability zones to ensure high availability and fault tolerance. It supports the following ports:
- **HTTP (80)**
- **HTTPS (443)**

## Security Features
- **HTTPS Support**: To enhance security, HTTPS has been enabled for the load balancer.
- **SSL Certificate**: A certificate was generated using **Amazon Certificate Manager (ACM)**.
- **Domain Setup**: A **CNAME record** was created in the hosted zone using **Route 53**, making the website accessible via HTTPS.

## Website Access
The website is now accessible securely over HTTPS.

## Prerequisites
- An active AWS account.
- A domain configured in Amazon Route 53.
- Access to Amazon Certificate Manager for SSL certificate creation.

## Steps to Reproduce
1. **Create a Load Balancer**:
   - Deploy the load balancer across three availability zones.
   - Enable HTTP (80) and HTTPS (443) ports.

2. **Generate SSL Certificate**:
   - Use Amazon Certificate Manager to create an SSL certificate for your domain.

3. **Update DNS Records**:
   - In Route 53, create a CNAME record pointing to the load balancer's domain.

4. **Verify HTTPS Access**:
   - Open a browser and navigate to your website's HTTPS URL.

## Tools and Technologies Used
- **AWS Elastic Load Balancer (ELB)**
- **Amazon Certificate Manager (ACM)**
- **Amazon Route 53**

## License
This project is open-source and available under the [MIT License](LICENSE).

