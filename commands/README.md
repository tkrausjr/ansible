

1) kraust-m01:ocp-install-demo kraust$ ansible all -m ping --ask-pass -i ~/gitHub/ansible/sps_hosts
SSH password:
192.168.10.21 | SUCCESS => {
    "changed": false,
    "failed": false,
    "ping": "pong"
}