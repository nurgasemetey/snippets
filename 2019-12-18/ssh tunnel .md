### ssh tunnel 


[How To Route Web Traffic Securely Without a VPN Using a SOCKS Tunnel | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-route-web-traffic-securely-without-a-vpn-using-a-socks-tunnel "How To Route Web Traffic Securely Without a VPN Using a SOCKS Tunnel | DigitalOcean")




```shell
ssh -D 8123 -f -C -q -N sammy@example.com

```
