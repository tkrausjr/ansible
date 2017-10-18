## Examples of running Playbooks

## update-hosts.yml
This playbook will update hostname, /etc/hosts, and enable routing fon all the target machines using the *hosts-file.j2* in the *templates/* folder to get ready for k8s.

#### Run playbook
*$ ansible-playbook ./playbooks/update-hosts.yml -i ./inventory/nested-esxi-hosts*


 
## setup-kubeadm.yml
This playbook is used to deploy a K8s cluster using Ansible and kubeadm.
This playbook will: 
- Install required packages for kubeadm and docker.
- Install kubeadm and k8s modules.
- Configure K8s on single Master
- Configure k8s on multiple kube-nodes and join the nodes to the cluster
- Configure kubectl CLI on Master
- Install & Configure Calico SDN for K8s.

#### Runplaybook
*$ ansible-playbook ./playbooks/setup-kubeadm.yml -i ./inventory/nested-esxi-hosts*

*$ vi ansible.cfg*    
    ``` bash
    sample
    output from the playbook
    /Users/someone/.ssh/id_rsa
    remote_user = root
    ```
