🔍 Task 1 – Network Port Scanning with Nmap

📌 Objective
Perform a TCP SYN Scan on the local network to discover open ports and running services, enhancing your understanding of network exposure and basic reconnaissance techniques.

🛠️ Tools Used
Nmap – for scanning the network and discovering open ports.

Wireshark (optional) – for analyzing network traffic.

Ubuntu 22.04 (VirtualBox VM)

🧪 What I Did
Installed Nmap:

bash
Copy
Edit
sudo apt install nmap
Identified Local IP Addresses & Interfaces:

bash
Copy
Edit
ip a | grep inet
Found IPs like 127.0.0.1, 10.0.2.15, 192.168.0.116.

Scanned the Loopback Range:

bash
Copy
Edit
sudo nmap -sS 127.0.0.1/8
Discovered port 631 (IPP service) open on 127.0.0.1.

Saved Results:

Screenshots captured (see repo).

Network traffic recorded in .pcapng format using Wireshark.

📸 Evidence
Description	Screenshot
🔢 Nmap Scan on 127.0.0.1/8	
![linux nmap](https://github.com/user-attachments/assets/e2ffce66-4c98-4a70-8637-b391291132fb)

🌐 IP Address Info	
![ip linux](https://github.com/user-attachments/assets/c3d80232-06e0-46fd-a72b-c0fe686e4711)

📦 Packet Capture	nmap_scan_capture.pcapng

🧠 Key Concepts
TCP SYN Scan (-sS): Stealth scan that sends SYN packets and detects open ports without completing the handshake.

IP Range Discovery: Helps identify all devices in the subnet.

Service Enumeration: Port 631 (IPP) was detected, commonly used by printer services.

Security Insight: Each open port is a potential entry point. Minimizing open ports = minimizing attack surface.

⚠️ Risks of Open Ports
Open ports can allow unauthorized access, especially if the service has vulnerabilities.

Port scanning is a common technique used by attackers to identify exploitable services.

Example: Port 631, if exposed, could allow attackers to interfere with printing services.

🔐 Securing Open Ports
Use a firewall to block unnecessary ports.

Disable services that aren't required.

Regularly audit your network for unexpected open ports.

