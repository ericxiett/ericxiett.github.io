# Set static routes in Ubuntu Server

``` bash
$ vim /etc/network/interfaces
auto eth0
iface eth0 inet static
    address 192.168.1.2
    netmask 255.255.255.0
    up route add -net 192.168.0.0 netmask 255.255.0.0 gw 192.168.1.1
    up route add -net 172.16.0.0 netmask 255.240.0.0 gw 192.168.1.1
```

