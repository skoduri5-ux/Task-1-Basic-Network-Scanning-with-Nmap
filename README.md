# Task-1-Basic-Network-Scanning-with-Nmap
Performing the network scan using nmap.

# Basic Network Scanning with Nmap

## Objective
The objective of this task is to perform network scanning using Nmap to identify open ports and running services on a target machine.

---

## Environment Used

- Operating System: Ubuntu (WSL)
- Tool Used: Nmap
- Target IP: 192.168.141.105

---

## Commands Used

### 1. Host Discovery

```bash
nmap -sn 192.168.141.105
```

Purpose:
Checks whether the target host is active on the network.

---

### 2. Port Scan

```bash
nmap 192.168.141.105
```

Purpose:
Scans the target for common open TCP ports.

---

### 3. Service Version Detection

```bash
nmap -sV 192.168.141.105
```

Purpose:
Identifies services and versions running on open ports.

---

### 4. Specific Port Scan

```bash
nmap -p 8080 -sV 192.168.141.105
```

Purpose:
Scans port 8080 and detects the running HTTP service.

---

## Findings

| Port | State | Service | Description |
|------|-------|----------|-------------|
| 8080 | Open | HTTP | Python temporary web server |

---

## Explanation of Open Port

### Port 8080
Port 8080 is commonly used for HTTP web services and development servers. In this task, a Python HTTP server was started locally using:

```bash
python3 -m http.server 8080
```

Nmap successfully detected the running service on this port.

---

## Output File

The scan results were saved using:

```bash
nmap -p 8080 -sV 192.168.141.105 -oN nmap_scan_results.txt
```
<img width="1706" height="266" alt="Screenshot 2026-05-27 161200" src="https://github.com/user-attachments/assets/a87426a6-174e-418d-8bab-c3db2479507d" />

---

## Screenshots Included

- Host discovery scan
- Port scanning output
- Service detection output

---

## Conclusion

Nmap successfully identified active hosts, scanned open ports, and detected services running on the target system. This task demonstrated basic network reconnaissance and service enumeration techniques using Nmap.
