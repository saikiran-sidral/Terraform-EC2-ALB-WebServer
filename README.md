# Terraform AWS EC2 + ALB Setup
This project contains Terraform scripts to set up a simple and scalable web server architecture on AWS.
The setup includes EC2 instances deployed in a public subnet, managed by an Application Load Balancer (ALB) to distribute incoming traffic evenly and ensure high availability.

## Architecture:
* VPC: A custom Virtual Private Cloud to host the infrastructure.

* Public Subnet: Hosts EC2 instances and ALB.

* Internet Gateway: Provides internet access to the VPC.

## Security Groups:

ALB allows HTTP (port 80) from the internet.

EC2 instances accept traffic only from the ALB.

## EC2 Instances:

Automatically provisioned with Apache via user_data.

Application Load Balancer (ALB): Distributes traffic across EC2 instances.

Publicly accessible via its DNS name.

## Setup
Clone the repository:

git clone https://github.com/saikiran-sidral/Terraform-EC2-ALB-WebServer.git

cd Terraform-EC2-ALB-WebServer/EC2-ALB-WebServer-Terraform

* Initialize Terraform: "terraform init"

* Review the plan: "terraform plan"

* Apply the configuration: "terraform apply"

## Access the Web Server:

After deployment, Terraform will output the ALB DNS name.

Open the DNS URL in your browser to access the web server.

* Destroy the infrastructure to avoid ongoing costs: "terraform destroy"

## Acknowledgments:

* Terraform Documentation: https://www.terraform.io/docs  
* AWS Documentation: https://aws.amazon.com/documentation/
