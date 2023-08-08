# Subnetting Scenarios

In this tutorial is a compliation of subnetting and binary problems. 
#


1. Enter the maximum number of valid subnets and usable hosts per subnet that you can get from the network 172.27.0.0 255.255.240.0
   
Host: 4094   
Host per Subnet: 16

Explanation: The Subnet Mask: 255.255.240.0 or /20 was converted into binary as such 11111111.11111111.11110000.00000000 .   
There are twenty 1's that represent the Subnet and twelve 0's that represent the Host.   
The calculation for Subnets: 2^4 = 2*2*2*2 = 16 . The calculation for Hosts: 2^12 - 2 = 2*2*2*2*2*2*2*2*2*2*2*2 - 2 = 8 -2 = 6 

2. Enter the first valid host on the network 192.168.182.16/29
   
First Host: 192.168.17   

Explanation: 
