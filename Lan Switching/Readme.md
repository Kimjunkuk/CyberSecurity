# Commands

### Viewing Ethernet Controller Statistics
S2# show controllers ethernet-controller FastEthernet 0/1

### User mode
Switch> 

### Privilege mode
Switch> enable
Switch#

### Full configuration mode
Switch# conf t
Enter configuration commands, one per line. End with CNTL/Z.
Switch(config)#

### Interface speed control
speed(Mbps)
Switch# conf t
Switch(conf)# interface FastEthernet 1/0/1
Switch(config-if)# speed 10

### Configuration mode Exit
Switch(config-if)# exit
Switch(config)# exit
Switch#

### Switch reset
Switch# del vlan.dat
Delete filename [vlan.dat]?
Delete flash:vlan.dat? [confirm]
Switch# erase start
Switch# reload

System configuration has been modified. Save?[yes/no]: no
Proceed with reload? [confirm]

Would you like to enter the initial configuration dialog? [yes/no]: no + Hit few more enter key

Press RETURN to get started!

00:07:06: %LINK-5-CHANGED: Interface Vlan1
