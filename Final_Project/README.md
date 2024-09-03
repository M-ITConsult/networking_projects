# Final Project: Cisco Packet Tracer Network Simulation

## Overview

This project is a network simulation created using Cisco Packet Tracer. The network is designed to represent a small office or home office (SOHO) setup with basic networking components. The network includes three PCs, a switch, a router, a printer, a server, and a cloud to connect to the internet. The main objective of this project is to demonstrate basic networking concepts such as IP addressing, DNS configuration, and internet connectivity.

## Network Topology

The network consists of the following components:
- **Three PCs (PC-Robert, PC-Camille, PC-Renaud):** End devices connected to the switch. Each PC is assigned a unique IP address.
- **One Switch (Switch0):** A central device to which all PCs, the printer, and the server are connected.
- **One Router (Router1):** The gateway device that connects the local network to the internet via the cloud.
- **One Printer (Printer0):** A network printer accessible by all PCs on the network.
- **One Server (Server0):** A server hosting a webpage that can be accessed via a custom DNS name.
- **One Cloud (Cloud0):** Represents the internet connection. It allows one of the PCs to access external websites.

## Key Features

1. **Local Network Configuration:**
   - All devices are assigned static IP addresses within the same subnet.
   - The switch facilitates communication between devices on the local network.

2. **Internet Connectivity:**
   - One of the PCs (PC0) is configured to access the internet through the router and cloud.
   - The router is configured with a default route to forward traffic to the internet.

3. **DNS Configuration:**
   - A DNS service is configured on the server (Server0).
   - The DNS service resolves the domain name `www.cisco.com` to the IP address of the server, allowing PCs to access a hosted webpage using this domain name.

4. **Web Server:**
   - A basic web page is hosted on the server, accessible via the DNS name `www.cisco.com`.
   - Any PC on the network can access this page by entering `www.cisco.com` in a web browser.

5. **Printer Setup:**
   - The printer is configured to be accessible from any PC on the network for printing tasks.

## How to Use

1. **Open the Project:**
   - Load the provided Cisco Packet Tracer file (.pkt) into Cisco Packet Tracer.

2. **Test Network Connectivity:**
   - Use the "Ping" tool or the command prompt on each PC to verify connectivity between devices.
   - Ensure that `PC-Robert` can ping external IP addresses to confirm internet access.

3. **Access the Webpage:**
   - Open a web browser on any of the PCs.
   - Enter `www.cisco.com` in the address bar to access the web page hosted on `Server0`.

4. **Printer Test:**
   - Ping to the printer with any pcs.

## IP Addressing Scheme

- **PC-Robert:** 192.168.1.10
- **PC-Camille:** 192.168.1.11
- **PC-Renaud:** 192.168.1.12
- **Server0:** 192.168.1.254
- **Printer0:** 192.168.1.13
- **Router0 (LAN Interface):** 192.168.1.1
- **Router0 (WAN Interface):** [Configured according to your setup]
- **Cloud0:** [Configured to simulate an internet connection]

## DNS Settings

- **Domain Name:** `www.cisco.com`

## Conclusion

This project demonstrates the basic setup and configuration of a small network using Cisco Packet Tracer. It includes internet connectivity, local network communication, DNS services, and a simple web server. This simulation is ideal for understanding the foundational concepts of networking in a controlled environment.