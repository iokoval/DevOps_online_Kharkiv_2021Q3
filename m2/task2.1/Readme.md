## Task 2.1
### Hypervisors
1. I think, about first typeof hypervisors. I mean this srtucture (Hardware->Hypervisor->VMs)
2. First type of the most popular hypervisors (Hardware->Hypervisor->VMs) this type  more productive because it worksdirectly with hardware.(Hyper-V, KVM, ESXi.)  
3. Second type of the mos popular hypervisors (Hardware->OS->Hypervisor->VMs(VMware Workstation, Oracle Virtual Box, OpenVZ))
In this task we are work with configuration Virtual Box,  
I am use ububntu machine, secondly i have clone this machine and they have some network adapters  
1. Nat  
2. NatNetwork  
3. Internal network
4. Host Only  
5. Bridge Adapter
### Nat CONFIG (in NAT we have two different LANs)
I am use port forwading, because i need connect with ssh to two machines we have two Ip (10.0.2.15 - 10.0.2.16)  
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/ssh15.png  
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/ssh16.png
### NatNetwork Config
In this mode i use port forwarding too, but in this mode Vms can interact with each other, because they have general local area network.  
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/NatNetworkconfig.png  
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/NatNetworkconfig2.png
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/natsshub.png  
### Bridge adapter (in this mode, our Vms have Ip 192.168.31.x, because this Ip it is host lan)  
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/bridge.png
### Host-only(in this method we take one lan of VB 192.168.56.x)
This adpater we can see in settings, on the host machine. Setting-> Setting network adapter Ethernet->VirtualBox Host-only Ethernet Adapter
We can comminuicate with VMs from host and from host to Vms  
## Vagrant  
Firstly we use init command for initialize our folder and setup vagrant file in this folder  
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/vagrantinit.png
Secondly, we use vargrant up command for start our box,Then we can connect to our machine from host with SSH 
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/vagrantUp.png  
We can check date with command Date
link: https://github.com/iokoval/DevOps_online_Kharkiv_2021Q3/blob/master/m2/task2.1/image/vagrantdate.png
