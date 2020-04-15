### Ansible provisioning ERROR Using a SSH password instead of a key is not possible


[vagrant - Ansible provisioning ERROR! Using a SSH password instead of a key is not possible - Stack Overflow](https://stackoverflow.com/questions/42462435/ansible-provisioning-error-using-a-ssh-password-instead-of-a-key-is-not-possibl "vagrant - Ansible provisioning ERROR! Using a SSH password instead of a key is not possible - Stack Overflow")


Using a SSH password instead of a key is not possible because Host Key checking is enabled

```bash
This error can also be solved by simply export ANSIBLE_HOST_KEY_CHECKING variable.

export ANSIBLE_HOST_KEY_CHECKING=False

```
