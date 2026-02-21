1️⃣ VPC
A VPC has a CIDR block, which defines the range of IP addresses available for resources inside the VPC.

2️⃣ Now comes Subnets —
A subnet is a group of IP addresses within a VPC. It helps us divide the VPC into smaller logical networks.

🖊️ There are 2 types of subnets:
Public Subnet
Private Subnet

🖊️ They work using gateways:
Internet Gateway (IGW) → for internet access
NAT Gateway → for outbound internet access from private subnet

🖊️ Subnet CIDR block size must be between /16 and /28.

🖊️ Reserved IP Addresses in a Subnet
The first 4 IP addresses of every subnet are reserved and cannot be used.
Example:
Subnet → 192.168.10.0/24
192.168.10.0 → Network address
192.168.10.1 → VPC router interface
192.168.10.2 → DNS
192.168.10.3 → Reserved for future use

The last IP address is reserved for the broadcast address: 192.168.10.255

🔐 Subnet Configuration Rule
- A subnet cannot overlap with other subnets within the same VPC.
- Subnet allows IPv6 CIDR Block /56 but you can only use IPv6, No IPv4 addresses.
- Subnets can communicate with each other in same VPC automatically.
- Enable Auto-assign public IPv4/IPv6 IP address option, in addition to private address to get public IP address. 
  Where it is useful when a user wants to send an request to instance.



![alt text](image-2.png)