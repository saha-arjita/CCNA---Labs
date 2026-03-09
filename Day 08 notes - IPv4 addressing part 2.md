# Day-08: IPv4 Addressing Part 2 (Layer 3 - Network)

Class C : 192.168.1.0/24 (host portion all 0s = network address) → 192.168.1.255/24 (host portion all 1s = broadcast address)
Host portion = 2^8 = 256
Maximum hosts per network = 2^8 -2 = 254
192.168.1.1/24 = first usable address
192.168.1.254/24 = last usable address

Class B: 172.16.0.0/16(host portion all 0s = network address)  → 172.16.255.255/16 (host portion all 1s = broadcast address)
Host portion = 2^16 = 65,536
Maximum hosts per network = 2^16 -2 = 65,534
172.16.0.1/16 = first usable address
172.16.255.254/16 = last usable address
Class A: 10.0.0.0/8 (host portion all 0s = network address) → 10.255.255.255/8 (host portion all 1s = broadcast address)
Host portion = 2^24 = 16,777,216
Maximum hosts per network = 2^24 -2 = 16,777,214  ( 2^n-2 )
10.0.0.1/8 = first usable address
10.255.255.254/8 = last usable address

IP Addressing for router
— status of each interface – show ip interface brief
Conf t
Interface gigabitethernet0/0 or in g0/0
Ip address 10.255.255.254 255.0.0.0
No shutdown
description  ##sw1## 

show interface g0/0 = gives the details of layer 1,2
show interfaces description

Status - administratively down =  interface has been disabled with the shutdown command
This is the default status of cisco router interfaces
Cisco switch interfaces are not administratively down by default
