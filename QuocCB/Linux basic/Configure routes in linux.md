### Configure Static routes in Debian or RHE Linux
**Display current Routing table Using ip command**
By using the *ip route* command you can set up and view static route.
For example, to display the current Routing table you can type the command
>\# ip route show

or

>\# route -n

you can add static route using following command:

> ip route add {NETWORK} via {IP} dev {DEVICE}

For example, Network 192.168.55.0/24 availble via 192.168.1.254:
> ip route add 192.168.55.0 via 192.168.1.254 dev eth1

Alternatively, you can use the old good route command too:
 >\# route add -net 192.168.55.0 netmask 255.255.255.0 gw 192.168.1.254 dev eth1

 **Linux permanant routes**

 The drowback of 'ip' or 'route' command is that when Linux system reboots it will
 forget static routes.

 You need to open */etc/sysconfig/network-scripts/route-eht0* file to difine the static routes for eth0 interface:

 >\# nano /etc/sysconfig/network-scripts/route-eth0

 Sample output:

 > GATEWAY0=192.168.1.254
 <br>NETMASK0=255.255.255.0
 <br>ADDRESS0=192.168.55.0
 <br>
 <br>GATEWAY1=10.164.234.112
 <br>NETMASK1=255.255.255.240
 <br>ADDRESS1=10.164.234.132

 On a modern version of CentOS 7 or RHEL 7, you need to create a file named /etc/sysconfig/network-scripts/route-eth0 and update as follows:

 >\# vi /etc/sysconfig/network-scripts/route-eth0

 add a permanent static route:

 > 172.16.1.0/24 via 10.10.8.254 dev eth0

 
