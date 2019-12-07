### auto create non existing dir in ansible


[What's the easy way to auto create non existing dir in ansible - Stack Overflow](https://stackoverflow.com/questions/22472168/whats-the-easy-way-to-auto-create-non-existing-dir-in-ansible "What's the easy way to auto create non existing dir in ansible - Stack Overflow")




```yml
- name: Ensures {{project_root}}/conf dir exists
  file: path={{project_root}}/conf state=directory
- name: Copy file
  template:
    src: code.conf.j2
    dest: "{{project_root}}/conf/code.conf"
```
