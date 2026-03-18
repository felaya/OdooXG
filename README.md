# OdooXG — Enterprise Deployment Guide

<div align="center">

![DevOps](https://img.shields.io/badge/DevOps-Enterprise-blue?style=for-the-badge)
![Odoo](https://img.shields.io/badge/Odoo-v18%20%7C%20v19-green?style=for-the-badge&logo=odoo)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**Professional Enterprise-Grade Odoo Installation & Deployment Guide**

[**🚀 OPEN LIVE GUIDE →**](https://felaya.github.io/OdooXG/)

*(Note: GitHub Markdown doesn't support forcing links to open in new tabs. Right-click or middle-click links to open in a new tab.)*

</div>

---

## 📖 About This Guide

A **comprehensive, production-ready DevOps deployment guide** for Odoo ERP installation and management. This single-file HTML resource covers everything from initial Odoo installation on Ubuntu/Debian to advanced multi-instance scaling, following enterprise best practices for security, performance, and reliability.

Designed for **DevOps Engineers, System Administrators, and Technical Leads** managing Odoo installations and deployments in enterprise environments.

**SEO Keywords**: Odoo installation guide, Odoo 19 deployment, Odoo production setup, Ubuntu Odoo install, PostgreSQL Odoo configuration, Nginx reverse proxy Odoo, Odoo worker configuration, enterprise Odoo scaling, Odoo backup strategies, Odoo troubleshooting.

---

## 📚 Complete Guide Contents

### ⚡ Part 0: Odoo 19 Key Changes
Understanding critical changes before deployment:
- Network parameters: `longpolling_port` → `gevent_port`, `xmlrpc_port` → `http_port`
- Controllers: `type='json'` → `type='jsonrpc'`
- ORM: `name_get()` removed, `read_group()` deprecated
- Security: `res.groups` restructured to privilege-based model

### 🚀 Part 1: Odoo Installation Guide
Complete production installation walkthrough with security best practices:
- **Hardware Requirements** — Worker calculations (`(CPU × 2) + 1`), RAM sizing (150-300MB per worker)
- **Prerequisites** — Ubuntu/Debian setup, system updates, dependency installation
- **Odoo Installation Steps** — Repository configuration, package installation, version selection (v18/v19)
- **Database Setup** — PostgreSQL installation, user creation with secure random passwords, database initialization
- **Configuration Best Practices** — Production-hardened `odoo.conf` (single DB, localhost binding, workers, secure session management)
- **Nginx Reverse Proxy + SSL** — Let's Encrypt SSL certificates, reverse proxy configuration, upload limits, caching headers
- **PostgreSQL Performance Tuning** — Memory allocation, SSD optimization, `jit = off` critical setting, connection pooling
- **Security Hardening** — Firewall rules (UFW), fail2ban configuration, secure file permissions, no hardcoded credentials
- **Post-Install Verification** — Service status checks, log validation, connectivity tests

### 🖥️ Part 2: Multi-Instance Setup
Run multiple Odoo instances on one server with isolated configurations:
- **Staging Environments** — Parallel instances for testing with separate databases
- **Port Allocation Strategy** — Managing multiple services with different ports (http_port, gevent_port)
- **Community & Enterprise Side-by-Side** — Licensed and non-licensed workloads in isolated environments
- **Configuration Isolation** — Separate config files, log directories, and systemd services
- **Resource Management** — CPU and RAM allocation per instance to prevent resource contention

### ⚙️ Part 3: Operations
Day-to-day operational procedures with security-first approach:
- **Safe Update Procedure** — Backup → Stop → Fetch → Update → Clear Cache → Start (zero downtime strategy)
- **Automated Backups** — PostgreSQL dumps with encryption, filestore synchronization scripts, offsite backup rotation
- **Database Restore** — Same-server and cross-server recovery procedures with integrity validation
- **Database Cloning** — Staging copies with neutralization (prevent emails/crons), secure credential handling
- **Enterprise License Management** — Subscription management, `database.uuid`, user tracking, compliance monitoring
- **Service Management** — systemctl and journalctl essential commands, log rotation, service monitoring
- **Odoo Shell Recipes** — Python REPL with ORM access for secure data operations, no hardcoded credentials
- **Quick Commands Reference** — Essential CLI snippets for daily tasks with parameter placeholders

### 🛠️ Part 4: Troubleshooting & Diagnostics
Problem resolution and diagnostics without exposing sensitive data:
- **Common Issues** — Connection errors, worker crashes, permission problems with secure debugging
- **Odoo 19 Specific Issues** — Migration pitfalls, version-specific solutions, compatibility checks
- **Diagnostics Tools** — Log analysis (anonymized), performance profiling techniques, query optimization
- **Emergency Procedures** — Critical failure recovery steps, rollback strategies, incident response
- **Security Incident Response** — Breach detection, credential rotation, audit trail analysis

### 📚 Part 5: Reference
Essential reference materials with security best practices:
- **Configuration Reference** — Complete `odoo.conf` parameter documentation with secure defaults
- **Production Checklist** — Pre-launch verification items table (security, performance, backup validation)
- **Directory Structure** — File layout for v18/v19 Community & Enterprise with permission guidelines
- **Windows Guide** — Command-line reference for Windows `.exe` installations with security notes
- **Environment Variables** — Secure credential management using environment variables instead of hardcoded values
- **SSL/TLS Configuration** — Certificate management, renewal procedures, cipher suite recommendations

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

1. **[Open the Live Guide](https://felaya.github.io/OdooXG/)** in your browser
2. **Navigate Sections** — Use the interactive Table of Contents with search functionality
3. **Follow Step-by-Step** — Each section includes copy-ready commands and configurations
4. **Bookmark References** — Quick access for ongoing operations and troubleshooting

> 💡 **Pro Tip**: The guide is designed as a single HTML file with no external dependencies. Right-click or middle-click links to open them in new tabs, allowing you to keep the guide accessible while implementing changes.

---

## 🔧 Key Features

✅ **Production-Ready Configurations** — Hardened settings for security and performance  
✅ **Odoo 18 & 19 Coverage** — Complete migration notes and version-specific guidance  
✅ **Multi-Environment Support** — Production, staging, and development setups with isolation  
✅ **Interactive Navigation** — Searchable TOC, smooth scrolling, glass-morphism UI  
✅ **Copy-Ready Code** — All commands and configs ready to paste (with placeholder variables)  
✅ **Comprehensive Troubleshooting** — Common issues with step-by-step resolutions  
✅ **Single File Format** — No dependencies, works offline once loaded  
✅ **Security-First Approach** — No hardcoded passwords, domains, or credentials; uses environment variables  
✅ **SEO Optimized Content** — Rich keywords for Odoo installation, deployment, and DevOps practices  

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

This project is open source and available under the [MIT License](LICENSE).

---

## 🔗 Important Links

<div align="center">

[**🌐 Live Guide Preview →**](https://felaya.github.io/OdooXG/) &nbsp;•&nbsp; 
[**📦 GitHub Repository →**](https://github.com/felaya/OdooXG) &nbsp;•&nbsp; 
[**📖 Odoo Official Docs →**](https://www.odoo.com/documentation)

</div>

---

<div align="center">

**Built for enterprise DevOps teams deploying Odoo at scale.**

*Note: GitHub Markdown doesn't support forcing links to open in new tabs. Use right-click or middle-click to open links in new tabs.*

</div>
