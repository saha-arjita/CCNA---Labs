 # Day-07:  IPv4 Addressing ( Layer 3 - Network )

Provides connectivity between end hosts on different networks
Provides logical addressing (IP address)
Provides path selection between source and destination 
Routers operate at layer 3

IPv4 address 32 bits (4 bytes) in length

128       64       32       16      8       4        2       1

Decimal to binary & binary to decimal – 
00111111 00111000 11100111 00010011
63.56.231.19

11110011 01111111 01100010 00000001
243.127.98.1

01101111 00000110 01011001 11000111
111.6.89.199

11001111 11000110 00101111 01001100
207.198.47.76

01100100 11001001 00100001 11111101
100.201.33.253

88.46.90.91
01011000 00101110 01011010 01011011

221.234.246.163
11011101 11101010 11110110 10100011


192.168.2.1/24 = 24 bits represent the network portion of the address remain 8 bits for the host

IPv4 Address Classes
| Class | Prefix | Netmask        | First Octet Pattern | First Octet Numeric Range |
|------|--------|---------------|---------------------|---------------------------|
| A    | /8     | 255.0.0.0     | 0xxxxxxx            | 0–127 (usable 1–126)      |
| B    | /16    | 255.255.0.0   | 10xxxxxx            | 128–191                   |
| C    | /24    | 255.255.255.0 | 110xxxxx            | 192–223                   |
| D    | —      | —             | 1110xxxx            | 224–239 (reserved Multicast)       |
| E    | —      | —             | 1111xxxx            | 240–255 (reserved Experimental)    |


- Address range 127.0.0.0 - 127.255.255.255
- Used to test the network stack (think OSI, TCP/IP model) on the local device (loopback addresses) - 127 range reserved

Host portion of the address is all 0’s = Network address
Host portion of the address is all 1’s = broadcast address
