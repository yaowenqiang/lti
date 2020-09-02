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





# Connections Protocols
# Internet Protocol(IP)
# ICMP
# TCP
# UDP
# Session Layer
# Application Layer
# Application Of Network Analysis
# Wireless
# IPv6
# wrapping Up
