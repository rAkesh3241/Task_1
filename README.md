# Task_1


1. Scan of 192.168.142.1
The scan of this host revealed a single open port: 3306/tcp, which is commonly associated with MySQL database services. This suggests the machine might be hosting a database server. The remaining 999 ports were filtered, meaning they either dropped incoming probes or were blocked by a firewall, leaving their status ambiguous. The host responded almost instantly (0.00018s latency), and its MAC address (00:50:56:C0:00:08) confirms it’s a VMware virtual machine. The lack of other detectable services implies this system could be a dedicated database host with strict access controls.

2. Scan of 192.168.142.134 
This host, identified as dc-2, had only one open port: 80/tcp (HTTP), indicating it’s likely running a web server. The other 999 ports were closed (responded with resets), meaning no services were actively listening on them. The negligible latency (0.000063s) and VMware MAC address (00:0C:29:10:D5:A4) suggest it’s part of the same virtualized lab environment. The absence of HTTPS (443/tcp) or SSH (22/tcp) might imply either a minimal web service or potential security hardening (e.g., SSH disabled to reduce attack surface).

3. Scan of 192.168.142.131
This machine showed two open ports:

80/tcp (HTTP)

443/tcp (HTTPS)
Both are tied to web traffic, hinting at a web server with encrypted traffic support. Notably, SSH (22/tcp) was closed, which could mean remote administration isn’t enabled or is restricted. The 997 filtered ports (no response) might indicate firewall rules silently dropping probes. The MAC address (00:0C:29:C3:10:B1) aligns with VMware, and the fast response time (0.00018s) places it on the same local network. The presence of HTTPS suggests sensitive data could be handled here.

4. Scan of 192.168.142.133
This host had three open ports:

22/tcp (SSH): Allows secure remote shell access.

80/tcp (HTTP): Hosts a web service.

111/tcp (RPCbind): Used for remote procedure calls, often tied to NFS or other distributed services.
The 997 closed ports (reset responses) confirm no other services are active. The MAC address (00:00:29:77:35:26) again points to VMware. SSH being open suggests this machine is configured for remote administration, while RPCbind’s presence could imply file-sharing or inter-process communication—though this service can pose security risks if misconfigured.
