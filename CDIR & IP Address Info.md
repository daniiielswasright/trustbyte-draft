## iP Address (x.x.x.x)
IP addresses connect us ton the world.

there are two types of IPs
A iPv4 address is x.x.x.x. It has 4 octets and consists of 32 bits. There are approximity 4 billion IPv4s.

A iPv6 address is x.x.x.x.x.x.x.x. it has 8 ocetets and consists of 128 bits. There are 340 decillion iPv6s.

## CIDR (x.x.x.x/x)
A CIDR (Classless Inter Domain Routing) (x.x.x.x/x) consists of an IP address (x.x.x.x) and a prefix ( /x). 

Youll see them in firewall rules, VPN configs and blocklists. They are a method for representing a range of IP addresses effcently.
### Prefix Length
The prefix ( /x) indicates how many of the 32 bits are fixed or for the network.

example: 255.255.255.240/20
The Prefix is 20 which means 20 of those are fixed and 12 are for hosts.
### How Many IPs?
iPv4s are 32 bits. 

iPv4s are 32 bits. Subtract your prefix from the total amount of bits. 32-20=12.

So now 12 of those are for hosts (think, all the people in your neighborhoods IPs).

Hosts have two states: 0 or 1.

2^the number of hosts after substracting the fixed from the total number of bits (in this case 12) = total number of IPs in that range.

$2^12 or 2x2x2x2x2x2x2x2x2x2x2x2x2= 4096 

This means there are 4096 255.255.255.240