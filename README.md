# CLI command translations for Cisco, Huawei, and Aruba switches
## General configuration
| Cisco                | Huawei                         | Aruba               | FS |
|----------------------|--------------------------------|---------------------|----|
| ping                 | ping                           | ping                |    |
| traceroute           | tracert                        |                     |    |
| no <command>         | undo <command>                 | no <command>        |    |
| show                 | display                        |                     |    |
| show interface       | display interface              |                     |    |
| write terminal (show running-config)  | display current-configuration  | show running-config |    |
| show startup-config  | display startup                | show startup-config |    |
| enable               | super (default: 3)             | enable              |    |
| conf t               | system-view                    | config              |    |
| exit                 | quit                           | exit                |    |
| end                  | return                         |                     |    |
| disable              | super 0 (privilege level: 0-3) | disable             |    |
| clock                | clock                          | set clock           |    |
| copy running-config  | save safely                    | copy running-config |    |
| write mem            | save                           | write m             |    |
| reload               | reboot                         |   |    |
| boot                 | bootrom                        | boot      |    |
| shutdown             | shutdown                       | shutdown  |    |

## User Management / Create User
### Cisco

### Huawei
- **Create user with plaintext password**

  - *"This command should be entered in interactive mode. Directly entering a plaintext password without being in interactive mode poses potential security risks."*

    ```local-user <username> password <password>```

- **Create user with ciphertext password**

  - ```local-user <username> password ( cipher | irreversible-cipher ) <password>```

- **Configure access type for local user (user access permission)**

  - *By default, all access types are disabled for a local user.*

    ```local-user <username> service-type ( 8021x | api | ftp | http | ppp | ssh | telnet | terminal | web | x25-pad ) *```

- **Configure user privilege level**

  - *Privilege level ranges from 0 (lowest) to 15 (highest). Default: 0*
 
    ```local-user <username> privilege level <level>```

- **Delete user**

  - *Removes the local user*
 
    ```undo local-user <user>```

### Aruba



### FS


---

## [Enable voice VLAN]

### Huawei
```
<HUAWEI> system-view
[HUAWEI] interface gigabitethernet 0/0/1
[HUAWEI-GigabitEthernet0/0/1] voice-vlan enable
```

### Aruba
```
Switch> config
Switch# vlan 10
Switch(vlan-10)# voice
```

---

---

* This page will be updated over time.
