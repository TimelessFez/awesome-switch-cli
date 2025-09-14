## CLI command translation
\**This page will be updated over time.*


## General configuration
# Network Switch Command Cheat Sheet
> Cisco | Huawei | Aruba | FS

---

## 1. Basic Connectivity
| Task / Function        | Cisco          | Huawei           | Aruba          | FS |
|------------------------|---------------|-----------------|----------------|----|
| Ping                   | `ping <ip>`   | `ping <ip>`     | `ping <ip>`    | `ping <ip>` |
| Traceroute             | `traceroute <ip>` | `tracert <ip>` | `traceroute <ip>` | `traceroute <ip>` |
| Show device info       | `show version` | `display version` | `show version` | `show version` |
| Set clock              | `clock <command>` | `clock <command>` | `set clock` | `clock set datetime HH:MM:SS MONTH DAY YEAR` |

---

## 2. Privilege & Configuration Mode
| Task / Function              | Cisco          | Huawei           | Aruba          | FS |
|-------------------------------|---------------|-----------------|----------------|----|
| Enter privileged mode        | `enable`       | `super` (default: 3) | `enable`       | `enable` |
| Disable privileged mode      | `disable`      | `super 0` (level 0–3) | `disable`     | `disable` |
| Enter configuration mode     | `configure terminal` | `system-view` | `configure terminal` | `configure terminal` |
| Exit current mode            | `exit`         | `quit`          | `exit`          | `exit` |
| Return to previous mode      | `end`          | `return`        | `exit`          | `exit` |

---

## 3. Interface Commands
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS |
|-------------------------------|-----------------------|------------------|--------------------|----|
| Show interface info           | `show interface`       | `display interface` | `show interface`  | `show interface` |
| Assign IP to interface        | `interface <int>` <br>`ip address <ip> <mask>` | `interface <int>` <br>`ip address <ip> <mask>` | `interface <int>` <br>`ip address <ip> <mask>` | `interface <int>` <br>`ip address <ip> <mask>` |
| Enable interface              | `no shutdown`          | `undo shutdown`   | `no shutdown`       | `no shutdown` |
| Disable interface             | `shutdown`             | `shutdown`        | `shutdown`          | `shutdown` |
| Interface description         | `description <text>`   | `description <text>` | `description <text>` | `description <text>` |

---

## 4. VLAN Commands
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS |
|-------------------------------|-----------------------|------------------|--------------------|----|
| Create / configure VLAN       | `vlan <id>`           | `vlan <id>`       | `vlan <id>`         | `vlan <id>` |
| Show VLANs                     | `show vlan`           | `display vlan`    | `show vlan`         | `show vlan` |
| Show MAC table                 | `show mac address-table` | `display mac-address` | `show mac-address-table` | `show mac-address-table` |
| Port security / sticky MAC     | `switchport port-security` | `port-security`  | `switchport port-security` | `port-security` |

---

## 5. Configuration Save & Reload
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS |
|-------------------------------|-----------------------|------------------|--------------------|----|
| Save running config           | `copy running-config`  | `save safely`     | `copy running-config` | `copy running-config` |
| Save config to memory         | `write memory` (`wr mem`) | `save`           | `write memory` (`write m`) | `write memory` |
| Reload / reboot device        | `reload`               | `reboot`          | `reload`           | `reload` |
| Boot commands                 | `boot`                 | `bootrom`         | `boot`             | `boot` |

---

## 6. Misc.
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS |
|-------------------------------|-----------------------|------------------|--------------------|----|
| Negate command                | `no <command>`        | `undo <command>`  | `no <command>`     | `no <command>` |
| Show spanning tree            | `show spanning-tree`  | `display stp`     | `show spanning-tree` | `show spanning-tree` |

## References
- https://dl.dell.com/manuals/all-products/esuprt_ser_stor_net/esuprt_networking/networking-n1100-series_users-guide_en-us.pdf
- https://www.mcwireless.co.uk/post/basic-guide-to-dell-vs-cisco-commands
- https://dl.dell.com/manuals/all-products/esuprt_ser_stor_net/esuprt_pedge_srvr_ethnt_nic/poweredge-mseries-blademultipack_white%20papers53_en-us.pdf
- https://www.dell.com/support/kbdoc/en-us/000120225/basic-command-line-interface-on-dell-networking-powerconnect-2800-model-switches

---

\**This page will be updated over time.*
