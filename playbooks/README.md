## Examples of running Playbooks

## update-hosts.yml
This playbook will prepare Ubuntu VMs for K8s install. It will:
- update hostname to the Ansible Inventory name.
- update /etc/hosts for DNS using the *hosts-file.j2* in the *templates/* folder.
- enable routing.

#### Run playbook
*$ ansible-playbook ./playbooks/update-hosts.yml -i ./inventory/nested-k8s-hosts-kubeadm*

 
## setup-kubeadm.yml
This playbook is used to deploy a K8s cluster using Ansible and kubeadm.
This playbook will: 
- Install required packages for kubeadm and docker.
- Install kubeadm and k8s modules.
- Configure K8s on single Master
- Configure k8s on multiple kube-nodes and join the nodes to the cluster
- Configure kubectl CLI on Master
- Install & Configure Calico SDN for K8s.
- Note: Tested on Ubuntu 16.04 and assumes update-hosts.yml was used to prepare hosts.

#### Run playbook
*$ ansible-playbook ./playbooks/setup-kubeadm.yml -i ./inventory/nested-k8s-hosts-kubeadm*

*$ vi ansible.cfg*    
    ``` bash
    sample
    output from the playbook
    /Users/someone/.ssh/id_rsa
    remote_user = root
    ```
