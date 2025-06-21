# nist-csf-labs
# 🔐 NIST Cybersecurity Framework (CSF) Labs & Projects

Welcome! This repository contains a collection of practical, hands-on cybersecurity labs and mini-projects mapped to the **NIST Cybersecurity Framework (CSF) 2.0**. The goal is to simulate real-world scenarios using open-source tools and to document each lab in a clear, repeatable, and informative way.

---

## 🎯 Goals

- 📚 **Apply NIST CSF concepts** in real-world cybersecurity environments.
- ⚙️ **Use industry tools** (Wazuh, Zeek, TheHive, YARA, etc.) across all CSF Functions.
- 📁 **Create 20+ labs/projects** to showcase in a professional GitHub portfolio.
- 📄 **Document clearly** using Markdown, diagrams, risk assessments, and logs.
- 🚀 **Build a roadmap** for cybersecurity learning and job-readiness.

---

## 📊 NIST CSF 2.0: Function Breakdown

| Function    | Description                                       | Sample Labs                                      |
|-------------|---------------------------------------------------|--------------------------------------------------|
| 🧭 Govern    | Governance, policies, and risk management         | Risk register, policy templates                  |
| 🧱 Identify  | Understanding assets and risk                     | Asset inventory, threat modeling                 |
| 🔒 Protect   | Safeguards and access control                     | IAM policy, encryption setup, MFA config         |
| 👀 Detect    | Monitoring and anomaly detection                  | File integrity monitoring, SIEM alerts           |
| 🚨 Respond   | Incident handling and mitigation                  | IR playbooks, incident analysis, IOC handling    |
| 🔁 Recover   | Restoration of systems and learning from incidents| Backup simulation, recovery testing              |

---

## 🧪 Lab Tracker (📌 Work in Progress)

| Lab Name                               | Function   | Status   |
|----------------------------------------|------------|----------|
| Asset Inventory with Nmap              | Identify   | ✅ Done  |
| Risk Register with Excel/Markdown      | Govern     | ✅ Done  |
| File Monitoring using Wazuh            | Detect     | 🔄 In Progress |
| IAM Role-Based Access Control (AWS)    | Protect    | 🕒 Planned |
| IR Workflow with TheHive               | Respond    | 🕒 Planned |
| Snapshot Restore Simulation (VM)       | Recover    | 🕒 Planned |

---

## 🛠 Toolset Across Labs

| Category       | Tools Used                                                                 |
|----------------|---------------------------------------------------------------------------|
| 📋 Risk & Policy | Excel, Markdown, NIST templates                                           |
| 🌐 Scanning      | `nmap`, `masscan`, `Shodan`                                               |
| 🛡 Protection    | `AWS IAM`, `iptables`, `ufw`, `OpenSSL`, MFA tools                        |
| 🔍 Monitoring    | `Wazuh`, `Zeek`, `Suricata`, `ELK Stack`                                  |
| ⚠️ Incident Resp | `TheHive`, `Cortex`, `Velociraptor`, `Wireshark`, `YARA`                  |
| 💾 Recovery      | `Veeam`, `Rsync`, VM snapshots, cloud backups                             |
| 📄 Docs & Infra  | `Markdown`, `GitHub Pages`, `Draw.io`, `Excel`, `Typora`                  |

---

<pre> ### 🧱 Folder Structure ``` nist-csf-labs/ ├── 01-Identify/ │ └── asset-inventory-nmap/ ├── 02-Protect/ ├── 03-Detect/ ├── 04-Respond/ ├── 05-Recover/ ├── 06-Govern/ ├── 00-Templates/ └── 07-Lab-Tracker.md ``` </pre>



Each lab includes:
- 📄 A README with context, tools, and step-by-step instructions  
- 📸 Screenshots of configuration or results  
- 📁 Logs, configs, and outputs (when possible)  
- ✅ CSF subcategory mapping and lessons learned

---

## 💬 Contributing & Feedback

This repository is part of a personal journey to learn and demonstrate practical cybersecurity skills aligned with NIST CSF. If you have suggestions, lab ideas, or feedback — feel free to open an issue or fork the repo!

---

## 📅 Roadmap

- [ ] 10 Labs Completed by [📆 Date Goal]
- [ ] Publish to GitHub Pages for public viewing
- [ ] Write blog-style breakdowns of 3 key labs
- [ ] Convert risk register to interactive dashboard

---

> _"Security is a process, not a product."_ – Bruce Schneier

