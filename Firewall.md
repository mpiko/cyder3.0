
```bash
#!/bin/bash

# Flush all existing rules
iptables -F
iptables -X
iptables -t nat -F
iptables -t nat -X
iptables -t mangle -F
iptables -t mangle -X

# Allow loopback traffic
iptables -A INPUT -i lo -j ACCEPT
iptables -A OUTPUT -o lo -j ACCEPT

# Allow established and related incoming traffic
iptables -A INPUT -m conntrack --ctstate ESTABLISHED,RELATED -j ACCEPT

# Allow all outgoing traffic
iptables -A OUTPUT -j ACCEPT

# Allow incoming traffic on port 22 (SSH)
iptables -A INPUT -p tcp --dport 22 -j ACCEPT

# Allow incoming traffic on port 80 (HTTP)
iptables -A INPUT -p tcp --dport 80 -j ACCEPT

# Allow incoming traffic on port 443 (HTTPS)
iptables -A INPUT -p tcp --dport 443 -j ACCEPT

# Allow ICMP (ping)
iptables -A INPUT -p icmp -j ACCEPT

# Apply security hardening

# Protect against SYN flood attacks
iptables -A INPUT -p tcp ! --syn -m conntrack --ctstate NEW -j DROP
iptables -A INPUT -p tcp --tcp-flags ALL NONE -j DROP
iptables -A INPUT -p tcp --tcp-flags SYN,FIN SYN,FIN -j DROP
iptables -A INPUT -p tcp --tcp-flags SYN,RST SYN,RST -j DROP

# Protect against ping flood (limit to 1 ping per second with burst of 3)
iptables -A INPUT -p icmp --icmp-type echo-request -m limit --limit 1/s --limit-burst 3 -j ACCEPT

# Protect against IP spoofing
iptables -A INPUT -s 10.0.0.0/8 -j DROP
iptables -A INPUT -s 172.16.0.0/12 -j DROP
iptables -A INPUT -s 192.168.0.0/16 -j DROP
iptables -A INPUT -s 127.0.0.0/8 -j DROP
iptables -A INPUT -s 224.0.0.0/4 -j DROP
iptables -A INPUT -s 240.0.0.0/5 -j DROP
iptables -A INPUT -s 0.0.0.0/8 -j DROP
iptables -A INPUT -s 169.254.0.0/16 -j DROP

# Log dropped packets (optional)
iptables -A INPUT -m limit --limit 5/min -j LOG --log-prefix "iptables denied: " --log-level 7

# Drop all other inbound traffic
iptables -A INPUT -j DROP

# End of script
```