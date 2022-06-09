# Basic commands
---
```Bash
ansible -i hosts.ini -m ping demo
```
```Bash
ansible -i hosts.ini -m user -a "name=dmitrytyt state=present" demo
```
```Bash
ansible -i hosts.ini -m user -a "name=dmitrytyt2 state=present" -b -K demo
```
```Bash
ansible -i hosts.ini -m user -a "name=dmitrytyt2 state=absent" -b -K demo
```
```Bash
ansible -i hosts.ini -m user -a "name=dmitrytyt2 state=absent" -e "ansible_become=true ansible_become_password=123" demo
```
## Commands ansible-playbook
```Bash
ansible-playbook -i hosts.ini user.yml
```
To enter the password, use the command
```Bash
ansible-playbook -i hosts.ini user.yml -K
```