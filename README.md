## Synopsis
+ A working REPO of my Ansible learning and work.

## Setup
 
Ansible host - OSX
1. *$ pip install ansible*
1. *$ vi ansible.cfg*    (Either in /etc/ansible/ or in current directory you are running from)
    ```[defaults]
    host_key_checking = False
    private_key_file = /Users/someone/.ssh/id_rsa
    remote_user = root
    ```
1. *$ ssh-keygen -t rsa*

```Your identification has been saved in /Users/someone/.ssh/id_rsa.
Your public key has been saved in /Users/someone/.ssh/id_rsa.pub.
```
For Certificate based Auth you will need to copy your public key to all target hosts.
1. *$ ssh-copy-id -i ~/.ssh/id_rsa.pub root@10.173.13.31*




## Built With
+ List of technology/tools you used to develop the project
## Resources
+ External resources you used for the project
## API Reference
+ API reference if you used any.
## Contributors
+ Who worked on the project
## License
+ Mention if the project is under any sort of License
## Acknowledgments
+ Write references of site you used
+ i.e [Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
+ and [mastering-markdown](https://guides.github.com/features/mastering-markdown/)
+ Mention book or people who helped you
+ Inspiration