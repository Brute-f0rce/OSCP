# Kali Linux Commands

## Basics

### Set the Target IP Address to the \`$ip\` system variable

```bash
export ip=192.168.1.100
```

### Find the location of a file

```bash
locate sbd.exe
```

### Search through directories in the \`$PATH\` environment variable

```bash
which sbd
```

### Find a search for a file that contains a specific string in it’s name

```bash
find / -name sbd\*
```

### Show active internet connections

```bash
netstat -lntp
```

### Verify a service is running and listening

```bash
netstat -antp |grep apache
```

### Boot, Start, Stop a service

```bash
systemctl enable ssh # Boot
systemctl start ssh # Start
systemctl start apache2 # Start
systemctl stop ssh #Stop
```

### Unzip a gz and tar.gz file

```bash
gunzip access.log.gz
tar -xzvf file.tar.gz
```

### Search Command History

```bash

```

### Download a Webpage

```text

```

### Print all files content in a directory

```bash

```

## String manipulation

### Count number of lines in file

```bash
wc -l index.html
```









## Decoding using Kali

### Decode Base64 Encoded Values

```bash
echo -n "QWxhZGRpbjpvcGVuIHNlc2FtZQ==" | base64 --decode
```







## Networking

### Manage Network Interfaces

```bash
vi /etc/network/interfaces
```







## Netcat









## Wireshark







## Tcpdump

### Display a pcap file

```bash
> tcpdump -r passwordz.pcap
```

### Display ips and filter and sort

```bash
> tcpdump -n -r passwordz.pcap | awk -F" " '{print $3}' | sort -u | head
```

### Grab a packet capture on port 80

```bash
> tcpdump tcp port 80 -w output.pcap -i eth0
```

### Check for ACK or PSH flag set in a TCP packet

```bash
> tcpdump -A -n 'tcp[13] = 24' -r passwordz.pcap
```



## IPTables

### Deny traffic to ports except for Local Loopback

```bash
> iptables -A INPUT -p tcp --destination-port 13327 ! -d $ip -j DROP

> iptables -A INPUT -p tcp --destination-port 9991 ! -d $ip -j DROP
```



### Clear ALL IPTables firewall rules

```bash
> iptables -P INPUT ACCEPT
> iptables -P FORWARD ACCEPT
> iptables -P OUTPUT ACCEPT
> iptables -t nat -F
> iptables -t mangle -F
> iptables -F
> iptables -X
> iptables -t raw -F iptables -t raw -X
```



## Users manipulation

### Adding a new user

```bash
> adduser <user name>
```

### Adding a User to the sudoers Files

```bash
> adduser <user name> sudo
```

### Switch Users

```bash
> su <user name>
```



