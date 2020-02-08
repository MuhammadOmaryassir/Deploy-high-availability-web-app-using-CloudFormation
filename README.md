![][header]

[header]: https://github.com/Omaroovee/Deploy-high-availability-web-app-using-CloudFormation/blob/Read-Me/header.jpeg "Header"

<br>

# Deploy a High-Availability Web Application Using AWS CloudFormation

Infrastructure-as-code (IAC) that automates the process of creating a secured and high-availability environment and deploying an application (packaged and staged in AWS S3 Storage) into a dockerized Apache Web Server. The script contains all the configurations needed for a repeatable process so that the infrastructure can be discarded and recreated at will multiple times.

<br>

### Features

`1.`  Load-balanced servers with auto-scaling capability across two availability zones within a single region.

`2.`  Server/instance specification: 2vCPUs, 4GB RAM, 10GB disk space.

`3.`  Linux Operating System using the Ubuntu distribution machine image.

`4.`  Compute instances are secured in a private subnet and only accepts traffic originating from a bastion host and load-balancer both within a public subnet.

`5.`  Each availability zone contain a bastion host to enable SSH to instances in each of the private subnets for debugging and troubleshooting.

`6.`  Load-balancer, bastion host, and application servers have security groups defined with only needed ports opened.

`7.`  Application servers have outbound internet access via NAT gateway for critical OS updates and patches.

`8.`  Sample application code is packaged and stored in an S3 bucket with IAM permissions.

`9.`  Application servers are configured with IAM instance profile to be able to access and download application code from AWS S3 bucket.

`10.` Application code is deployed in a dockerized apache web server for added security and isolation.

`11.` Health checks and thresholds are defined to aid in system availability detection.  Metrics are collected, aggregated, and monitored via AWS CloudWatch.

`12.` Entire environment is fully virtualized in a cloud platform that can be taken down and brought back up within a short period of time. The process of creating and starting all the services, spinning up instances are automated via scripts in this repo.

<br>

### Detailed Infrastructure Architecture

![alt text][architecture]

[architecture]: https://github.com/Omaroovee/Deploy-high-availability-web-app-using-CloudFormation/blob/Read-Me/UDGRAM-Design.png "Architecture Diagram"

<br>


### Credits
Udacity Cloud DevOps Nanodegree Program<br>
Author : Muhammad Omar<br>
Email : Omaroovee@gmail.com<br>
