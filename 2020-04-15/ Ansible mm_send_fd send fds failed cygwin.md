###  Ansible mm_send_fd send fds failed cygwin


[Ansible throws an error with SSH connection reset when used under cygwin - Server Fault](https://serverfault.com/questions/886438/ansible-throws-an-error-with-ssh-connection-reset-when-used-under-cygwin "Ansible throws an error with SSH connection reset when used under cygwin - Server Fault")


 $ ansible all -m ping

example.org | UNREACHABLE! => {

    "changed": false,

    "msg": "Failed to connect to the host via ssh: mm_send_fd: sendmsg(2): Connection reset by peer\r\nmux_client_request_session: send fds failed\r\n",

    "unreachable": true 

}



```bash
Add the following lines to ansible.cfg (either in the playbook folder or in /etc/ansible/ansible.cfg):

[ssh_connection]
ssh_args = -o ControlMaster=no
From what I've gathered, ControlMaster=auto also works, but under cygwin this option has to be disabled. Source.
```
