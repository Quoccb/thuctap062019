### About Network Interface

Each physical and virtual network device on an CentOS has an associated configuration file named *ifcfg-"interface"* in the /etc/sysconfig/network-scripts
directory, where *"interface"* is the name off interface. For example:

>\# cd /etc/sysconfig/network-scripts
<br># ls ifcfg-*
<br> ifcfg-l0  ifcfg-eth0    ifcfg-eth1

In this example, *ifcfg-eth0* and *ifcfg-eth1* are two configuration files for Network Interfaces.
*ifcfg-i0* is default  file for loopback interface. The system reading the network configuration files at boot time to configure the network interfaces.
The following are sample entries from an *ifcfg-eth0* file for a network interface that obtains its IP Address using the DHCP.

>DEVICE="eth0"<br>
ONBOOT=yes<br>
USERCTL.............<br>
TYPE=Ethernet<br>
BOOTPROTO=dhcp <br>
DEFROUTE=yes<br>
IPV4_FAILURE_FATAL=yes<br>
IPV6INIT=no<br>
NAME="System eth0"................<br>
HWADDR= "Hardware address"<br>
PEERDNS=yes<br>
PEERROUTES=yes

If the interface is configured with a static IP Address, the file contains entries such as the following
>DEVICE=etho<br>
NM_CONTROLLED=yes<br>
ONBOOT=yes<br>
USERCTL=no.........<br>
TYPE=Ethernet<br>
BOOTPROTO=none <br>
DEFROUTE=yes<br>
IPV4_FAILURE_FATAL=yes<br>
IPV6INIT=no<br>
NAME="System eth0"<br>
HWADDR= \<Hardware Address><br>
IPADDR= \<IPV4 Address><br>
NETMASK= <br>
BROADCAST= \<broadcast address><br>
PEERDNS=yes<br>
PEERROUTES=yes<br>

The following parameters are typically used in interface configuration files:
<br>
*BOOTPROTO*: How the interface obtains its IP address.
- **bootp**: Bootstrap Protocol (BOOTP)
- **dhcp**: Dynamic Host Configuration Protocol (DHCP).
- **none**: Statically configured IP address

**BROADCAST**: IPv4 broadcast Address

**DEFROUTE**: Whether this interface is the default route

**DEVICE**: Name of the physical network interface DEVICE

**HWADDR**: MAC address of an Ethernet device

**IPADDR**: IPV4 address of the interface.

**IPV4_FAILURE_FATAL**: Whether the device is disabled if IPv4 configuration fails

**IPV6ADDR**: IPV6 address of the interface in CIDR notation.

**IPV6INIT**: Whether to enable IPv6 for interface

**MASTER**: Specifies the name of the master bonded interface, of which this interface is slave

**Name**: Name of the interface as displayed in the Network Connections GUI.

**NETMASK**: IPv4 network mask of the interface.

**NETWORK**: IPv4 address of the network.

**NM_CONTROLLED**: Whether the network interface is controlled by the network management deamon.Networkmamager.

**ONBOOT**: Whether the interface is activated in the boot time

**PEERDNS**: Whether the */etc/resolv.conf* file used for DNS resolution contains the information obtained from the DHCP server.

**PEERROUTES**: Whether the information for the routing table entry that defines the default gateway for the interface is obtained from the DHCP server.

**SLAVE**: Specifies that this interface is a component of a bonded interface.

**TYPE**: Interface type

**USERCTL**: Whether users other than *root* can controll the state of this interface

**UUID**: Universally unique identifier for the network interface device.
