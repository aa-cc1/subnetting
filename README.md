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

Explanation: The Subnet is displayed as /29 and converted to binary looks like:   

Subnet Mask in decimal:   255.     255.     255.     248   
Subnet Mask in binary: 11111111.11111111.11111111.11111000 

I also converted the Network ID to binary as shown below: 

Network ID in decimal:   192.     16.      182.      16   
Network ID in binary:  11000000.10101000.10110110.00010000   

From converting both the Network ID and Subnet Mask to binary I'm able to see the full representation of 1's and 0's in each octect. There are twenty-nine 1's that represent the Subnet and four 0's that represent the Host. Since we're only going to be dealing with the last octect, and working with the first 5 bits, we can simply intermix the 1's and 0's until we get 16 in binary format as such:   x.x.x.11111000 -> x.x.x.00001000 -> x.x.x.00010000 -> etc. or we can use a binary chart, or use the binary conversation that was done for the Network ID up above. 

Subnet Mask:           11111111.11111111.11111111.00010000   

The calculation for Subnets: 2^5 = 2*2*2*2*2 = 32 . The calculation for Hosts: 2^3 - 2 = 2*2*2 - 2 = 8 -2 = 6   
Last Host: 192.168.182.22   
Broadcast: 192.168.182.23   
Next Subnet: 192.168.182.24


 

3. Enter the subnet the host 172.19.160.163 255.255.255.248 belongs to

Subnet:   
Host:   

Explanation: 
