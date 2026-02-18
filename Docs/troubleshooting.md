Troubleshooting & Issue Resolution

This document records real technical issues encountered during the enterprise sysadmin lab build and the steps taken to diagnose and resolve them.

❗ Issue 1 – Client Received APIPA Address (169.254.x.x)
Symptoms:

Client could not communicate with Domain Controller

No internet or domain connectivity

IP address automatically assigned as 169.254.x.x

Cause:

DHCP was not providing an IP address to the client.

Resolution:

Verified network adapter connected to internal lab switch

Configured DHCP server properly

Renewed client IP address using:

ipconfig /release
ipconfig /renew

Result:

Client successfully received valid IP address from DHCP.

❗ Issue 2 – Domain Join Failed
Symptoms:

Error when attempting to join lab.local domain

Client unable to locate Domain Controller

Cause:

DNS server not pointing to Domain Controller IP address.

Resolution:

Updated client DNS to DC01 IP

Verified using:

ipconfig /all

Result:

Domain join completed successfully.

❗ Issue 3 – Server Accidentally Configured for DHCP Instead of Static IP
Symptoms:

Domain Controller received APIPA address

Network services disrupted

Cause:

Network settings were mistakenly modified on server instead of client.

Resolution:

Reconfigured DC01 with static IP

Restored DNS pointing to itself

Result:

Domain services stabilized.

🧠 Key Lessons Learned

DNS is critical for Active Directory functionality

Domain Controllers must always use static IP addresses

APIPA indicates DHCP/network failure

Always verify which machine is being configured

IP configuration should be validated early

📸 Supporting Screenshots

Located in:

screenshots/

🎯 Outcome

All network and domain-related issues were successfully diagnosed and resolved, resulting in a fully functional enterprise-style lab environment.

🚀 Value of This Section

Demonstrates:

✔ Real troubleshooting skills
✔ Root cause analysis
✔ Enterprise thinking
✔ Practical IT experience