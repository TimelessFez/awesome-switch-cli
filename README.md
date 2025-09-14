# Awesome Switch CLI
Multi-vendor network switch CLI made simple — saving your sanity, one `no shutdown` at a time! 🤓

---

## 1. Basic Connectivity
| Task / Function        | Cisco          | Huawei           | Aruba          | FS | HP (ProCurve) | Dell (PowerConnect) |
|------------------------|---------------|-----------------|----------------|----|---------------|-------------------|
| Ping                   | `ping <ip>`   | `ping <ip>`     | `ping <ip>`    | `ping <ip>` | `ping <ip>` | `ping <ip>` |
| Traceroute             | `traceroute <ip>` | `tracert <ip>` <br> /`traceroute <ip>` | `traceroute <ip>` | `traceroute <ip>` | `traceroute <ip>` | `traceroute <ip>` |
| Show device info       | `show version` | `display version` | `show version` | `show version` | `show version` | `show version` |
| Set clock              | `clock <command>` | `clock <command>` | `set clock` | `clock set datetime HH:MM:SS MONTH DAY YEAR` | `clock datetime <HH:MM:SS> <MM/DD/YYYY>` | `clock set <HH:MM:SS> <MM/DD/YYYY>` |

---

## 2. Privilege & Configuration Mode
| Task / Function              | Cisco          | Huawei           | Aruba          | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|---------------|-----------------|----------------|----|---------------|-------------------|
| Enter privileged mode        | `enable`       | `super` (default: 3) | `enable`       | `enable` | `enable` | `enable` |
| Disable privileged mode      | `disable`      | `super 0` (level 0-3) | `disable`     | `disable` | `disable` | `disable` |
| Enter configuration mode     | `configure terminal` | `system-view` | `configure terminal` | `configure terminal` | `configure` | `configure` |
| Exit current mode            | `exit`         | `quit`          | `exit` (back once) / `end` (back to exec mode)          | `exit` | `exit` | `exit` |
| Return to previous mode      | `end`          | `return`        | `exit`          | `exit` | `exit` | `end` |

---

## 3. Interface Commands
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Show interface info           | `show interface`       | `display interface` | `show interface`  | `show interface` | `show interfaces` | `show interfaces` |
| Assign IP to interface        | `interface <int>` <br>`ip address <ip> <mask>` | `interface <int>` <br>`ip address <ip> <mask>` | `interface <int>` <br>`ip address <ip> <mask>` | `interface <int>` <br>`ip address <ip> <mask>` | `interface <int>` <br>`ip address <ip> <mask>` | `interface vlan <id>` <br>`ip address <ip> <mask>` |
| Enable interface              | `no shutdown`          | `undo shutdown`   | `no shutdown`       | `no shutdown` | `no shutdown` | `no shutdown` |
| Disable interface             | `shutdown`             | `shutdown`        | `shutdown`          | `shutdown` | `shutdown` | `shutdown` |
| Interface description         | `description <text>`   | `description <text>` | `description <text>` | `description <text>` | `description <text>` | `description <text>` |

---

## 4. VLAN Commands
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Create / configure VLAN       | `vlan <id>`           | `vlan <id>`       | `vlan <id>`         | `vlan <id>` | `vlan <id>` | `vlan <id>` |
| Show VLANs                     | `show vlan`           | `display vlan`    | `show vlan`         | `show vlan` | `show vlan` | `show vlan` |
| Show MAC table                 | `show mac address-table` | `display mac-address` | `show mac-address-table` | `show mac-address-table` | `show mac-address` | `show mac-address-table` |
| Port security / sticky MAC     | `switchport port-security` | `port-security`  | `switchport port-security` | `port-security` | `mac-address-table secure` | `port-security` |

---

## 5. Configuration Save & Reboot
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Save running config           | `copy running-config`  | `save safely`     | `copy running-config` | `copy running-config` | `write memory` | `copy running-config startup-config` |
| Save config to memory         | `write memory` (`wr mem`) | `save`           | `write memory` (`write m`) | `write memory` | `write memory` | `write memory` |
| Reboot                        | `reload`               | `reboot`          | `reload`           | `reload` | `boot system` | `reload` |
| Boot commands                 | `boot`                 | `bootrom`         | `boot`             | `boot` | `boot` | `boot` |

---

## 6. Misc.
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Negate / undo                 | `no <command>`        | `undo <command>`  | `no <command>`     | `no <command>` | `no <command>` | `no <command>` |
| Show spanning tree            | `show spanning-tree`  | `display stp`     | `show spanning-tree` | `show spanning-tree` | `show spanning-tree` | `show spanning-tree` |

---

