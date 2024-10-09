
# AWS CloudFront with Multiple Origins and Failover

This project demonstrates the use of **Amazon CloudFront** to deliver content from multiple origins with failover capabilities. The architecture is designed to ensure high availability and fault tolerance, with requests automatically routed to a backup origin in case the primary origin fails.

## Project Overview

In this project, I have configured an **Amazon CloudFront distribution** with multiple origins to enhance content delivery reliability. The key feature of this setup is failover between the primary and secondary origin, ensuring continuous availability of web assets.

This project was completed as part of the **Digital Cloud Training** bootcamp, where I gained hands-on experience in designing and implementing cloud architectures using AWS services.

### Key Features
- **Multiple Origins**: Two origins were used in the setup, an **S3 bucket** and an **EC2 instance**. CloudFront intelligently routes traffic to the primary origin, while the secondary origin acts as a backup.
- **Origin Failover**: Implemented failover between the two origins to provide resilience in case the primary origin becomes unavailable.
- **Content Caching**: Leveraged CloudFront’s edge locations to cache content closer to users for improved performance and reduced latency.
- **Custom Origin Policies**: Configured origin request policies for enhanced security and content management.

## Architecture

The solution includes:
1. **Amazon CloudFront**: Acts as the content delivery network (CDN) with multiple origins.
2. **Amazon S3**: Serves as the primary origin for delivering static assets.
3. **Amazon EC2**: Configured as the secondary origin to host dynamic content.
4. **Failover Configuration**: If the primary origin (S3) is unavailable, CloudFront automatically routes requests to the secondary origin (EC2).



## AWS Services Used
- **Amazon CloudFront**: For delivering content globally with low latency.
- **Amazon S3**: Used as a scalable object storage service for static content.
- **Amazon EC2**: Serves dynamic content as the backup origin.
- **Route 53**: Configured for DNS management and failover detection.

## How to Deploy
1. Clone the repository to your local environment.
2. Deploy CloudFront with multiple origins using the CloudFormation template.
3. Test the setup by making requests and monitoring failover behavior between origins.

## Lessons Learned
- CloudFront's origin failover mechanism provides a reliable way to ensure availability even in the case of backend failure.
- Setting up appropriate caching policies significantly improves content delivery performance.
- Careful configuration of security and cache invalidation is key to maintaining an efficient and secure CDN.

## Next Steps
- Implement **WAF** (Web Application Firewall) for added security.
- Explore adding more origins with different content types, such as APIs or media streaming.

## Conclusion

This project showcases the implementation of **Amazon CloudFront** with a resilient multi-origin architecture, ensuring high availability and optimal content delivery performance.
![Screenshot 2024-04-12 191727](https://github.com/user-attachments/assets/f9e02108-d061-42bf-b809-fd89f875bd0f)
