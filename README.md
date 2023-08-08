
# Subnetting Scenarios
</p>

This is a compliation of subnetting and binary practice exercises. 

#


**1. Enter the maximum number of valid subnets and usable hosts per subnet that you can get from the network 172.27.0.0 255.255.240.0**
   
Host: 4094   
Host per Subnet: 16

**Explanation:** The Subnet Mask: 255.255.240.0 or /20 was converted into binary as such 11111111.11111111.11110000.00000000 .   
There are twenty 1's that represent the Subnet and twelve 0's that represent the Host.  

The calculation for Subnets: 2^4 = 2x2x2x2 = 16 . The calculation for Hosts: 2^12 - 2 = 2x2x2x2x2x2x2x2x2x2x2x2 - 2 = 4096 -2 = 4094
<p align="center">
<img src="Exercise 1.png"/>   


**2. Enter the first valid host on the network 192.168.182.16/29**
   
First Host: 192.168.17   

**Explanation:** The Subnet is displayed as /29 and converted to binary looks like:   

Subnet Mask in decimal:   255.     255.     255.     248   
Subnet Mask in binary: 11111111.11111111.11111111.11111000 

I also converted the Network ID to binary as shown below: 

Network ID in decimal:   192.     16.      182.      16   
Network ID in binary:  11000000.10101000.10110110.00010000   

From converting both the Network ID and Subnet Mask to binary I'm able to see the full representation of 1's and 0's in each octect. There are twenty-nine 1's that represent the Subnet and four 0's that represent the Host. Since we're only going to be dealing with the last octect, and working with the first 5 bits, we can simply intermix the 1's and 0's until we get 16 in binary format as such:   x.x.x.11111000 > x.x.x.00001000 > x.x.x.00010000 > etc. or we can use a binary chart, or use the binary conversation that was done for the Network ID up above. 

Subnet Mask:           11111111.11111111.11111111.00010000   

The calculation for Subnets: 2^5 = 2x2x2x2x2 = 32 . The calculation for Hosts: 2^3 - 2 = 2x2x2 - 2 = 8 -2 = 6   

Last Host: 192.168.182.22   
Broadcast: 192.168.182.23   
Next Subnet: 192.168.182.24
<p align="center">
<img src="Exercise 2.png"/>   


**3. Enter the subnet the host 172.19.160.163  255.255.255.248 belongs to**

Subnet: 172.19.160.160     

**Explanation:** The Subnet Mask is 255.255.255.248 and converted to binary looks like: x.x.x.11111000 . This already lets me know that we'll be working with only the last octect. Let's convert the Host. We should get something along the lines of: x.x.x.10100011 . Looking at the Subnet Mask as /29 leaves three 0's for the Host.   

The calculation for Subnets: 2^5 = 2x2x2x2x2 = 32 . The calculation for Hosts: 2^3 - 2 = 2x2x2 - 2 = 8 -2 = 6   

Since we're only working with 5 bits in the last octect, lets start intermixing the 0's and 1's beginning with: x.x.x.0000100 = x.x.x.8 . As you can see, this is the subnet 1 of 32 and also means that we will be working in multiples of 8. We need to find a number that is divisible by 8 and closest to 163.   

8x12 = 96 > 8x18 = 144 > 8x20 = 160

Convert 160 to binary as such: 10100000 

Network ID: 172.19.160.160   
First Host: 172.19.160.161   
Last Host:  172.19.160.166   
Broascast: 172.19.160.167   
<p align="center">
<img src="Exercise 3.png"/>   

   
**4. What is the Subnet Mask corresponding to a shorthand of /19?**

   Subnet Mask: 255.255.224.0

   **Explanation:** There are 32 bits in IPv4 binary and /19 let us know that there are nineteen 1's so there must be thirteen 0's.
   In binary, it should look something like: 11111111.11111111.11100000.00000 and converted to decimal will be 255.255.224.0 .   
<p align="center">
<img src="Exercise 4.png"/>   


#
If your interested in trying some out yourself, head over to Subnetting.net (www.subnetting.net) .


























