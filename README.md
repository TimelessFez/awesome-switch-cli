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

https:/github.com/TimelessFez/switch-config/Cisco.md

### Aruba

### FS

---

### Aruba
```
Switch> config
Switch# vlan 10
Switch(vlan-10)# voice
```

---

---

* This page will be updated over time.
