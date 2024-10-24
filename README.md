Ansible Project for EC2 Deployment
 This project uses Ansible to deploy Docker containers running NGINX on AWS EC2 instances. 
It leverages a Bastion Host for secure access to private EC2 instances.
 Features- Automated provisioning of EC2 instances on AWS.- Secure access to private EC2 instances through a Bastion Host.- NGINX deployment using Docker containers.- High Availability by distributing instances across Availability Zones (AZs)


 Project Structure
 ├── roles/
│   ├── common/
│   ├── web/
├── playbooks/
│   └── site.yml
└── inventory/


- roles/: Contains reusable Ansible roles for configuration.- playbooks/: The main Ansible playbooks for deployment.
 Requirements
 1. AWS Account: Ensure you have access to AWS and appropriate IAM permissions.
 2. Ansible: Installed on your local machine.
 3. SSH Key Pair: For accessing EC2 instances.
Setup and Deployment

 1. Clone the repository:
#    git clone https://github.com/Ebrahimabdelmonem1/ansible_project.git
#   cd ansible_project
 2. Update the inventory file with EC2 instance details.
 3. Run the Ansible playbook to configure the instances and deploy NGINX:
#    ansible-playbook -i inventory playbook.yml
 4. Verify the NGINX server is running by accessing the public IP of the EC2 instance.
 Clean-Up
 Terminate the EC2 instances to avoid unwanted AWS charges.

 License
 This project is licensed under the MIT License - see the LICENSE file for details
