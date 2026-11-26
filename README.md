# 2-tier-architecture-with-route53
AWS Two-Tier Architecture with Route 53: Designed and implemented a scalable web application using AWS EC2 and RDS (MySQL), integrated with Amazon Route 53 for DNS management and domain routing. Configured VPC, subnets, security groups, and database connectivity to ensure secure and reliable application access.
In this project, the application is divided into two main layers: the Web/Application Tier and the Database Tier. The Web/Application Tier is hosted on Amazon EC2, which handles user requests and application processing. The Database Tier uses Amazon RDS (MySQL) to store and manage application data.

Amazon Route 53 is integrated to manage DNS records and route user requests to the application using a domain name. Amazon VPC provides an isolated network environment with public and private subnets, while Security Groups control communication between different resources.
2. AWS Services Used
1. Amazon VPC: Created an isolated virtual network for hosting AWS resources.
2. Amazon EC2: Deployed the web application and handled user requests.
3. Amazon RDS (MySQL): Created and managed the application database.
4. Amazon Route 53: Configured DNS records to connect the domain name to the application.
5. Internet Gateway: Enabled internet connectivity for public resources.
6. NAT Gateway: Provided outbound internet access to private resources.
7. Security Groups: Controlled inbound and outbound network traffic.
8. Application Load Balancer (if used): Distributed incoming application traffic across multiple EC2 instances.
3. Project Implementation
- Created a custom VPC with public and private subnets.
- Launched an EC2 instance in the public subnet to host the web application.
- Installed and configured the required web server, such as Apache or Nginx.
- Created an Amazon RDS MySQL database in private subnets.
- Configured database connectivity between EC2 and RDS using Security Groups.
- Created a Route 53 hosted zone and configured DNS records.
- Connected the domain name to the application using an appropriate DNS record.
- Tested the application through the domain name in a web browser.
- Verified communication between the web server and the database.
  The application works in the following sequence:
1. The user enters the website domain name in a browser.
2. Amazon Route 53 resolves the domain name to the application's endpoint.
3. The request reaches the EC2 web server.
4. EC2 processes the request and communicates with the RDS database.
5. RDS retrieves or stores the requested information.
6. EC2 sends the response back to the user's browser.
