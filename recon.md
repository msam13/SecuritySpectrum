# Reconnaissance Tools and Tactics

## Terminal tools
1. whois `domain_name`<br> 
2. dig -t `flag` `domaing_name`
	- MX
	- AXFR
	- ANY

## Google Dork
```
- site
- link
- inurl
- intitle
- filetype
- intext

```
checkout : gdbd

## Shodan
Used to find IoT devices on internet

## NMAP
Port scanning works for TCP, since they repond with syn+ack when they recieve a syn

NMAP send the following in the order given below, to find whether an IP is in use
1. ICMP echo request (ping)
2. TCP SYN to 443
3. TCP ACK to 80
4. ICMP timestamp requet

**NMAP scan types** : 
1. `-sT` TCP FULL connect scan
1. `-sS` TCP SYN scan (default when root)
1. `-sA` TCP ACK scan (useful for mapping firewall rules)
1. `-sF` TCP FIN scan (useful for mapping firewall rules)
1. `-sN` TCP NULL scan (no TCP flag is set)
1. `-sU` UDP scan
1. `-sX` Xmas scan (FIN, PSH, URG are set)

**OS Fingerprinting**
`-O` 

**Version scanning**
`-sV`

**ALL** (OS detection, version detection, Script scanning, traceroute)
`-A`

**Other ARGS**
`-p `(port)
example : -p U:53,111,137, T:21-25

The "-Oa" flag in Nmap is used to enable aggressive operating system detection. This flag tells Nmap to use a combination of active and passive techniques to determine the operating system of the target machine.It sends more probes to the target, which may increase the chance of being detected by intrusion detection systems (IDS) or firewalls. Therefore, it should be used with caution and only when necessary.
