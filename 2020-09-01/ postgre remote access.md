###  postgre remote access


[How to enable remote access to PostgreSQL server on a Plesk server? – Plesk Help Center](https://support.plesk.com/hc/en-us/articles/115003321434-How-to-enable-remote-access-to-PostgreSQL-server-on-a-Plesk-server- "How to enable remote access to PostgreSQL server on a Plesk server? – Plesk Help Center")


 

```
psql -U postgres -c 'SHOW config_file'

add to file

listen_addresses = '*'


```
