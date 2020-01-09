### remote script execution on ssh


[linux - How do I pull from a git repo on a remote machine through ssh? - Stack Overflow](https://stackoverflow.com/questions/38816663/how-do-i-pull-from-a-git-repo-on-a-remote-machine-through-ssh "linux - How do I pull from a git repo on a remote machine through ssh? - Stack Overflow")


 

```shell
ssh -A -p 8100 178.251.45.187 -l issd "cd /home/issd/tkm_profiles && bash deploy.sh docker-compose.swarm-test.yml"
```
