# Network

# Internet Addresses

In order to communicate effectively, each computer in a network needs a distinguishing
name called an address. For the Internet this address is currently a 32-bit number
called the **Internet Protocol (IP)** address (although 128-bit addresses are being phased
in to accommodate the growth of the Internet). For technical reasons some computers
have more than one address, whereas other sets of computers, which use the Internet only
sporadically, may share a pool of addresses that are assigned on a temporary basis. Like
telephone numbers, IP addresses are divided into parts: one, the network ID, specifies the
local network to which a given computer belongs, and the other, the host ID, specifies the
particular computer.

An example of an IP address is 10001100 11000000 00100000 10001000, where the 32 bits have been divided into four groups of 8 for easier reading. To make the reading even easier, IP addresses are normally written as “dotted decimals,” in which each group of 8 bits is converted into a decimal number between 0 and 255. For instance, the IP address above converts into 140.192.32.136.

In order to accommodate the various sizes of the local networks connected through the
Internet, the network IDs are divided into several classes, the most important of which are called A, B, and C. In every class, a host ID may not consist of either all 0’s or all 1’s.

**Class A** network IDs are used for very large local networks. The left-most bit is set to 0, and the left-most 8 bits give the full network ID. The remaining 24 bits are used for individual host IDs. However, neither 00000000 nor 01111111 is allowed as a network ID
for a class A IP address.

![Class A](/images/network/ip_class_a.png)

**Class B** network IDs are used for medium to large local networks. The two left-most
bits are set to 10, and the left-most 16 bits give the full network ID. The remaining 16 bits are used for individual host IDs.

![Class B](/images/network/ip_class_b.png)

**Class C** network IDs are used for small local networks. The three left-most bits are set to 110, and the left-most 24 bits give the full network ID. The remaining 8 bits are used for individual host IDs.

![Class C](/images/network/ip_class_c.png)

### References:
Discrete mathematics with applications - Susanna S Epp