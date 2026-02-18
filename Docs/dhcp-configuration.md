DHCP Configuration

This document describes the setup and verification of the Dynamic Host Configuration Protocol (DHCP) service used to automatically assign IP addresses to client machines in the enterprise sysadmin lab.

🌐 Purpose of DHCP in This Lab

DHCP is used to:

Automatically assign IP addresses to client computers

Reduce manual configuration errors

Centralize network address management

Simulate real enterprise networking environments

🖥️ DHCP Server Role Installation

DHCP role was installed on:

Server: DC01

Steps performed:

Opened Server Manager

Added DHCP Server role

Completed post-installation configuration

Authorized DHCP in Active Directory

📡 DHCP Scope Configuration

Configured a scope for the internal lab network:

Example Scope Settings:

IP Range: (example) 192.168.1.50 – 192.168.1.200

Subnet Mask: 255.255.255.0

Default Gateway: (if applicable)

DNS Server: DC01 IP address

Domain Name: lab.local

🔄 Client Configuration

Client machines were set to:

Obtain IP address automatically

Obtain DNS server automatically

This allows DHCP to assign both IP and DNS information.

✅ Verification & Testing

On client machines:

ipconfig /release
ipconfig /renew
ipconfig /all


Confirmed:

DHCP-assigned IP address

DNS pointing to DC01

Successful network connectivity

Successful domain communication

🧠 Best Practices Implemented

✔ Servers use static IP addresses
✔ Clients use DHCP for scalability
✔ Centralized DNS distribution
✔ Enterprise-style network management

📸 Related Screenshots

Stored in:

screenshots/

🎯 Outcome

DHCP successfully automates IP addressing for all client systems while maintaining proper DNS and domain communication.

🚀 Next Steps

DHCP now supports:

Scalable client growth

Automated network configuration

Reliable domain connectivity