AWS Cloud Infrastructure with Terraform and Ansible
This project demonstrates the use of Terraform and Ansible for setting up and configuring AWS cloud infrastructure. The setup includes creating a VPC, deploying EC2 instances, and configuring them with Ansible.

Project Overview
Infrastructure: Managed with Terraform
Configuration Management: Managed with Ansible
Components:
VPC with two subnets (one public and one private)
Two EC2 instances (one in each subnet)
Security groups and key pairs
Configuration of NGINX on the public EC2 instance using Ansible
Prerequisites
*Terraform
*Ansible
*AWS account with appropriate permissions

Getting Started
1. Clone the Repository

git clone https://github.com/Ebrahimabdelmonem1/ansible_project.git
cd ansible_project
2. Set Up Terraform
Navigate to the Terraform directory.

Initialize Terraform:

terraform init
Review the planned changes:

terraform plan
Apply the changes to create the infrastructure:

terraform apply
3. Set Up Ansible
Navigate to the Ansible directory.

Ensure you have the necessary inventory and playbook files.

Run the Ansible playbook to configure the public EC2 instance:

ansible-playbook -i inventory playbook.yml

Configuration
Terraform: The Terraform configuration files define the VPC, subnets, EC2 instances, security groups, and key pairs.
Ansible: The Ansible playbook configures the public EC2 instance by installing NGINX, creating a user, a directory, and a file, and then displays the directory content.

**Project Structure:

ansible_project/
│
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
└── ansible/
    ├── inventory.ini
    ├── playbook.yml
    └── roles/
        └── webserver/
            ├── tasks/
            │   └── main.yml
            └── templates/
                └── nginx.conf.j2
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements
Terraform and Ansible documentation
AWS services and tools
Contact
For any questions or feedback, please reach out to esanad912@gmail.com
