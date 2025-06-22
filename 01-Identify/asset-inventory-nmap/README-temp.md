# 🧠 Asset Inventory using Nmap

This lab demonstrates how to use **Nmap** to identify assets and services on a local network — aligning with the **Identify (ID)** function of the NIST Cybersecurity Framework (CSF), specifically **ID.AM-1** and **ID.AM-2**.

---

## 🎯 Objectives

- Identify active devices on a local network
- Discover open ports and services
- Save scan output for future use
- Map results to NIST CSF subcategories

---

## 🛠️ Tools Used

| Tool  | Purpose |
|-------|---------|
| `Nmap` | Network discovery, OS/service detection |
| `ip a` | Check local IP address/subnet |
| `Terminal` | Command-line interface (Linux/macOS/WSL) |

---

## 🧪 Steps Performed

### 1. ✅ Find Your Network Range

Run:
```bash
ip a

Look for something like:  
`inet 192.168.1.14/24` → This means your subnet is `192.168.1.0/24`

### 2. 🔍 Discover Active Devices (Ping Scan)

Once you know your subnet (e.g., `192.168.1.0/24`), the next step is to scan your network to find **all live (online) devices**. This helps build an inventory of active IP addresses on your local network — such as routers, laptops, phones, printers, smart TVs, virtual machines, and more.

Run the following command in your terminal:

```bash
sudo nmap -sP 192.168.1.0/24
🔎 Explanation:
sudo — Runs the command with administrative privileges (required for certain network scans)

nmap — The network scanner tool

-sP — Performs a "ping scan" to see which hosts respond; this is a quick way to find active devices

192.168.1.0/24 — The subnet you're scanning (replace with your actual local subnet if different)
✅ What You’ll See:
Nmap will return a list of IP addresses with lines like:
Nmap scan report for 192.168.1.1
Host is up (0.0030s latency).
MAC Address: AA:BB:CC:DD:EE:FF (Vendor)
Each of these indicates a live device. You’re now starting your asset inventory — which is the goal of this lab and ties directly to NIST CSF subcategory ID.AM-1 ("Physical devices are inventoried").

### 3. 📦 Perform a Service and Port Scan (Deeper Asset Info)

Now that you’ve discovered which devices are online, the next step is to learn **what software/services** those devices are running, and possibly identify their **operating systems**. This helps build a more detailed inventory of your network.

Run the following command:

```bash
sudo nmap -sV -O -T4 192.168.1.0/24

🔎 Explanation:
sudo — Runs with admin permissions (some scans require root access)
-sV — Enables service version detection (e.g., Apache 2.4.41, OpenSSH 8.0)
-O — Tries to detect the operating system (e.g., Windows 10, Linux, etc.)
-T4 — Increases the scan speed (suitable for local networks)

192.168.1.0/24 — Replace with your actual subnet if needed
🧾 Sample Output (example):
PORT     STATE SERVICE     VERSION
22/tcp   open  ssh         OpenSSH 8.2p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
80/tcp   open  http        Apache httpd 2.4.41
443/tcp  open  ssl/https   OpenSSL 1.1.1f
MAC Address: AA:BB:CC:DD:EE:FF (Vendor)
Device type: general purpose
Running: Linux 5.X

#### 📌 Why This Matters (NIST CSF Tie-In):

This deeper level of scanning supports:

- **ID.AM-2**: You are identifying **software platforms** in use across your devices
- You can detect **unauthorized or unexpected services**, like:
  - A telnet server (insecure)
  - An unknown web server
  - An open database exposed to the network

These findings help inform later steps like risk assessment and protection.

### 4. 💾 Save and Export Scan Results (Optional but Recommended)

To keep a record of your scan for reporting, future reference, or importing into analysis tools, you can export the Nmap results as a file.

Run the command below to save your scan in **XML format**:

```bash
sudo nmap -sV -O 192.168.1.0/24 -oX scan-results.xml

📌 Why This Matters (NIST CSF Tie-In)
Saving and reviewing the results supports the ongoing process of:

Building a repeatable asset inventory process (ID.AM-1, ID.AM-2)

Supporting future risk assessments (ID.RA)

Showing a practical, well-documented approach to asset management
“Without documentation, discoveries disappear. Export your findings.”

