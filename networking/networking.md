[العربي](./networking_ar.md)

# <a name="-13-networking"></a>🌐 Chapter 13: Networking

## 1. What is it?

Computer Networking is the discipline concerned with connecting two or more devices together for the purpose of sharing resources and exchanging information. It is the "circulatory system" of the digital world, allowing data to flow between different points, whether they are in the same room or on different continents.

The best analogy: Imagine it as the global postal and logistics system, but for digital data.

## 2. What does the specialist do?

A Network Engineer is responsible for designing, implementing, maintaining, and securing the computer networks that organizations rely on. Their tasks include:

* Configuring network devices: Setting up devices like Routers, Switches, and Firewalls.
* Designing networks: Designing the network layout, IP addressing schemes, and segmenting the network into subnets.
* Monitoring network performance: Monitoring data traffic to identify bottlenecks and ensure network speed.
* Troubleshooting: Diagnosing and resolving connectivity issues.
* Implementing security policies: Enforcing security rules on the network to prevent unauthorized access.

## 3. Sub-domains

* Enterprise Networking: Managing the internal networks of large companies.
* Data Center Networking: Designing ultra-high-speed networks within data centers.
* Service Provider Networking: Working for Internet Service Providers (ISPs) to build and manage the core infrastructure of the internet.
* Network Security: A specialization that focuses on protecting the network itself (overlaps with Cybersecurity).
* Wireless Networking: Specializing in Wi-Fi and other wireless technologies.

## 4. Expanded Key Concepts

* Networking Models (OSI & TCP/IP):
  * `OSI Model`: A theoretical 7-layer model to standardize network functions. It is a reference for study and understanding.
  * `TCP/IP Model`: A practical 4-layer model on which the internet is built.
* Addressing:
  * `IP Address`: The logical address of a device on the network (e.g., 192.168.1.10). There are two versions: IPv4 (old) and IPv6 (new).
  * `MAC Address`: The unique physical address of a network card, which does not change.
  * `Subnet Mask`: Used to divide a large network into smaller subnets.
* Core Protocols:
  * `IP`: Responsible for routing "Packets" to the correct address.
  * `TCP`: Provides a reliable, ordered, and error-free connection (like registered mail).
  * `UDP`: Provides a fast but unreliable connection (like a postcard).
  * `DNS`: The "phone book of the internet" that translates domain names (like google.com) into IP addresses.
  * `DHCP`: Automatically assigns IP addresses to devices on the network.
* Network Devices: Router (connects different networks), Switch (connects devices on the same network), Firewall (for protection).

## 5. Expanded Tools & Technologies

* Hardware Vendors: Cisco, Juniper, Arista.
* Network Analysis Tools: Wireshark (for packet analysis), tcpdump.
* Network Scanning Tools: Nmap.
* Command-Line Tools: ping, traceroute, ipconfig/ifconfig, netstat.
* Simulation Software: Cisco Packet Tracer, GNS3.
* Monitoring Tools: Nagios, Zabbix.

## 6. In-Depth Workflow

Project: A new employee has joined the company and needs to connect their computer to the office network.

 1. Physical Connection: The network engineer ensures an available network port and connects the employee's computer to the port via an Ethernet cable. This port is connected to a Switch in the server room.
 2. Obtaining an IP Address (via DHCP): When the computer starts, it sends a broadcast message on the local network saying, "I'm new here, can I have an IP address?" The DHCP server responds and offers an available IP address (e.g., 10.1.2.55), a subnet mask, and the default gateway address (the router).
 3. Accessing the Internet: The employee opens a browser and types <www.google.com>.
     * DNS Query: The computer doesn't know Google's IP, so it sends a query to the local DNS server, which looks up the IP and returns it to the computer.
     * Routing: The browser creates an HTTP packet destined for Google's IP. Since this IP is outside the local network, the computer sends the packet to the "default gateway" (the office's main router).
     * Packet Journey: The router forwards the packet to the next router in the ISP's network, and the packet hops from router to router across the internet until it reaches Google's data center.
 4. Firewall: Throughout this process, the firewall inspects the data traffic. It allows the outgoing request from the employee but blocks any unsolicited incoming connections from the internet.
 5. Troubleshooting: If the employee says "The internet is not working," the engineer uses the following steps:
     * `ipconfig`: Did the computer get a correct IP?
     * `ping 8.8.8.8`: Can I reach the internet? (tests basic connectivity).
     * `ping www.google.com`: Is DNS working correctly?
     * `traceroute www.google.com`: Where is the connection breaking in the path?

## 7. Common Job Roles

* Network Engineer
* Network Administrator
* Network Architect
* Network Security Engineer

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`ARP`** | Address Resolution Protocol, links an IP address to a MAC address on a local network. |
| **`DHCP`** | Dynamic Host Configuration Protocol, automatically distributes IP addresses to devices. |
| **`DNS`** | Domain Name System, translates domain names into IP addresses. |
| **`Firewall`** | A device or software that inspects and filters network traffic. |
| **`Gateway`** | The default gateway, the device (usually a router) that directs traffic from a local network to external networks. |
| **`HTTP/HTTPS`** | Hypertext Transfer Protocol, the foundation of web browsing. |
| **`IP Address`** | The unique logical address of a device on a network. |
| **`LAN`** | Local Area Network. |
| **`MAC Address`** | Media Access Control address, the unique physical address of a network card. |
| **`NAT`** | Network Address Translation, a technique that allows multiple devices on a private network to share a single public IP address. |
| **`NIC`** | Network Interface Card, the hardware that allows a computer to connect to a network. |
| **`OSI Model`** | Open Systems Interconnection model, a 7-layer reference model. |
| **`Packet`** | A small unit of data sent over a network. |
| **`Ping`** | A tool to test the reachability of another device on a network. |
| **`Port`** | A number used to identify a specific application or service on a device (e.g., port 80 for web). |
| **`Protocol`** | A set of rules that govern how data is exchanged. |
| **`Router`** | A device that connects different networks and forwards packets between them. |
| **`Subnet`** | A sub-section of a larger network. |
| **`Switch`** | A device that connects devices within the same local network. |
| **`TCP`** | Transmission Control Protocol, provides a reliable connection. |
| **`Traceroute`** | A tool that traces the path of packets across a network from source to destination. |
| **`UDP`** | User Datagram Protocol, provides a fast but unreliable connection. |
| **`VLAN`** | Virtual Local Area Network, allows a single physical LAN to be partitioned into multiple logical virtual networks. |
| **`VPN`** | Virtual Private Network, creates a secure and encrypted connection over a public network like the internet. |
| **`WAN`** | Wide Area Network. |

</details>

[⬆️ Back to Table of Contents](../README.md)

