### Parse csv in shell 





 

```shell
while IFS=, read -r modbus_address ip
do
    echo "UPDATE camera SET MODBUSS_ADDRESS = $modbus_address WHERE CAMERA_IP = \"$ip\";"
done < buruncuk.csv
```
