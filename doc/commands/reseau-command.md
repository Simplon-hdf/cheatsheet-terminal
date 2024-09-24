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
## tracepath
The tracepath command is similar to the traceroute command. The command identifies paths and latencies from source to destination, mapping the router and network hops.
```
tracepath [options] [hostname/IP]
```
## host
The host command is a simple tool for performing DNS lookups. The command resolves IP addresses into domain names and vice versa.
```
host [options] [hostname/IP]
```
## hostname
The hostname command helps display and change a system's hostname and domain and identifies devices within a network environment.
```
hostname [options] [name]
```
## ping
The ping command is a network utility for testing whether a host is reachable. The command sends ICMP requests to a host (a computer or server) and measures the round-trip time (RTT).
```
ping [options] [hostname/IP]
```
## ss
The ss command is a CLI tool for displaying network statistics. The tool is part of the iproute2 package and is a faster alternative to the netstat command.
```
ss [options] [filter]
```
## route
The route command in Linux is a specialized command for displaying and configuring the routing table. The command modifies the kernel's IP routing tables and helps set up static routes to specific hosts or networks.
```
route [options] [subcommand] [arguments]
```
## arp
The arp command shows and configures the Address Resolution Protocol (ARP) cache.
```
arp
```
## iwconfig
The iwconfig command shows and configures wireless network interface information.
```
iwconfig [interface] [options]
```
## curl or wget
The wget and curl commands are command-line tools for downloading files from the internet.
```
wget [options] [URL]
```
```
curl [options] [URL]
```
## mtr
The mtr command (my traceroute) is a diagnostics tool that combines elements from the ping and traceroute commands.
```
mtr [options] [hostname/IP]
```