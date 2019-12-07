### Filter by uri in wireshark. Tshark example 





 

```shell
nohup sudo tshark -i eth0 -Y 'http.request.uri contains "/balance/"' -Tfields -e http.request.method -e http.request.full_uri -e http.file_data > balance.out 2>&1 &
```
