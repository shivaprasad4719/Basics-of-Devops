## 🌐 Networking in Linux – Complete Guide

Networking in Linux is a core skill for System Administrators, DevOps Engineers, and Cloud Engineers.
This guide covers fundamental networking concepts, commands, configuration files, and troubleshooting tools used in Linux systems.

---

## 📌 What is Networking in Linux?

Linux networking allows systems to communicate with each other over a network using IP addresses, protocols, ports, and interfaces.
Linux provides powerful command-line tools to configure, monitor, and troubleshoot network connections.

---

## 🔹 Basic Networking Concepts

- Concept	Description
- IP Address	Unique identifier for a device on a network
- MAC Address	Hardware address of a network interface
- Port	Logical endpoint for communication
- Protocol	Rules for data transmission (TCP, UDP, ICMP)
- Gateway	Entry point to another network
- DNS	Resolves domain names to IP addresses
---

## 🔹 Network Interface Commands
<pre>
📍 Check Network Interfaces
ip addr
ifconfig
</pre>
<pre>
📍 Enable / Disable Interface
ip link set eth0 up
ip link set eth0 down
</pre>
<pre>
📍 Show Routing Table
ip route
route -n
</pre>
---

## 🔹 IP Address Management
📍 Assign IP Address (Temporary)
<pre>
ip addr add 192.168.1.100/24 dev eth0
</pre>

📍 Remove IP Address
<pre>
ip addr del 192.168.1.100/24 dev eth0
</pre>
## 🔹 Network Configuration Files
## 🔸 Debian / Ubuntu
<pre>
/etc/network/interfaces
/etc/netplan/*.yaml
</pre>

## 🔸 RHEL / CentOS
<pre>
/etc/sysconfig/network-scripts/ifcfg-*
</pre>
---

## 🔹 DNS Configuration
📍 DNS Resolver File
<pre>
/etc/resolv.conf


Example:

nameserver 8.8.8.8
nameserver 8.8.4.4
</pre>

## 🔹 Hostname Configuration
📍 View Hostname
<pre>hostname</pre>

📍 Set Hostname
<pre>hostnamectl set-hostname linux-server</pre>  

## 🔹 Network Testing & Troubleshooting
🔧 Ping (Connectivity Test)
<pre>ping google.com</pre>

🔧 Traceroute (Path Tracking)
<pre>traceroute google.com</pre>

🔧 Check Open Ports
<pre>ss -tulnp
netstat -tulnp
</pre>
🔧 DNS Lookup
<pre>nslookup google.com
dig google.com
</pre>

## 🔹 File Transfer Commands
📦 SCP (Secure Copy)
<pre>scp file.txt user@remote:/path</pre>

📦 Rsync
<pre>rsync -avz source/ destination/</pre>

# 🔹 Firewall Basics
🔥 Check Firewall Status
<pre>ufw status
firewall-cmd --list-all
</pre>
🔥 Allow Port
<pre>ufw allow 22
firewall-cmd --add-port=80/tcp --permanent
</pre>

---

## 🔹 Important Networking Tools
<pre>
|Tool   |         |Purpose              |
|ping   |         |Test connectivity    |
|ip	    |         |Network configuration|
|ss     |         |Socket statistics    |
|curl   |         |Test HTTP endpoints  |
|wget   |         |Download files       |
|tcpdump|         |Packet analysis      |
</pre>

## 🔹 Common Networking Ports
<pre>
|Service|       |Port|
|SSH    |       | 22 |
|HTTP   |       | 80 |
|HTTPS	|       | 443|
|FTP    |       | 21 |
|DNS    |       | 53 |
</pre>
---
  
## 🎯 Why Learn Linux Networking?
<pre>
✔ Essential for DevOps & Cloud roles
✔ Required for Kubernetes, Docker & CI/CD
✔ Helps in troubleshooting production issues
✔ Foundation for AWS, Azure, GCP networking
  
</pre>
---

## 📚 Recommended Next Topics

- Advanced IP Routing
- NAT & Bridging
- Network Namespaces
- Linux Networking for Docker & Kubernetes

---

## ⭐ Conclusion

Linux networking skills are non-negotiable for modern infrastructure roles.
Practice these commands regularly to build strong networking fundamentals.

---

🔗 Connect & Learn More

If you find this useful, ⭐ star the repo and follow for more Linux & DevOps content.
