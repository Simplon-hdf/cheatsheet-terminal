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
## dig
The dig command queries Domain Name Systems (DNS) and finds information for DNS records. The command collects domain name information and associated records.
```
dig [options] [domain] [record type] [DNS server]
```
## nslookup
The nslookup command is similar to the dig command. The main difference between the two commands is that nslookup features an interactive mode. It enables diagnosing and querying DNS servers, which is helpful for network troubleshooting and DNS tasks.
```
nslookup [domain] [DNS server]
```
## netstat
The netstat command (network statistics) is a networking utility that shows various networking statistics. The command provides statistics for network ports and shows port availability.
```
netstat [options]
```
## traceroute
The traceroute command is a networking diagnostics tool available for Linux, macOS, and Windows. The command tracks the route that packets take to reach a destination on a TCP/IP network.
```
traceroute [options] [hostname/IP]
```
