# OdooXG — Enterprise DevOps Deployment Guide

<div align="center">

![DevOps](https://img.shields.io/badge/DevOps-Enterprise-blue?style=for-the-badge)
![Odoo](https://img.shields.io/badge/Odoo-v18%20%7C%20v19-green?style=for-the-badge&logo=odoo)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**Professional Enterprise-Grade Odoo Deployment Guide**

[**🚀 OPEN LIVE GUIDE →**](https://felaya.github.io/OdooXG/){:target="_blank"}

*(All links open in new tabs for seamless workflow)*

</div>

---

## 📖 About This Guide

A **comprehensive, production-ready DevOps deployment guide** for Odoo ERP systems. This single-file HTML resource covers everything from installation to troubleshooting, following enterprise best practices for scalability, security, and reliability.

Designed for **DevOps Engineers, System Administrators, and Technical Leads** managing Odoo deployments in enterprise environments.

---

## 📚 Complete Guide Contents

### ⚡ Part 0: Odoo 19 Key Changes
Understanding critical changes before deployment:
- Network parameters: `longpolling_port` → `gevent_port`, `xmlrpc_port` → `http_port`
- Controllers: `type='json'` → `type='jsonrpc'`
- ORM: `name_get()` removed, `read_group()` deprecated
- Security: `res.groups` restructured to privilege-based model

### 🚀 Part 1: Installation
Complete production installation walkthrough:
- **Hardware Requirements** — Worker calculations (`(CPU × 2) + 1`), RAM sizing (150-300MB per worker)
- **Installation Steps** — From prerequisites to verification
- **Configuration** — Production-hardened `odoo.conf` (single DB, localhost binding, workers)
- **Nginx + SSL** — Reverse proxy, SSL termination, upload limits, caching
- **PostgreSQL Tuning** — Memory allocation, SSD optimization, `jit = off` critical setting
- **Post-Install Verification** — Service checks and validation commands

### 🖥️ Part 2: Multi-Instance Setup
Run multiple Odoo instances on one server:
- **Staging Environments** — Parallel instances for testing
- **Port Allocation** — Managing multiple services with different ports
- **Community Edition Side-by-Side** — Licensed and non-licensed workloads together

### ⚙️ Part 3: Operations
Day-to-day operational procedures:
- **Safe Update Procedure** — Backup → Stop → Fetch → Update → Clear Cache → Start
- **Automated Backups** — PostgreSQL dumps + filestore synchronization scripts
- **Database Restore** — Same-server and cross-server recovery procedures
- **Database Cloning** — Staging copies with neutralization (prevent emails/crons)
- **Enterprise License** — Subscription management, `database.uuid`, user tracking
- **Service Management** — systemctl and journalctl essential commands
- **Odoo Shell Recipes** — Python REPL with ORM access for data operations
- **Quick Commands Reference** — Essential CLI snippets for daily tasks

### 🛠️ Part 4: Troubleshooting & Diagnostics
Problem resolution and diagnostics:
- **Common Issues** — Connection errors, worker crashes, permission problems
- **Odoo 19 Specific Issues** — Migration pitfalls and version-specific solutions
- **Diagnostics** — Log analysis, performance profiling techniques
- **Emergency Procedures** — Critical failure recovery steps

### 📚 Part 5: Reference
Essential reference materials:
- **Configuration Reference** — Complete `odoo.conf` parameter documentation
- **Production Checklist** — Pre-launch verification items table
- **Directory Structure** — File layout for v18/v19 Community & Enterprise
- **Windows Guide** — Command-line reference for Windows `.exe` installations

---

## 🎯 Who Should Use This Guide

| Role | Primary Use Cases |
|------|------------------|
| **DevOps Engineers** | Production deployments, automation, monitoring setup |
| **System Administrators** | Daily operations, backups, updates, troubleshooting |
| **Technical Leads** | Architecture planning, multi-environment strategies |
| **Developers** | Local development setup, debugging, shell operations |

---

## 🛠️ Technologies & Platforms Covered

<div align="center">

![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04%20%7C%2024.04-orange?style=flat-square&logo=ubuntu)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-14+-blue?style=flat-square&logo=postgresql)
![Nginx](https://img.shields.io/badge/Nginx-Reverse%20Proxy-green?style=flat-square&logo=nginx)
![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![Systemd](https://img.shields.io/badge/Systemd-Service%20Management-purple?style=flat-square)
![Git](https://img.shields.io/badge/Git-Version%20Control-red?style=flat-square&logo=git)
![Linux](https://img.shields.io/badge/Linux-Ubuntu%2FDebian-yellow?style=flat-square&logo=linux)
![Windows](https://img.shields.io/badge/Windows-Installer%20Guide-blue?style=flat-square&logo=windows)

</div>

---

## 📋 Quick Start

1. **[Open the Live Guide](https://felaya.github.io/OdooXG/)**{:target="_blank"} in your browser
2. **Navigate Sections** — Use the interactive Table of Contents with search functionality
3. **Follow Step-by-Step** — Each section includes copy-ready commands and configurations
4. **Bookmark References** — Quick access for ongoing operations and troubleshooting

> 💡 **Pro Tip**: The guide is designed as a single HTML file with no external dependencies. All internal and external links open in new tabs, allowing you to keep the guide accessible while implementing changes.

---

## 🔧 Key Features

✅ **Production-Ready Configurations** — Hardened settings for security and performance  
✅ **Odoo 18 & 19 Coverage** — Complete migration notes and version-specific guidance  
✅ **Multi-Environment Support** — Production, staging, and development setups  
✅ **Interactive Navigation** — Searchable TOC, smooth scrolling, glass-morphism UI  
✅ **Copy-Ready Code** — All commands and configs ready to paste into terminal  
✅ **Comprehensive Troubleshooting** — Common issues with step-by-step resolutions  
✅ **New Tab Workflow** — All links open in new tabs for uninterrupted work  
✅ **Single File Format** — No dependencies, works offline once loaded  

---

## 📄 Repository Structure

```
OdooXG/
├── index.html          # Complete HTML guide (single-file, no dependencies)
├── README.md           # This README file
└── .git/               # Git repository metadata
```

---

## 🤝 Contributing

Contributions are welcome! If you find errors, have improvements, or want to add sections:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request with your changes

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE){:target="_blank"}.

---

## 🔗 Important Links

<div align="center">

[**🌐 Live Guide Preview →**](https://felaya.github.io/OdooXG/){:target="_blank"} &nbsp;•&nbsp; 
[**📦 GitHub Repository →**](https://github.com/felaya/OdooXG){:target="_blank"} &nbsp;•&nbsp; 
[**📖 Odoo Official Docs →**](https://www.odoo.com/documentation){:target="_blank"}

</div>

---

<div align="center">

**Built for enterprise DevOps teams deploying Odoo at scale.**

*All links in this README and the guide open in new tabs for seamless navigation.*

</div>
