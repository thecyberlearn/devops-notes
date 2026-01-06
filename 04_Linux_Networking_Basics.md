# Linux – Networking Basics (Day 4)

## What is Networking in Linux?
Networking means how computers and servers communicate with each other
using IP addresses, ports, and protocols.

Every DevOps engineer must understand networking
because applications run on networks.

---

## Why Networking is Important for DevOps?
If networking fails:
- app will not open
- server looks “down”
- deployment fails

Most DevOps issues are actually network issues.

---

## IP Address
An IP address identifies a machine on a network.

Check IP:
```bash
ip a
```
or
```bash
ifconfig
```

---

## Hostname
```bash
hostname
```

---

## Ping Command
```bash
ping google.com
```
Stop ping:
```bash
Ctrl + C
```

---

## curl Command (VERY IMPORTANT)
```bash
curl google.com
curl -I google.com
```

---

## wget Command
```bash
wget https://example.com/file.txt
```

---

## Ports (CRITICAL CONCEPT)
Common ports:
- 22 → SSH
- 80 → HTTP
- 443 → HTTPS
- 3306 → MySQL

---

## Check Open Ports
```bash
netstat -tuln
```
or
```bash
ss -tuln
```

---

## Check Which Process Uses a Port
```bash
sudo netstat -tulnp
```

---

## DNS Resolution
```bash
nslookup google.com
dig google.com
```

---

## Test Server Connectivity
```bash
telnet google.com 80
```

---

## Real DevOps Scenario
Commands used:
```bash
curl
ping
netstat
ss
```

---

## Common Mistakes
- Forgetting port number
- Confusing localhost and public IP

---

## DevOps Rule
If something doesn’t work → check network first.

---

## Summary
Linux networking basics: IP, ports, ping, curl, DNS, and open ports.
