# SFTP-Provision
This program uses Python and Ansible to provision an SFTP server for any given user. This will take in three parameters and will use them to create an SFTP server with that user and password combination. 

##Installing Ansible
Ansible Can not be run from a Windows platform so you must use some distro of OSX or Linux. 
### Ubuntu:
```
$ sudo apt-get update
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```


## Before running the script
Before running the script you must modify playbooks/sftp.yml. You will need to change the parameter for

```
vars:
   ansible_port: 22
   ansible_ssh_pass: <root password>
   ansible_become_pass: <root password>
   ansible_user: root
```

Before running this script you must also make sure that you have ssh'd into the SFTO server to make sure the host machines fingerprint is on the SFTP server prior to running. 

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
