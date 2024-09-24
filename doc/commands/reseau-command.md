# Network command
---
## Summary
- [ip](#ip)
    - [ip adr](#ip-adr)
    - [ip link](#ip-link)
    - [ip route](#ip-route)
- [dig](#dig)
## ip
The ip command helps view and configure routing, interfaces, network devices, and tunnels.
```
ip [ OPTIONS ] OBJECT { COMMAND | help }
```
#### ip adr
The ip addr command manages and shows network interface IP addresses.
```
ip addr [subcommand]
```
#### ip link
The ip link command manages and shows network interface information. It allows viewing, changing, enabling, and disabling network interfaces.
```
ip link [subcommand] [options] [interfaces]
```
#### ip route
The ip route command shows and configures the IP routing table. The command allows users to adjust the routing table and perform other crucial networking tasks with the routing table.
```
ip route [subcommand] [options] [destination]
```
## ifconfig
The ifconfig (interface configuration) command manages and shows network interface information on a system. The command is part of the net-tools package.
```
ifconfig [interface] [options]
```