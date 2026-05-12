# Linux Networking Commands Cheat Sheet

# 1. `ifconfig`

## Definition
Used to **view and configure network interfaces**.

It helps check:
- IP address
- MAC address
- network Interfaces

## Syntax
```bash
ifconfig
```

## Common Flags
- `ifconfig` → Show active network interfaces
- `ifconfig -a` → Show all interfaces (including inactive)

## Example
```bash
ifconfig
```

---

# 2. `ip`

## Definition
Modern replacement for `ifconfig`.

Used to manage:
- IP addresses
- Network interfaces
- Routing tables

## Syntax
```bash
ip [option]
```

## Common Flags
- `ip addr` → Show IP addresses
- `ip a` → Short form of `ip addr`
- `ip link show` → Show interfaces

## Example
```bash
ip a
```

---

# 3. `ping`

## Definition
Checks whether another system/server is reachable.

It sends packets and waits for replies.

## Syntax
```bash
ping [host]
```

## Common Flags
- `ping google.com` → Check connection
- `ping -c 4 google.com` → Send 4 packets
- `ping -i 2 google.com` → Send packet every 2 seconds

## Example
```bash
ping -c 4 google.com
```

---

# 4. `hostname`

## Definition
Displays your system's hostname or IP address.

## Syntax
```bash
hostname
```

## Common Flags
- `hostname` → Show system name
- `hostname -I` → Show IP address

## Example
```bash
hostname -I
```

---

# 5. `lsof`

## Full Form
**List Open Files**

## Definition
Shows which process is using which file/resource.

Useful for:
- Finding process using a port
- Checking open files
- Troubleshooting stuck processes

## Common Flags
- `lsof` → Show all open files
- `lsof -i` → Show network connections
- `lsof -i :PORT` → Show process using specific port
- `lsof -u USER` → Show files opened by a user
- `lsof -p PID` → Show files opened by a process
- `lsof -t` → Show process IDs only

## Example
```bash
lsof -i :3000
```

---

# 6. `lspci`

## Full Form
**List PCI**

## Definition
Displays PCI hardware devices connected to the system.

Examples:
- Graphics card
- WiFi adapter
- Ethernet controller
- USB controller

## Common Flags
- `lspci` → Show all PCI devices
- `lspci -v` → Detailed device info
- `lspci | grep TEXT` → Search specific device

## Example
```bash
lspci
```

---

# 7. `netstat`

## Full Form
**Network Statistics**

## Definition
Displays:
- Active connections
- Open ports
- Routing table
- Listening services

## Syntax
```bash
netstat [option]
```

## Common Flags
- `netstat` → Show active connections
- `netstat -a` → Show all connections
- `netstat -t` → TCP connections
- `netstat -u` → UDP connections
- `netstat -l` → Listening ports
- `netstat -n` → Numeric addresses
- `netstat -p` → Show process info
- `netstat -r` → Routing table
- `netstat -s` → Protocol statistics

## Important
- `netstat -nultp` → Show listening TCP/UDP ports with process details

## Example
```bash
netstat -nultp
```

---

# 8. `ss`

## Full Form
**Socket Statistics**

## Definition
Modern and faster replacement for `netstat`.

## Common Flags
- `ss` → Show socket connections
- `ss -a` → Show all sockets
- `ss -t` → TCP sockets
- `ss -u` → UDP sockets
- `ss -l` → Listening sockets
- `ss -n` → Numeric addresses
- `ss -p` → Process info
- `ss -s` → Summary statistics

## Important
- `ss -nultp` → Show listening TCP/UDP ports with process details

## Example
```bash
ss -nultp
```

---

# 9. `nslookup`

## Definition
Finds the IP address of a domain.

## Syntax
```bash
nslookup [domain name ]
```

## Example
```bash
nslookup google.com
```

---

# 10. `traceroute`

## Definition
Shows the route packets take to reach a destination.

## Syntax
```bash
traceroute [host]
```

## Example
```bash
traceroute google.com
```

---

# 11. `curl`

## Definition
Transfers data from or to a server.

Useful for testing APIs and websites.

## Common Flags
- `curl URL` → Fetch webpage
- `curl -I URL` → Show headers
- `curl -O URL` → Download file

## Example
```bash
curl -I google.com
```

---

# 12. `wget`

## Definition
Downloads files from the internet.

## Common Flags
- `wget URL` → Download file
- `wget -c URL` → Resume download
- `wget -O file URL` → Save with custom name

## Example
```bash
wget https://example.com/file.zip
```

---

# 13. `ssh`

## Full Form
**Secure Shell**

## Definition
Used to securely connect to another computer/server remotely over a network.

It allows you to:

- Log in to remote systems
- Run commands remotely
- Manage servers
## Syntax
```bash
ssh username@host
```

---

## Common Flags

- `ssh user@host` → Connect to remote system
- `ssh -p PORT user@host` → Connect using custom port
- `ssh -i key.pem user@host` → Connect using private key

## Example

### Connect to a remote server
```bash
ssh ubuntu@192.168.1.10
```

---
