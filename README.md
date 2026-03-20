# net-practice
Fundamentals, and general exercises to discover networking.

______________________________________________________________________
  
**NetPractice** is mostly about IPv4 addressing + routing decisions:

  1. Subnet masks and what they imply
  2. Network/broadcast/host ranges
  3. Default gateway meaning
  4. When hosts can talk directly vs must route
  5. How routers choose where to forward packets (longest prefix match)?

______________________________________________________________________
  
**What is an IP?**

An IP address stands for Internet Protocol Address, which is a set of rules for communication over the internet, such as sending emails, streaming videos, or connecting to a website, etc…, an IP address identifies a network or a device on the internet. 
  
**What is the difference between the IPv4 and the IPv6?**

**IPv4:** Deployed in the 1981, works with a 32-bits address, and has over 4.3 billion addresses (which is a small amount of addresses compared to IPv6), so IP addresses must be reused and masked, and it uses Numeric Dot-Decimal Notation (ex: 192.108.42.64), and you have to configure it manually.    
**Ipv6:** Deployed in the 1998, works with a 128-bits address, and has over 340 undecillion addresses (which is 340 trillion, trillion, trillion, trillion [36 zeros]), so every device can have it's unique IP address, and it uses Alphanumeric Hexadecimal Notation (ex: 2002:0de6:0001:0042:0100:8c2e:0370:7234), and it supports auto-configuration.
  
  
**What is TCP/IP?**

TCP/IP stands for Transmission Control Protocol/Internet Protocol, which is a set of rules that guide and allow computers to communicate on a network such as the internet.
  
______________________________________________________________________

**The four layers of the TCP/IP model:**
  
**Datalink Layer:** also called the physical layer, handles the physical parts of sending and recieving data using the Ethernet, or WiFi, etc…  
**Internet Layer:** also called the network layer, and it controls the movement of the packets around the internet.  
**Transport Layer:** provides a reliable data connection between two devices, it divides the data into packets, knows the packets that are recieved from the other device, and it makes sure that the other device knows the packets it recieves.  
**Application Layer:** group of the applications that requires a network communication, which is what the user typically interacts with, such as emails, and messaging, because the lower layer handles the details of communication, and there’s no need for the applications to concern themselves with it.  

______________________________________________________________________
