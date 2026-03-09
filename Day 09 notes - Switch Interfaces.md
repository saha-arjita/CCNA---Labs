# Day-09:  Switch Interfaces

Router interfaces have the shutdown command applied by default
 will be the administratively down/down state by default

Switch interfaces do not have the shutdown command applied by default 
Will be in the up/up state if connected to another device or
In the down/down state if not connected to another device
 
Show interfaces status
Int f0/1
Speed ?
Duplex ?
Description ##to R1##
Interface range f0/5 - 12
Description ## not in use ##
Shutdown
Int range f0/5 - 6 , f0/9 - 12
No shut 

Full Duplex = indicates the device is capable of both sending and receiving data at the same time . It does not have to wait. The device attached to the switch works as a full duplex.

Half - duplex = the device  can not send and receive data at the same time if it is receiving a frame it must wait before sending  a frame. Almost nowhere to be used.
In the Hub half duplex is used. When a hub receives two frames at the same time and tries to transmit them, a collision occurs because the network medium is shared.  To deal with the collisions ethernet devices use a mechanism 
CSMA/CD - Carrier senses multiple access with collision detection.
Before sending frames, devices listen to the collision domain until they detect that other devices are not sending
If a collision does occur, the device sends a jamming signal to inform the other devices that a collision happened.
Each device will wait a random period of time before sending its own frame.


Interfaces that can run at different speeds(E=10/F=10/100/G=10/100/1000) have default settings of speed auto and duplex auto.
Interfaces ‘advertise’ their capabilities to the neighboring device, and they negotiate the best speed and duplex settings they are both capable of.

What if auto negotiation is disabled on the device connected to the switch-
The switch will try to sense the speed that the other device is operating at, if it fails to sense the speed, it will use the slowest supported speed (10 mbps on a 10/100/1000 interface)
If the speed is 10 or 100 mbps, the switch will use half duplex if the speed is 1000 mbps or greater use full duplex.(cause collision result poor network performance ) , always should use autonegotiation on all devices in the network.

show interface f0/0
Runts : frames that are smaller than the minimum frame size (64 bytes)
Giants: frames that are larger than the maximum frame size (1518 bytes)
CRC: frames that failed the CRC Check (in the ethernet FCS trailer)
Frame: frames that have an incorrect format due to an error
Input error: total of various counters, such as the above four
Output errors : frames the switch tried to send, but failed due to an error.
