# SFTP-Provision
This program uses Python and Ansible to provision an SFTP server for any given user. This will take in three parameters and will use them to create an SFTP server with that user and password combination. 

## Before running the script
Before running the script you must modify playbooks/sftp.yml. You will need to change the parameter for

```
vars:
   ansible_port: 22
   ansible_ssh_pass: __<root password>__
   ansible_become_pass: __<root password>__
   ansible_user: root
```

## Running the Script
To run this script you will need three parameters. 
1. Username (Desired login username)
2. Password (desired login password)
3. IP of machine (IP of the machine to provision)

EX
```
cd SFTP-Provision
python3 generate.py <username> <password> <IP>
```
