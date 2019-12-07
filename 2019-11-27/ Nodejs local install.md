###  Nodejs local install





 

```
Prerequisites

virtualenv -p python2 .venv
source .venv/bin/activate
pip install ansible
example of galaxy
ansible-galaxy install geerlingguy.nodejs


ansible-playbook -e ansible_python_interpreter=/usr/bin/python  playbook.yml

- name: "Ansible playbook example"
  hosts: 127.0.0.1
  connection: local
  become: true
  roles:
    - geerlingguy.nodejs
```
