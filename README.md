# ansible-bootcamp

## Goals
1. Use Ansible to deploy the NodeWeightTracker application

## Configuration:
* Clone reposetory - https://github.com/TamirAtia/week6-terraform-ansible and follow the instruction
* Clone this reposetory
* Connect with ssh to Ansible Controller VM and clone this reposetory
* Run the command `export ANSIBLE_HOST_KEY_CHECKING=False` to enable connection to the hosts machines with user name and password.
* Add two files, `inventory` and `vars`
* In inventory copy this and fill the IP of the VM's and the user and password

```
20.231.98.221 host="20.231.98.221" 
20.231.98.222 host="20.231.98.222"
  

[all:vars]
ansible_connection=ssh
ansible_port=22:wq
ansible_user=<user name> 
ansible_ssh_pass=<password>
```

* In vars copy this and fill them
```
pghost: 
pg_username: ""
pg_password: ""
okta_url: ""
okta_client_id: ""
okta_client_secret: ""

```
* Run this command `ansible-playbook -i inventory playbook.yaml`
