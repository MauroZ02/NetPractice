*This project has been created as part of the 42 curriculum by mzangaro.*

# NetPractice

## Description

**NetPractice** is a practical networking project from the 42 curriculum. Its purpose is
to introduce the fundamental concepts required to understand and configure small IPv4
networks.

The project is completed through a browser-based training interface. Each level presents
a network that is incorrectly configured and a set of communication goals. The objective
is to modify the available IP addresses, subnet masks and routing tables until every
required device can communicate correctly.

Rather than writing a program, NetPractice focuses on understanding how packets travel
through a network and how hosts, switches and routers interact with one another.

There are **10 training levels**. A configuration file must be exported after completing
each level and submitted in the Git repository.

## Networking concepts studied

The main concepts studied while completing the project were:

- IPv4 addressing and the structure of a 32-bit IPv4 address.
- Network and host portions of an IP address.
- Subnet masks and CIDR notation.
- Network addresses, broadcast addresses and usable host ranges.
- Subnetting and subnet size calculation.
- Public and private IPv4 address ranges.
- Loopback addresses.
- Local Area Networks (LANs) and other network types.
- Default gateways.
- Switches and communication inside the same network.
- Routers and communication between different networks.
- Router interfaces and the fact that one router can belong to several networks.
- Routing tables.
- Destination networks and next-hop addresses.
- Default routes (`0.0.0.0/0`).
- Forward and reverse packet paths.
- TCP/IP addressing.
- The TCP/IP model.
- The OSI model and its layers.
- The role of Layer 2 switching and Layer 3 routing.
- Packet forwarding between hosts, routers and networks.

A particularly important idea in NetPractice is that successful communication is
**bidirectional**. It is not enough for a packet to reach its destination: the destination
must also have a valid path back to the source.

## Instructions

### Launching the training interface

Download and extract the NetPractice files supplied with the project.

From the extracted directory, run:

```bash
./run.sh
```

The script launches a local web server and opens the NetPractice interface in a browser.

If `run.sh` does not work, the interface can be served manually with Python:

```bash
python3 -m http.server 49242
```

Then open:

```text
http://localhost:49242
```

### Training

1. Open the **Training** tab.
2. Enter your 42 login.
3. Start the first level.
4. Read the communication objective or objectives displayed at the top of the page.
5. Modify only the editable fields in the network diagram.
6. Use **Check again** to test the configuration.
7. Read the logs at the bottom of the interface when a route or configuration is wrong.
8. Once the level is correct, use **Get my config** to export the configuration.
9. Save the exported file.
10. Continue to the next level and repeat the process until all 10 levels are complete.

When troubleshooting a level, the configuration should be analysed in terms of:

1. Which subnet each interface belongs to.
2. Whether directly connected interfaces are in compatible subnets.
3. Whether a host can reach its configured gateway.
4. Whether the router has a route towards the destination network.
5. Whether the specified next hop is reachable.
6. Whether a valid reverse route exists from the destination back to the source.

## Submission

The repository must contain:

- This `README.md`.
- **10 exported configuration files**, one for each NetPractice level.
- All 10 configuration files must be placed at the **root of the repository**.

The login used in the NetPractice interface must be the student's 42 login before
exporting the configurations.

During the peer evaluation, three random levels must be solved within a limited amount
of time. External tools are not allowed during the evaluation, apart from a simple
calculator such as `bc`.

## Resources

The following materials were used or collected while studying NetPractice. They cover
NetPractice itself as well as IPv4 addressing, subnetting, routing, routers, switches,
packet forwarding, TCP/IP and the OSI model.

Where different resources present concepts with different levels of detail, standards
and technical documentation such as RFC, Cisco, Microsoft and IBM documentation should
be preferred for verification.

### NetPractice-specific guides

- **From Zero to Network Hero: A Practical Guide to NetPractice 1337 Rabat — Mohamed Amin Tarza**  
  https://medium.com/%40mohamedamintarza/from-zero-to-network-hero-a-practical-guide-to-netpractice-1337-rabat-a2ffb614a928

- **tblaase — Net_Practice: solutions and networking basics**  
  https://github.com/tblaase/Net_Practice?utm_source=chatgpt.com

- **lpaube — NetPractice guide**  
  https://github.com/lpaube/NetPractice

- **NetPractice: An Intro to IP Addresses and Subnets**  
  https://www.youtube.com/watch?v=HQUw0CfQWAM

### IPv4 addressing, subnetting and CIDR

- **NetworkChuck — What is an IP Address? // You SUCK at Subnetting // EP 1**  
  https://www.youtube.com/watch?v=5WfiTHiU4x8&list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF&index=1

