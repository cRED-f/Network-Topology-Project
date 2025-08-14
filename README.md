# 🖧 Network Topology Project

## 📌 Overview
In this project, we designed and implemented a network consisting of three routers, two switches, a DHCP server, and four end-user devices. Our goal was to create a segmented and scalable network with proper IP address management and efficient inter-subnet communication.

---

## 🛠 Network Components
### Routers
We configured **three Cisco 1941 routers**, each responsible for connecting and routing between different subnets:
- **Router1**: 192.168.1.0, 10.0.0.0, 12.0.0.0
- **Router2**: 192.168.2.0, 11.0.0.0, 12.0.0.0
- **Router3**: 192.168.3.0, 10.0.0.0, 11.0.0.0

### Switches
- **Switch0**: Connected to Router1, PC0, and DHCP Server (192.168.1.0 subnet)
- **Switch2**: Connected to Router3, PC2, and Laptop0 (192.168.3.0 subnet)

### End-User Devices
- **PC0** → 192.168.1.x (via DHCP)
- **PC1** → 192.168.2.x (Static IP)
- **PC2** → 192.168.3.x (via DHCP)
- **Laptop0** → 192.168.3.x (via DHCP)

### DHCP Server
- **IP Address**: 192.168.1.3  
- Configured to assign dynamic IPs in all three subnets:  
  - **serverPool** → 192.168.1.4 – 20 users  
  - **two** → 192.168.2.3 – 20 users  
  - **three** → 192.168.3.2 – 20 users  

---

## 🌐 Subnets Used
- 192.168.1.0
- 192.168.2.0
- 192.168.3.0
- 10.0.0.0
- 11.0.0.0
- 12.0.0.0

---

## 📊 IP Address Summary

| Device        | Subnet/Interface      | IP Address                |
|---------------|-----------------------|---------------------------|
| Router1       | LAN to Switch0        | 192.168.1.0               |
|               | Link to Router3       | 10.0.0.0                  |
|               | Link to Router2       | 12.0.0.0                  |
| Router2       | LAN to PC1             | 192.168.2.0               |
|               | Link to Router3       | 11.0.0.0                  |
|               | Link to Router1       | 12.0.0.0                  |
| Router3       | LAN to Switch2         | 192.168.3.0               |
|               | Link to Router1        | 10.0.0.0                  |
|               | Link to Router2        | 11.0.0.0                  |
| PC0           | LAN to Switch0         | 192.168.1.x (via DHCP)    |
| PC1           | Direct to Router2      | 192.168.2.x               |
| PC2           | LAN to Switch2         | 192.168.3.x (via DHCP)    |
| Laptop0       | LAN to Switch2         | 192.168.3.x (via DHCP)    |
| DHCP Server   | LAN to Switch0         | 192.168.1.3               |

---

## 📝 Conclusion
We designed this network to ensure efficient traffic flow and scalability. By dividing it into six subnets, we improved organization and routing efficiency. Our DHCP server automates IP allocation across all subnets, reducing manual configuration and errors. With support for up to 20 devices per subnet, this design meets current needs and allows for future expansion while maintaining robust connectivity and stability.

---

## 📷 Network Diagram
<img width="793" height="512" alt="image" src="https://github.com/user-attachments/assets/f4b9176c-6802-416d-8621-5c928ef9c74a" />






