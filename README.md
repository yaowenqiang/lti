Learning TCP/IP

# Protocols

+ Internet Protocol
+ Transmission Control Protocol
+ User Datagram Protocol
+ Address resolution Protocol
+ simple Mail transport Protocol
+ Hypertext Transport Protocol
+ Post Office Protocol

# Utilities

+ Wireshark - capturing packets
+ Ping - network diagnostics
+ Netstat - network statistics

# ICP IP fundamentals

## History of the Internet

+ Advanced Research Project agency
+ Requested a network that became ARPANet
+ 1967 - design discussions held
+ BBN contracted to build the ARPANet
+ Primarily used to facilitate research 
+ First nodes in 1969


transition to TCP


+ Host Software request in 1969
+ Network Control Protocol original protocol
+ 1974, first specification to TCP
+ 1978, spli into TCP and IP
+ 1981, RFC801 had NCP-TCP transition plan
+ Early 80s, TCP/IP becomes predominant protocol

Other Networks

+ BITNET - IBM Mainframes
+ Csnet - computer science network
+ Lat 1980s, NSFNet had faster backbone speed


## OSI MOdel 

Upper layers

+ Application -- HTTTP, FTP, SMTP
+ Presentation -- JPEG,GIF, MPEG
+ Session -- AppleTalk, Winsock 

 Lower layers

+ Transport -- TCP, UDP, SPX
+ Network -- IP, ICMP, IPX router
+ Data Link -- Ethernet, ATM switch, bridge
+ Physical -- ethernet, token Ring hub, repeater



+ Open Systems Interconnection
+ Seven Layer Model
+ Create in the 1970s as an architecture for distributed database systems
+ Adopted by the ISO as a standard communication architecture


Physical Layers

+ Handles all pyhsical definitions - connection types(coax, 4-pair, fiber, etc)
+ handles error connection and detection on the pyhsical medium

Data Link Layer 

+ Handles translation from digital data to physical signals(framing)
+ Physical addressing(Media Access Coontrol)
+ Flow control & access Control (CSMA/CD)

Network Layer

+ Logical addressing to ensure reachability
+ Handles getting data from one network to another(routing)
  + Conrast with Data Link Layer which is within the same network

Transport Layer

+ handles end-to-end, reliable data service
+ In the case of TCP/IP, handles ports to differentiate traffic

Session Layer

+ Controls specific dialogs between two systems (session management)
+ A bit more abstract than lower layers
+ Sometimes disagressment over which protocols land here(SSL/TLS, SSH, NetBIOS, etc)


Presentation Layer

+ Managing how data is presented
+ XML, JPEG

Application Layer

+ Applications
+ Closest to the user
+ Must do all management of connections


Layer to Layer

+ One layer speaks to another layer
+ Each layer adds headers (encapsulation)
+ each layer is responsible for peeling that layer off from the other end


TCP/IP Model

+ Application Layer
+ transport Layer
+ Internet Layer
+ Network Access Layer


> rfc1122


Internet Layer 

+ IP, ICMP intended for this layer
+ Robustness Principle - "Be liberal in what you accept and conservative in what you send" specifically applies here
+ Processing rules to ensure datagrams end up where they are supposed to
+ May require reassembly


Transport Layer

+ TCP, UDP are Transport Layer protocols
+ handle end-to-end delivery
  + UDP doesn't care whether datagrams arrive or not
  + TCP handles connection-oriented communication



Wireshark

filters

> ip
+ TCP
+ HTTP
+ ip.addr == 192.168.8.1
+ ip.src == 192.168.1.1


IETF



# Connections Protocols

## Ethernet

> OUI
> PPP PROTOCOL(Point to Point Protocol)

WAN Protocols - Sonet, ATM and Frame Relay

VLANs and 802.1Q


# Internet Protocol(IP)

## IP headers

### IP Address and Subnet


10.110.10.1 
Network address
10.110.10.0
Broadcast address
10.110.10.255

## Routing

> netstat -rn # show routing table
> traceroute 4.2.2.1

## BGP(Border Gatway Protocol port 179) 

ibgp
ebgp




## RIP(Routing Information Protocol)

## OSPF(Open Shortest Path First)

## ARP(Address Resolution Protocol)

>> arp -a

##  ARP spoofing

> arpspoof 192.168.1.1
> tcpdump -i br0 host 192.168.1.1

## RARP(Reverse Address Resolution Protocol)


## Internet Registries

> whois -h whois.arin.net 4.2.2.1

## Autoconfiguration with Bootp / DCHP

> /etc/udhcpd.conf


## IP configuration

### Windows

> ipconfig

> ipconfig /all

## IP fragmentation

> ping -s 3100 192.168.1.1

> Identification

# ICMP

Internet Control Message Protocol

## ICMP message types

> rfc 792

> https://tools.ietf.org/html/rfc792

## Ping

> ping  192.168.1.1

### Error messages

> traceroute www.google.com

### ICMP attach

> ping -s 1450 192.168.1.1

> ping 192.168.101.255



# TCP



# UDP
# Session Layer
# Application Layer
# Application Of Network Analysis

## Firewall

> https://www.checkpoint.com/
> cisco

### stateful firewall

> iptables

> sudo iptables -A OUTPUT -p tcp -m state --state NEW -j DROP
> sudo iptables -F

> sudo iptables -L -v

> sudo iptables -A OUTPUT -p icmp -m state --state NEW -j DROP

> sudo iptables -A OUTPUT -p tcp --dport 80 -m state --state NEW,ESTABLISHED,RELATED -j DROP
> telnet www.baidu.com 80 # fail
> telnet www.baidu.com 443 # succeed

### Stateless - Access Control Lists

### Application Layer Firewall

> squid proxy 

> cisco application layer protocol protection

> blue coat
> acmepacket


## Building Packets

> packETH
> hping

# Wireless
# IPv6
# wrapping Up
