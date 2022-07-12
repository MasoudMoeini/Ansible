# Ansible
[Reference](https://docs.ansible.com/ansible/latest/index.html)<br/>
Ansible uses OpenSSH — the open source connectivity tool for remote login with the SSH (Secure Shell) protocol.<br/>
Ansible is decentralized–it relies on your existing OS credentials to control access to remote machines. And if needed<br/>
You need invetory, To Set Up Ansible Inventories:<br/>
```
nano ansible inventory
```
```
203.0.113.111
203.0.113.112
203.0.113.113
server_hostname
```
```
ansible-inventory -i inventory --list
```
```
ansible-playbook -i inventory playbook.yaml
ansible-playbook -i hosts nginx.yaml --check 
ansible-playbook nginx.yaml
```


