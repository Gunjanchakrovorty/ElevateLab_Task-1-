
# 🔍 Task 1 – Network Port Scanning with Nmap

![nmap](https://img.shields.io/badge/Nmap-TCP_SYN_Scan-blue) ![Wireshark](https://img.shields.io/badge/Wireshark-Optional_Analysis-informational) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 🧠 Task Overview

This task was part of the **12th Gurugram Police Cyber Security Internship 2025**, focused on gaining hands-on experience in **network reconnaissance** by scanning for open ports using `Nmap`.

---

## 🛠️ Tools Used

| Tool       | Purpose                               |
|------------|----------------------------------------|
| Nmap       | Port scanning and reconnaissance       |
| Wireshark  | (Optional) Traffic packet analysis     |
| Ubuntu     | Linux-based environment (VM)           |
| Terminal   | Executing commands and scans           |

---

## 🔍 Commands Used

```bash
# Install Nmap
sudo apt install nmap

# Check network interfaces
ip a | grep inet

# TCP SYN Scan on loopback
sudo nmap -sS 127.0.0.1/8
```

📝 **Note**: Use `/24` for scanning all devices in a subnet, e.g. `192.168.0.0/24`

---

## 📸 Screenshots & Output

| Description                  | File                  |
|------------------------------|------------------------|
| 🔍 Nmap Scan Result          |![linux nmap](https://github.com/user-attachments/assets/f2e324d0-04e6-4243-baf2-da543ebf87ea)|
| 🌐 IP Configuration          | ![ip linux](https://github.com/user-attachments/assets/189628f1-0a31-4f27-a002-dd248a479512)         |
---

## 📊 Scan Output Summary

- **Target Range Scanned**: `127.0.0.1/8`
- **Discovered Open Ports**:
  - `631/tcp` – Internet Printing Protocol (IPP)
- **TCP SYN Scan**:
  - Quick and stealthy
  - Doesn’t complete full TCP handshake

---

## 🔐 Security Insights

- **Port 631 (IPP)**: Commonly used for printing services, can be vulnerable if exposed externally.
- **Open Ports = Attack Surface**: Every open port can be a way in for malicious users.

---

## 🎓 Learning Takeaways

- How to **install and use Nmap**
- Understand **IP ranges and subnets**
- Perform and interpret a **TCP SYN scan**
- Use **Wireshark** to inspect traffic
- Understand **real-world risk** from open ports

---

## 📚 Useful Resources

- [Nmap Official Guide](https://nmap.org/book/man.html)
- [Wireshark Basics](https://www.wireshark.org/docs/wsug_html_chunked/)
- [Common TCP Ports](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)
