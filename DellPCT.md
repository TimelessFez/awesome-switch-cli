
serial console:
9600 baud, 8 data bits, 1 stop bit, no parity, no flow control

PowerConnect 3524, PowerConnect 3524P, PowerConnect 3548, PowerConnect 3548P, PowerConnect 5524, PowerConnect 5524P, PowerConnect 5548, PowerConnect 5548p, PowerConnect 6224, PowerConnect 6224F, PowerConnect 6224P, PowerConnect 6248 , PowerConnect 6248P, PowerConnect 7024, PowerConnect 7024F, PowerConnect 7024P, PowerConnect 7048, PowerConnect 7048P, PowerConnect 7048R, PowerConnect 8024, PowerConnect 8024F, PowerConnect 8100 Series, PowerConnect M6220, PowerConnect M6348, PowerConnect M8024, PowerConnect M8024-K
re: https://www.dell.com/support/kbdoc/en-us/000122285/how-to-configure-an-ip-address-on-dell-networking-powerconnect-switches

---

CLI syntax

command negation
```no```

display <option>
```show <command>```

display current configuration
```show running-config```

display start-up configuration
```show startup-config```

user exec mode
```
enable
console> 
```

privileged exec mode
```
console> configure
console# 
```

display available commands
```<command> ?```

int
```console(config)# interface gi1/0/1```

vlan
```console(config)# vlan <vlanid>```

user management
```username <user> password <passwd> level <1-15>```
```console(config)# username admin password password level 15```

assign ip
```console(config)# ip address A.B.C.D/X```

no ip
```console(config)# no ip dhcp```

hostname
```console(config)# hostname <hostname>```

ip route
```console(config)# ip route A.B.C.D/X```

vlan access mode
```
interface <int>
switchport mode access
switchport access vlan <vlanid>
```

vlan trunk mode
```
interface <int>
switchport mode trunk
switchport trunk allowed <vlanid>
```