## 7. Routing & Layer 3
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Show IP route                  | `show ip route`        | `display ip routing-table` | `show ip route`      | `show ip route` | `show ip route` | `show ip route` |
| Configure static route         | `ip route <dest> <mask> <next-hop>` | `ip route-static <dest> <mask> <next-hop>` | `ip route <dest> <mask> <next-hop>` | `ip route <dest> <mask> <next-hop>` | `ip route <dest> <mask> <gateway>` | `ip route <dest> <mask> <next-hop>` |
| Enable routing                 | `ip routing`           | `ip routing enable` | `ip routing`         | `ip routing` | `ip routing` | `ip routing` |
| Show ARP table                 | `show arp`             | `display arp`     | `show arp`           | `show arp` | `show arp` | `show arp` |

---

## 8. Port / Interface Aggregation (LACP / EtherChannel)
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Create port channel / LAG      | `interface port-channel <id>` | `interface Eth-Trunk <id>` | `interface lag <id>` | `interface lag <id>` | `trunk <interface> trk <id> lacp` | `interface port-channel <id>` |
| Add interface to LAG           | `channel-group <id> mode active` | `trunkport <interface> prelag <id>` | `lag <id> <interface>` | `lag <id> <interface>` | `trunk <interface> trk <id>` | `channel-group <id> mode active` |
| Show port channel / LAG        | `show etherchannel summary` | `display eth-trunk` | `show lag`         | `show lag` | `show trunk` | `show etherchannel summary` |

---

## 9. PoE / Power
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Show PoE status                | `show power inline`    | `display poe interface` | `show poe`          | `show poe` | `show power inline` | `show poe` |
| Enable PoE on interface        | `interface <int>` <br>`power inline auto` | `interface <int>` <br>`poe enable` | `interface <int>` <br>`poe enable` | `interface <int>` <br>`poe enable` | `interface <int>` <br>`poe enable` | `interface <int>` <br>`poe enable` |
| Disable PoE                    | `interface <int>` <br>`power inline never` | `interface <int>` <br>`poe disable` | `interface <int>` <br>`poe disable` | `interface <int>` <br>`poe disable` | `interface <int>` <br>`no poe` / `no power-over-ethernet` | `interface <int>` <br>`poe disable` |

---

## 10. Access Control / Security
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Show ACLs                      | `show access-lists`    | `display acl all` | `show access-list`  | `show access-list` | `show access-lists` | `show access-lists` |
| Apply ACL to interface         | `ip access-group <name> in|out` | `traffic-filter <name> inbound|outbound` | `ip access-group <name> in|out` | `ip access-group <name> in|out` | `ip access-group <name> in|out` | `ip access-group <name> in|out` |

---

## 11. Logging / Monitoring
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Show logs                      | `show logging`         | `display logbuffer` | `show logging`     | `show logging` | `show logging` | `show logging` |
| Enable logging to server       | `logging <server-ip>`  | `info-center loghost <server-ip>` | `logging host <server-ip>` | `logging host <server-ip>` | `logging <server-ip>` | `logging <server-ip>` |
| Show interface counters        | `show interfaces counters` | `display interface counters` | `show interfaces counters` | `show interfaces counters` | `show statistics` <br> / `show interfaces statistics`  | `show interfaces counters` |

---

## 12. NTP / Time Sync
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Configure NTP server           | `ntp server <ip>`      | `ntp-service unicast-server <ip>` | `ntp server <ip>` | `ntp server <ip>` | `ntp <server-ip>` | `ntp server <ip>` |
| Show NTP status                | `show ntp status`      | `display ntp status` | `show ntp status` | `show ntp status` | `show ntp status` | `show ntp status` |

---

## 13. SNMP
| Task / Function               | Cisco                  | Huawei             | Aruba                | FS | HP (ProCurve) | Dell (PowerConnect) |
|-------------------------------|-----------------------|------------------|--------------------|----|---------------|-------------------|
| Show SNMP configuration        | `show running-config` | `include snmp` | `display snmp-agent` | `show snmp` | `show snmp` | `show snmp` | `show snmp` |
| Configure SNMP community       | `snmp-server community <name> ro\|rw` | `snmp-agent community <name> read-only\|read-write` | `snmp-server community <name> ro\|rw` | `snmp-server community <name> ro\|rw` | `snmp-server community <name> <RO\|RW>` | `snmp-server community <name> ro\|rw` |

---

## References
- https://dl.dell.com/manuals/all-products/esuprt_ser_stor_net/esuprt_networking/networking-n1100-series_users-guide_en-us.pdf
- https://www.mcwireless.co.uk/post/basic-guide-to-dell-vs-cisco-commands
- https://dl.dell.com/manuals/all-products/esuprt_ser_stor_net/esuprt_pedge_srvr_ethnt_nic/poweredge-mseries-blademultipack_white%20papers53_en-us.pdf
- https://www.dell.com/support/kbdoc/en-us/000120225/basic-command-line-interface-on-dell-networking-powerconnect-2800-model-switches

---

\**This page will be updated over time.*
