# Some useful commands and instructions

## You need to install the softwares below
* brew install python (Python 2.7.16)
* brew install ansible (ansible 2.10.9)
* brew install vagrant (Vagrant 2.2.16)
* install virtual box (version compatible with vagrant version, example: 6.1.22)

---

### Check ansible version
* ansible --version

---
## Some steps to follow
* create the vagrant file as the example and after run the below command
   * vagrant init ubuntu/bionic64
   * vagrant up

* Ansible commands:
    * ansible wordpress -u vagrant --private-key .vagrant/machines/wordpress/virtualbox/private_key -i hosts -m shell -a 'echo Hello, World'

    * ansible -vvvv wordpress -u vagrant --private-key .vagrant/machines/wordpress/virtualbox/private_key -i hosts -m shell -a 'echo Hello, World'

    * you need to create the provisioning.yml file after that you can run the below command:
        * ansible-playbook provisioning.yml -u vagrant -i hosts --private-key .vagrant/machines/wordpress/virtualbox/private_key

        * ansible-playbook provisioning.yml -i hosts --private-key .vagrant/machines/wordpress/virtualbox/private_key

        * ansible-playbook provisioning.yml -i hosts 
            * Note: **for this last command we don't need to inform the user and private key parameters, because it is inside the hosts file**

---
## Some Mysql commands
* mysql -u root
* show databases;
* use xxx;
* show tables;
---
