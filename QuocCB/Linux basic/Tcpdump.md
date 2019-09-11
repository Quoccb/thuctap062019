### TCPDUMP
Tcpdump is a command line utility allows you to capture and analyze network traffic going through your system.
It is often use to troubleshoot network issues, as well as a security tool.

#### 1. Installation on Linux
Tcpdump is included with several Linux distributions, so chances are, you already have it installed.
Check if tcpdump is installed in your system with the following command:

>which tcpdump <br>
/usr/sbin/tcpdump

If tcpdump is not installed, you can install it but using the distribution's package manager. For example, on CentOS or Red Hat Enterprise Linux, like this:

>yum install -y tcpdump

Tcpdump requires libpcap, which is a library for network package capture. If it is not install, it will be automatically added as a dependency.

#### 2. Capturing packets with tcpdump.

To begin, use the command tcpdump -D to see which interface are availble for capture.
>tcpdump -D
<br>1.eth0
<br>2.nflog (Linux netfilter log (NFLOG) interface)
<br>3.nfqueue (Linux netfilter queue (NFQUEUE) interface)
<br>4.eth1
<br>5.usbmon1 (USB bus number 1)
<br>6.usbmon2 (USB bus number 2)
<br>7.any (Pseudo-device that captures on all interfaces)
<br>8.lo [Loopback]

In the example above, you can see all the interfaces availble in my machine.
The special interface *any* allows capturing in any active interface.
<br> Let's use it to start capturing some packages. Capture all package in any interface by running this command:

>tcpdump -i any

Tcpdump continues to capture packets until it receives an interupt signal. You can interupt capturing by pressing **Ctrl + C**. As you can see in this example, tcpdump captured more than 9000 packets.
In this case, since I am connected to this server using ssh, tcpdump captured all these packets. To limit the number of packets  captured and terminated tcpdump, use the -c option:
> tcpdump -i any -c

In this case, tcpdump stopped capturing automatically after capturing five packets.
This is useful in different scenarios—for instance, if you're troubleshooting connectivity and capturing a few initial packets is enough.
This is even more useful when we apply filters to capture specific packets (shown below).

By default, tcpdump resolves IP addresses and ports into names, as shown in the previous example.
When troubleshooting network issues, it is often easier to use the IP addresses and port numbers; disable name resolution by using the option -n and port resolution with -nn:
>tcpdump -i any -c5 -nn

As shown above, the capture output now displays the IP addresses and port numbers. This also prevents tcpdump from issuing DNS lookups, which helps to lower network traffic while troubleshooting network issues.

Now that you're able to capture network packets.
