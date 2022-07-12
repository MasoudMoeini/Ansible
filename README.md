# Ansible
[Reference](https://docs.ansible.com/ansible/latest/index.html)<br/>
Ansible uses OpenSSH — the open source connectivity tool for remote login with the SSH (Secure Shell) protocol.<br/>
Ansible is decentralized–it relies on your existing OS credentials to control access to remote machines.<br>
You need invetory, To Set Up Ansible Inventories:<br/>
```
nano ansible inventory
203.0.113.111
203.0.113.112
203.0.113.113
server_hostname
```
```
nano ansible-hosts
[myvirtualmachines]
192.0.2.50
192.0.2.51
192.0.2.52
```
Now we have two customised inventory hosts
```
cat inventory
or 
cat ansible-hosts
``` 
```
ansible-inventory -i inventory --list
ansible-inventory -i ansible-hosts --list
```
To run playbook on localhost without inventory hosts
```
ansible-playbook ansible-local.yml 
```
To run playbook on customised inventory hosts 
```
ansible-playbook -i ansible-hosts ansible-local-all.yml 
```
```
Excluded
ansible-playbook -i inventory playbook.yaml
ansible-playbook -i ansible-hosts playbook.yaml
ansible-playbook -i hosts nginx.yaml --check 
ansible-playbook nginx.yaml
ansible-playbook -i ansible-hosts ansible-local-all.yml 
```


