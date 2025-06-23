# Detect Function – Nmap Network Scan Lab

This lab aligns with the **Detect** function of the NIST Cybersecurity Framework (CSF). It focuses on identifying active devices and open ports on a network using `nmap`.

## 🔍 Purpose
To demonstrate how to use `nmap` for:
- Scanning a local network to detect live hosts
- Identifying open ports and services
- Understanding basic network visibility for threat detection

## 🛠️ Tools Used
- **Nmap**: A powerful network scanning tool
- **Mac Terminal**: Local environment for running commands
- **Homebrew**: Used to install nmap

---

## 🧪 Lab Steps

### ✅ 1. Install Homebrew and Nmap
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install nmap
```
If brew isn't recognized, run:
eval "$(/opt/homebrew/bin/brew shellenv)"

### ✅ 2. Identify Local IP Address
```
ifconfig | grep inet
```
📸 See Screenshot 1: Shows the local IP address 10.0.0.22

### ✅ 3. Discover Active Hosts on Network
```
nmap -sn 10.0.0.0/24
```
📸 See Screenshot 2: Displays a list of live hosts

### ✅ 4. Detect Open Ports and Services
```
nmap -sV -T4 10.0.0.0/24
```

#### ✅ Outcome
- 12 hosts detected
- Open ports and services identified on active devices
- Practical understanding of how detection tools can inform threat monitoring

####🧠 NIST CSF Alignment
- Detect	Anomalies & Events	DE.AE-1: A baseline of network operations is established
- Detect	Security Monitoring	DE.CM-1: The network is monitored to detect potential cybersecurity events
