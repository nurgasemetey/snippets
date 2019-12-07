###  Bluetooth LE scan as non root


[Bluetooth LE scan as non root? - Unix &amp; Linux Stack Exchange](https://unix.stackexchange.com/questions/96106/bluetooth-le-scan-as-non-root "Bluetooth LE scan as non root? - Unix &amp; Linux Stack Exchange")




```shell
The Bluetooth protocol stack for Linux checks two capabilities. Capabilities are a not yet common system to manage some privileges. They could be handled by a PAM module or via extended file attributes. (see http://lxr.free-electrons.com/source/net/bluetooth/hci_sock.c#L619)

 $> sudo apt-get install libcap2-bin
installs linux capabilities manipulation tools.

 $> sudo setcap 'cap_net_raw,cap_net_admin+eip' `which hcitool`
sets the missing capabilities on the executable quite like the setuid bit.

 $> getcap !$
 getcap `which hcitool`
 /usr/bin/hcitool = cap_net_admin,cap_net_raw+eip

```

