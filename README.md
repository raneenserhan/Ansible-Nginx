# NGINX-AWS-ANSIBLE <br/>

## About <br/><br/>
This is to Run nginx using AWS infrastructure, using ansible to provision infrastructure.<br/>
##### uses and creates following aws services:<br/>
* VPC and it's components
* Subnet, Route Table, Internet Gateway.
* EC2 instance(ubuntu)
* Kaypair
* Security Groups to access EC2 instance

------------------------------------------------------------------------------------------------<br/>
## Pre-requisite:<br/><br/>
* create an IAM user and create security credentials(AccessKey, SecretKey) and update in the in the vars.yml file 

  ![image](https://user-images.githubusercontent.com/82150368/118038314-a2476480-b377-11eb-8709-099f2f59909d.png)

* install python by entering the following:<br/>
  sudo apt update<br/>
  sudo apt install python3.8  
  * Allow the process to complete and verify the Python version was installed sucessfully:<br/>
  python3 ––version
* install ansible:<br/>
  apt install -y ansible
  * Allow the process to complete and verify the Python version was installed sucessfully:<br/>
   ansible --version
* install Community AWS Collection:<br/>
  ansible-galaxy collection install community.aws
* install boto:<br/>
  python3 -m pip install boto3
  
------------------------------------------------------------------------------------------------<br/>

## Usage:<br/>
### provisioning :<br/>
* git clone https://github.com/raneenserhan/Ansible-Nginx.git
* in the cmd enter: ansible-playbook -e @vars.yml main.yml

------------------------------------------------------------------------------------------------<br/>
### Versions:
* python 3.8.5
* ansible 2.10.9

