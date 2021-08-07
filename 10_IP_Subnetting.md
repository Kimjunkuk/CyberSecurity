IP address 
-Subnet Address
-1st host Address
-Lost Host Address
-Broadcast Address

Two Methods
-Binary Method
-Quick Method

### Typical Example

PC1: 192.168.10.18/(mask)24 <-> Router1

What IP address would rout1 be configured with if it is use the first IP address in the same subnet as PC1?

what brodcast address is use by PC1

What IP Address would Route1 be configured with if it is to use the last IP address in the smae subnet as PC1?'

What subnet is PC part of?

### Binary Rules!!
Network/Subnet address - Fill the host portion of an address with binary O's

Broadcast Address - Fill the host portion of an address with binary 1's

First host - Fill the host portion of an address with binary 0's except for the last bit which is set to binary1

Last host - fill the host portion of an address with binary 1's except for the last bit which is set to binary 0 


### 1Basic Example 

PC1: 192.168.10.18/(mask)24 or 192.168.10.18 with 255.255.255.0

>>> mask 24 means 24 bits in subnet mask

192.168.1.18 (Last 18 is the host portion if the address)

Subnet    = 192.168.1.000 000 00(8 binary 0's) = 192.168.1.0
1st Host  = 192.168.1.000 000 01 = 192.168.1.1
Last Host = 192.168.1.111 111 10 = 192.168.1.254
Broadcast = 192.168.1.111 111 11 = 192.168.1.255

Q1. To configured the first IP address in the same subnet as PC1?
A1. 192,.168.10.1/24 or 192.168.1.1 with 255.255.255.0


### 2Basic Example

PC1: 172.16.35.123/20 or 172.16.35.123 with 255.255.240.0

mask /20 - means that 20 bits of the 32 bit IP address are used for network / subnet and the remaining 12 bits are used as the host portion.
