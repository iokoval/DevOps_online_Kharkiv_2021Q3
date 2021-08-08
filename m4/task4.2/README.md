### TASK 4.2(first exersise)
In this exersise we are used one router and two switches.  
We did new settings on router for DHCP-server(network 192.168.1.0/24)  
We have two buildings in this exersise. 
Beetwen buildings distance == 100 meters(cooper cable, no fiber)
## Settings for Router(DHCP)  
In conf t.  
int gi 0/0
ip address 192.168.1.0 255.255.255.0  
exit  
ip dhcp pool DHCP 
network 192.168.1.0 255.255.255.0 
default-router 192.168.1.1  
dns-server 1.1.1.1, 8.8.8.8
exit  
ip dhcp excluded-address 192.168.1.1 //this is string for exclude ip address 192.168.1.1,  
because he use on our router.  
### TASK4.2 (Second exersise)
In this task we have one build with four floor and two groups.  
First group have 3 computers.
Second group have 5 computers.  
In this build we have corporate lan and 8 subnetworks.  
FIRST GROUP    
1. 192.168.2.0/29(VLAN2 - BUH)  
2. 192.168.3.0/29(VLAN3 - SYS)  
3. 192.168.4.0/29(VLAN4 - ADMINS)  
4. 192.168.5.0/29(VLAN5 - HEADS)
SECOND GROUP    
5. 192.168.6.0/29(VLAN6 - PHYSLICA)  
6. 192.168.7.0/29(VLAN7 - YRLICA)  
7. 192.168.8.0/29(VLAN8 - MARKETING)  
8. 192.168.9.0/29(VLAN9 - SALES)  
9. 192.168.10.1/30(VLAN10 - DHCP)  
SERVERS  
1. DHCP-server (192.168.10.2static ip, with 9 pools for vlans)  

I made new settings on two swithes for vlans, example:  
int range fa0/1-5  
switchport mode access  
switchport access vlan 6  
And trunk port on switches:  
int gi0/1  
switchport mode trunk  
switchport trunk allowed vlan 2-10  

