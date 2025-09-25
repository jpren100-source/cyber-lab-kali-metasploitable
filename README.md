# Cybersecurity Homelab: Kali Linux & Metasploitable 2

## Lab Purpose
This lab provides a safe, isolated environment for practicing cybersecurity and penetration testing techniques. It uses Kali Linux as the attacker system and Metasploitable 2 as the vulnerable target system. The lab allows testing of network scanning, vulnerability assessment, and other common security tasks without affecting real systems.

---

## Setup Steps

### 1. Virtual Machine Configuration

**Kali Linux VM:**  
- RAM: 2 GB  
- CPU: 2 cores  
- Network Adapter 1: NAT (for internet access)  
- Network Adapter 2: Host-Only Adapter (for lab network)  

**Metasploitable 2 VM:**  
- RAM: 512 MB  
- CPU: 1 core  
- Network Adapter 1: Host-Only Adapter (for lab network only)  

Both VMs are run in VirtualBox on the host PC.

---

### 2. Host-Only Network Setup

1. Open VirtualBox → File → Host Network Manager.  
2. Create a Host-Only network (example: `VirtualBox Host-Only Ethernet Adapter`).  
   - IP: `192.168.56.1`  
   - Enable DHCP server (optional).  
3. Connect Kali and Metasploitable VMs to this network via Adapter 2.

---

### 3. IP Addresses of VMs

- **Kali Linux:** `192.168.56.101`  
- **Metasploitable 2:** `192.168.56.102`  

You can verify IP addresses using `ifconfig` or `ip addr` in Linux.

---

### 4. Tools Used

- **Nmap:** For scanning open ports and services on Metasploitable 2.  
- **Ping:** To verify network connectivity between VMs.  
- **VirtualBox:** For VM management and networking.  
- **Optional:** Other Kali tools for future testing (Metasploit, Nikto, etc.).

---

### 5. How to Reproduce the Lab

1. Download and install VirtualBox on the host machine.  
2. Import the Kali Linux VM and Metasploitable 2 VM into VirtualBox.  
3. Configure RAM, CPU, and network adapters as specified above.  
4. Create a Host-Only network and connect both VMs.  
5. Start both VMs and verify network connectivity with `ping`.  
6. Run Nmap scans from Kali Linux against the Metasploitable 2 IP.  
7. Save results and screenshots to the project folder for documentation.

---

This lab setup provides a foundation for hands-on cybersecurity practice and can be expanded with additional tools and exercises.
