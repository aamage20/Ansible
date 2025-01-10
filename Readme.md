## Ansible
Ansible is an open-source automation tool used for configuration management, application deployment, and task automation. It is designed to be simple, agentless, and easy to use, allowing you to automate complex IT tasks such as provisioning servers, configuring systems, and deploying applications across multiple machines.

## Basic Components of Ansible

Playbooks: Files written in YAML format to define automation tasks.

Tasks: Actions defined within playbooks that are executed on target hosts (e.g., install packages, configure settings).

Roles: Groupings of tasks, templates, variables, and files used for better organization of playbooks.

Inventory: A list of target hosts to apply automation tasks to.

Modules: Pre-built pieces of functionality that perform specific tasks (e.g., install packages, manage files).

## Use Case for Ansible

Configuration Management: Ensures systems are in a desired state by automating the installation and configuration of software.

Application Deployment: Automates deployment of applications to multiple servers, ensuring consistency across environments.

Provisioning Infrastructure: Automates the creation and configuration of servers, virtual machines, and cloud instances.

Continuous Integration/Continuous Delivery (CI/CD): Integrates with CI/CD pipelines to automate the deployment process.

Network Automation: Configures networking devices like switches and routers.

## Installation of Ansible on UBUNTU

 
````
sudo apt-add-repository ppa:ansible/ansible
````
````
sudo apt update
````
````
sudo apt install ansible
````
````
ansible --version
````
### set up inventory file

````
sudo nano /etc/ansible/hosts
private-ip of instance
````

### edit ansible.cfg

````
[defaults]
inventory = hosts
host_key_checking = False
````


### ping all nodes to test connection
````
ansible all -m ping
````
### run playbook
````
ansible-playbook nginx.yaml
````

