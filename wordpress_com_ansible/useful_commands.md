brew install python
brew install ansible
brew install vagrant
--install virtual box

ansible --version

--create the vagrant file as the example and after run the below command
vagrant up

--first ansible command
ansible wordpress -u vagrant --private-key .vagrant/machines/wordpress/virtualbox/private_key -i hosts -m shell -a 'echo Hello, World'

ansible -vvvv wordpress -u vagrant --private-key .vagrant/machines/wordpress/virtualbox/private_key -i hosts -m shell -a 'echo Hello, World'

--you need to create the provisioning.yml file after that you can run the below command:
ansible-playbook provisioning.yml -u vagrant -i hosts --private-key .vagrant/machines/wordpress/virtualbox/private_key

ansible-playbook provisioning.yml -i hosts --private-key .vagrant/machines/wordpress/virtualbox/private_key

ansible-playbook provisioning.yml -i hosts


---
mysql -u root
show databases;
use xxx;
show tables;