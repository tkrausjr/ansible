## Examples of running Playbooks

## update-hosts.yml
This playbook will update /etc/hosts file on all the target machines using the *hosts-file.j2* in  
the *templates/* folder.

*$ ansible-playbook ./playbooks/update-hosts.yml -i ./inventory/nested-esxi-hosts*


 
## future-playbook.yml
1. *$ vi ansible.cfg*    
    ``` bash
    sample
    output from the playbook
    /Users/someone/.ssh/id_rsa
    remote_user = root
    ```
