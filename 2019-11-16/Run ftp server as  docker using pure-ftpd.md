### Run ftp server as  docker using pure-ftpd







```shell
docker run -d --name ftpd_server --restart always -p 21:21 -p 30000-30099:30000-30099 -e FTP_USER_NAME=navigation_downloader -e FTP_USER_PASS=zTWmG5bch -e FTP_USER_HOME=/home/navigation-data -e FTP_MAX_CLIENTS=50 -e FTP_PASSIVE_PORTS=30000:30099 -v /home/ubuntu/navigation-data:/home/navigation-data stilliard/pure-ftpd
```