- **NetworkChuck — We ran OUT of IP Addresses!! // You SUCK at Subnetting // EP 2**  
  https://www.youtube.com/watch?v=tcae4TSSMo8&list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF&index=2

- **NetworkChuck — Private IP Addresses**  
  The same video was supplied through several positions in the subnetting playlist:

  - https://www.youtube.com/watch?v=8bhvn9tQk8o&list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF&index=3
  - https://www.youtube.com/watch?v=8bhvn9tQk8o&list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF&index=4
  - https://www.youtube.com/watch?v=8bhvn9tQk8o&list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF&index=5
  - https://www.youtube.com/watch?v=8bhvn9tQk8o&list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF&index=6

- **IPv4 Addressing and Subnetting (Explained)**  
  https://www.youtube.com/watch?v=SHbBso63X38

- **Practical Networking — Subnetting Mastery**  
  https://www.practicalnetworking.net/stand-alone/subnetting-mastery/?utm_source=chatgpt.com

- **RFC 4632 — Classless Inter-domain Routing (CIDR): The Internet Address Assignment and Aggregation Plan**  
  https://www.rfc-editor.org/info/rfc4632/?utm_source=chatgpt.com

- **Cisco — Configure IP Addresses and Unique Subnets for New Users**  
  https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html

- **IBM — TCP/IP Addressing**  
  https://www.ibm.com/docs/es/aix/7.1.0?topic=protocol-tcpip-addressing

- **Microsoft Learn — TCP/IP Addressing and Subnetting**  
  https://learn.microsoft.com/es-es/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting

- **Types of IP addresses: private, public, static and dynamic — Alberto López**  
  https://www.youtube.com/watch?v=iHJnqDR5sF8

### Routing, routers, switches and packet travel

- **Practical Networking — Packet Traveling Series Finale**  
  https://www.practicalnetworking.net/series/packet-traveling/packet-traveling-series-finale/?utm_source=chatgpt.com

- **NetworkChuck — What is a ROUTER? // FREE CCNA // EP 2**  
  https://www.youtube.com/watch?v=p9ScLm9S3B4

- **NetworkChuck — What is a SWITCH? // FREE CCNA // Day 1**  
  https://www.youtube.com/watch?v=9eH16Fxeb9o

### TCP/IP and OSI models

- **OSI and TCP/IP Models — Best Explanation**  
  https://www.youtube.com/watch?v=3b_TAYtzuho

- **NetworkChuck — REAL LIFE example!! TCP/IP and OSI layers**  
  https://www.youtube.com/watch?v=3kfO61Mensg

- **NetworkChuck — What is TCP/IP and OSI? // FREE CCNA // EP 3**  
  https://www.youtube.com/watch?v=CRdL1PcherM

- **What is the OSI Model? Explained Simply — Alberto López**  
  https://www.youtube.com/watch?v=ODY4q4_3Acc

- **Wikipedia — TCP/IP Model**  
  https://es.wikipedia.org/wiki/Modelo_TCP/IP

- **Fortinet — What is TCP/IP?**  
  https://www.fortinet.com/lat/resources/cyberglossary/tcp-ip

### General networking

- **Network Types: LAN, WAN, PAN, CAN, MAN, SAN, WLAN**  
  https://www.youtube.com/watch?v=4_zSIXb7tLQ&t=3s

### Additional discovery reference

The following Google search was also supplied during the research process and was used
to discover additional material about TCP/IP addressing:

https://www.google.com/search?q=tcp%2Fip+addressing&oq=tcp%2Fip+addressing+&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIICAEQABgWGB4yCAgCEAAYFhgeMggIAxAAGBYYHjIICAQQABgWGB4yCAgFEAAYFhgeMggIBhAAGBYYHjIGCAcQRRg60gEJMTE4NDFqMGo3qAIAsAIA&sourceid=chrome&ie=UTF-8

## AI usage

AI was used as a learning and review tool during the project, particularly for:

- Explaining networking terminology in simpler terms.
- Reviewing IPv4 addressing and subnetting reasoning.
- Checking how subnet masks divide addresses into network and host portions.
- Analysing routing tables and identifying the purpose of destination and next-hop fields.
- Following packets through hosts and routers step by step.
- Understanding default gateways and default routes.
- Diagnosing failed forward and reverse paths from NetPractice logs.
- Comparing the roles of switches and routers.
- Discussing the TCP/IP and OSI models.
- Organising and reviewing the resources used during the learning process.
- Structuring and proofreading this README.

AI-generated explanations were treated as study support and were cross-checked against
the project subject, technical documentation and the other resources listed above. The
goal was to understand the reasoning behind each configuration rather than simply
obtain completed NetPractice solutions.
