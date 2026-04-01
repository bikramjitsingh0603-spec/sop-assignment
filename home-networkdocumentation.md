# Home Network Documentation
Author: Bikramjit Singh

---

# 1. Physical Network Topology

The home network is installed in a two-room apartment with the main router located in the living room. The modem connects to the ISP service line and provides internet access to the wireless router.

Physical layout:

Living Room:
- ISP Modem (connected to fiber line)
- WiFi Router (connected to modem using Ethernet cable)
- Desktop Computer (connected via Ethernet cable)

Bedroom:
- Laptop (connected via WiFi)
- Smartphone (connected via WiFi)
- Smart TV (connected via WiFi)

Connection Types:
- Ethernet cables: Cat6
- Wireless: 2.4 GHz and 5 GHz WiFi

---

# 2. Logical Network Topology
# Network Topology Diagram

![Network Diagram](topoplogy.png)

The home network follows a star topology where all devices connect through a central wireless router.

Topology Structure:

Internet → ISP Modem → Wireless Router → Devices

Connected Devices:

- Desktop PC
- Laptop
- Smartphone
- Smart TV

The router manages DHCP, NAT, firewall protection, and wireless access.

---

# 3. Addressing Documentation

Private IP addressing scheme:

Network Range:
192.168.1.0/24

Default Gateway:
192.168.1.1

Device Address Table:

| Device | IP Address | Connection Type |
|-------|-----------|----------------|
Router | 192.168.1.1 | Ethernet |
Desktop | 192.168.1.10 | Ethernet |
Laptop | 192.168.1.20 | WiFi |
Smartphone | 192.168.1.30 | WiFi |
Smart TV | 192.168.1.40 | WiFi |

DHCP Range:
192.168.1.100 – 192.168.1.200

DNS Server:
Provided automatically by ISP router

---

# 4. Network Devices and Services

Devices used in the network:

ISP Modem
Provides internet connectivity from service provider

Wireless Router
Provides DHCP services
Provides NAT translation
Provides firewall protection
Provides wireless connectivity

Desktop Computer
Used for assignments and development work

Laptop
Used for portable connectivity

Smartphone
Used for daily communication

Smart TV
Used for streaming services

Services running:

DHCP (Router)
NAT (Router)
Firewall (Router)
WiFi Access Point (Router)

---

# 5. Device Configurations

Router Configuration:

SSID Name:
Home_Network

Wireless Security:
WPA2 Personal

Router Login Address:
192.168.1.1

DHCP Enabled:
Yes

Firewall Enabled:
Yes

NAT Enabled:
Yes

Desktop Configuration:

Connection Type:
Ethernet

IP Assignment:
DHCP automatic

Laptop Configuration:

Connection Type:
Wireless

IP Assignment:
DHCP automatic

---

# 6. Secure Storage of Login Credentials

All network login credentials are securely stored using a password manager.

Security Method Used:

Microsoft Edge Password Manager

Additional protection methods:

Strong passwords enabled
Two-factor authentication enabled
Router admin password changed from default
WiFi password secured with WPA2 encryption
