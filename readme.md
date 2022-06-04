# Company Networking Project

### Topology:
![image]([https://user-images.githubusercontent.com/81536161/172024143-297b7ece-9c95-4695-a352-1a7198e641f4.png](https://github.com/saadabuzaid/Company-network-configuration/blob/main/Network-Assignment/Topology.png))


### Scenario:
You are to configure the routing and switching for part of the company network shown in Figure 1, in particular 
the wide area networking routing (including Branch and Data Centre gateways) and the switching for the Data 
Centre. Some of the systems are pre-configured. You must complete this assignment using Cisco Packet Tracer 
version 8.0.1 (or later). Some of the assignment (e.g some IP addresses) is specified exactly, but other parts you 
will have to make sensible design choices based on the scenario as described here and the methods you have learnt 
from the lab tasks
he scenario only shows part of the company network, you are to assume that the actual network is very large with 
many branches (not shown). All the branches connect to the WAN and access the Internet through WAN2. 
 
There is a placeholder for the Internet (InternetServer) accessed through an Internet Service Provider. The router 
ISP is a placeholder for the Internet Service Providers network. ISP provides one public IP address for the whole 
company to use (202.202.202.2 on WAN2). The company hosts should be able to access Web servers in the 
Internet, however, it is not necessary for the Internet to access any hosts in the company network (and in fact the 
ACLs you will implement will block this traffic). 
 
The data centre needs to have a highly-reliable design and you will note that it has two systems (routers, switches 
and servers) so that it can cope with a single failure. PC2 is a placeholder for management terminals and only one 
is shown. There are only two servers and access switches (DS3 and DS4) shown although you should assume there 
are many more systems to be connected to DS3 and DS4 in the future and not shown. There are no clients or 
servers directly connected to the distribution layer switches (DS1 and DS2). You should configure the networking 
so that if there is a failure of any single switch, or either router DSR1 or DSR2, then any host will still have 
network connectivity without any need for manual intervention. You will need to look back at CE231 content to 
remind you how to allow multiple routers to act as a gateway. (You should assume that DSGW is a highly-fault 
tolerant router with dual systems and connectivity that are not shown.) 
 
On the Access switches (DS3, DS4), the lower half of the ports (fa0/1-12) are to be allocated to VLAN S, the 
upper two of the ports (fa0/23-24) are to be allocated to VLAN C. VLAN M is for managing the switches and 
routers. Other ports are free. All ports not actually connected to a device should be shutdown. VLANs and switch 
port configuration were covered in CE231. 
 
The company network manager has specified that you use OSPF for routing and to ensure it is configured to route 
traffic across the whole network and has basic security by limiting where OSPF traffic can be sent/received from to 
only essential interfaces. 
 
For the OSPF extension work: 
 
• OSPF should be reconfigured to be multi-area, the ABRs must be BR1 and DSGW; 
• network addresses (routes) between areas must be summarised using a single address that is the smallest
possible summary address to encompass the networks you have been allocated (you are to assume 
addresses in the summary not used in your scenario are available for expansion at a future date). You will 
need to find out about this as it is not covered in the Cisco courseware; 
• OSPF costs must be correct to allow routing over the fastest path where this is relevant. As the “auto-cost 
reference bandwidth” command does not work in Packet Tracer link costs must be set manually. 
 
Note that this extension work will require you to look carefully at the multi-area OSPF Packet Tracer Lab example 
and to carry out your own research in order to complete it. It is not covered by the Cisco courseware in any depth. 
