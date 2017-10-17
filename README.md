## This is my Ansible Practice Repository

### Setup
 
 Ansible host - OSX
	*$ pip install ansible *
	*$ vi ansible.cfg *    (Either in /etc/ansible/ or in current directory you are running from)


		[defaults]
		host_key_checking = False
		private_key_file = /Users/someone/.ssh/id_rsa
		remote_user = root

	*$ ssh-keygen -t rsa *
	Your identification has been saved in /Users/someone/.ssh/id_rsa.
	Your public key has been saved in /Users/someone/.ssh/id_rsa.pub.
  
  	For Certificate based Auth you will need to copy your public key to all target hosts.

  	*$ ssh-copy-id -i ~/.ssh/id_rsa.pub root@10.173.13.31 *
  	
  Target hosts
  	> Usually taget hosts will need Python 2.x such as 2.7. 
  	> On Ubunutu 16.04 this was not installed and required either
  	> On each host, 
  	*$ sudo apt-get install -y python-minimal *
  	>	OR
  	> From the Ansible host create an inventory with all target hosts and run 
  	*$ ansible -i ./inventory/nested-esxi-hosts --sudo -m raw -a "apt-get install -y python-minimal" all *

  TEST the setup
  	*$ ansible kube-cluster -i ./inventory/nested-esxi-hosts -m ping*