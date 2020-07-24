### ubuntu 20 pgadmin 


[Download](https://www.pgadmin.org/download/pgadmin-4-apt/ "Download")


 

```
https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/

sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'

must be focal for 20.04
```
