<p align="center">
  <img src="assets/banner.png" alt="Gophish Phishing Simulation Banner" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-blue.svg" alt="Version">
  <img src="https://img.shields.io/badge/Go-1.19+-00ADD8.svg?logo=go" alt="Go Version">
  <img src="https://img.shields.io/badge/Platform-Railway-0B0D0E.svg?logo=railway" alt="Platform">
  <img src="https://img.shields.io/badge/license-MIT-green.svg" alt="License">
  <img src="https://img.shields.io/badge/status-active-success.svg" alt="Status">
</p>

<p align="center">
  <i>A comprehensive guide to phishing attack simulation and employee security awareness using Gophish on Railway.</i>
</p>

---

## 🎯 Project Aim

> **"The best defense against phishing isn't technology — it's prepared people."**

In a world where **91% of cyberattacks begin with a phishing email**, organizations can no longer rely solely on spam filters and firewalls. This project aims to:

🛡️ **Empower organizations** to proactively test their human firewall before real attackers do

🎓 **Transform employees** from security vulnerabilities into security assets through hands-on learning

📊 **Provide measurable insights** into organizational security posture and awareness gaps

⚡ **Democratize security testing** by making enterprise-grade phishing simulation accessible to startups and small teams

Whether you're a security professional, IT administrator, or startup founder — this guide will help you build a culture of security awareness, one simulated phish at a time.

---

## 📑 Table of Contents

- [🔍 Overview](#-overview)
- [✨ Key Features](#-key-features)
- [🏗️ Architecture](#️-architecture)
- [🚀 Quick Start](#-quick-start)
- [🎓 Skills Demonstrated](#-skills-demonstrated)
- [🏆 Project Achievements](#-project-achievements)
- [📊 Key Metrics & Performance](#-key-metrics--performance)
- [🙏 Acknowledgments](#-acknowledgments)
- [🎬 Project Summary](#-project-summary)
- [📞 Contact & Support](#-contact--support)
- [📊 Project Stats](#-project-stats)

---

## 🔍 Overview

Phishing remains one of the most effective attack vectors for gaining unauthorized access to sensitive information including login credentials, financial records, and personal data. While anti-phishing technologies continue to evolve, the human element remains the weakest link in organizational security.

This project provides a complete guide to deploying **Gophish**, an open-source phishing framework, on **Railway** for conducting realistic phishing simulations and improving employee security awareness.

> ### 💡 Why Phishing Simulations?
> 
> Organizations like Google have successfully mitigated phishing attacks using hardware security keys, but they also heavily rely on **user awareness and preparation**. Phishing simulations help:
> - Educate employees about phishing tactics
> - Test organizational resilience to attacks
> - Identify security weaknesses
> - Reduce the risk of successful phishing attacks

---

## ✨ Key Features

### 🎯 Gophish Capabilities
- 📧 **Full HTML Editor** — Create realistic phishing email templates
- 👥 **Group Management** — Organize target users into groups
- ⏰ **Scheduled Campaigns** — Launch campaigns at optimal times
- 📊 **Real-time Tracking** — Monitor campaign results as they happen
- 📎 **Attachment Support** — Include files in phishing simulations
- 🌐 **Landing Pages** — Create convincing phishing landing pages

### ☁️ Railway Deployment Benefits
- 🚀 **One-Click Deploy** — Instant deployment with starter template
- 🔒 **Automatic TLS** — Built-in SSL/TLS certificate management
- 🌍 **Custom Domains** — Support for branded domain names
- 📈 **Auto-Scaling** — Handle campaigns of any size
- 🔄 **GitHub Integration** — Automatic deployments on push

### 📈 Analytics & Reporting
- 📉 **Click Tracking** — Monitor who clicked phishing links
- 📝 **Data Submission** — Track credential submissions
- 📧 **Email Opens** — Detect when emails are opened
- 📊 **Campaign Dashboard** — Comprehensive results visualization

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                         RAILWAY PLATFORM                            │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│   ┌─────────────────┐         ┌─────────────────┐                  │
│   │   TLS/SSL       │         │   Custom        │                  │
│   │   Termination   │◄───────►│   Domain        │                  │
│   └────────┬────────┘         └─────────────────┘                  │
│            │                                                        │
│            ▼                                                        │
│   ┌─────────────────────────────────────────────┐                  │
│   │              GOPHISH SERVER                  │                  │
│   │  ┌─────────────┐      ┌─────────────┐       │                  │
│   │  │   Admin     │      │   Phishing  │       │                  │
│   │  │   Panel     │      │   Listener  │       │                  │
│   │  │  (Port 3333)│      │  (Port 80)  │       │                  │
│   │  └─────────────┘      └─────────────┘       │                  │
│   └─────────────────────────────────────────────┘                  │
│            │                                                        │
│            ▼                                                        │
│   ┌─────────────────────────────────────────────┐                  │
│   │              DATABASE (SQLite)               │                  │
│   │  • Campaign Data    • User Groups           │                  │
│   │  • Email Templates  • Landing Pages         │                  │
│   │  • Results/Metrics  • Sending Profiles      │                  │
│   └─────────────────────────────────────────────┘                  │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────────┐
│                        TARGET USERS                                 │
│   ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐          │
│   │  User 1  │  │  User 2  │  │  User 3  │  │  User N  │          │
│   │  📧      │  │  📧      │  │  📧      │  │  📧      │          │
│   └──────────┘  └──────────┘  └──────────┘  └──────────┘          │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 🚀 Quick Start

### Prerequisites

- 📦 GitHub account
- ☁️ Railway account (sign up with GitHub)
- 📧 SMTP relay service (for sending emails)

### Option 1: One-Click Template Deployment

1️⃣ **Sign up for Railway** using your GitHub account

2️⃣ **Deploy with one click:**

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/gophish)

3️⃣ **Review settings** and click **Deploy**

4️⃣ **Access admin panel** at `xxx.up.railway.app`

5️⃣ **Find credentials** in deployment logs:
```
Please login with the username admin and the password 0f564e8fxd9171d25
```

### Option 2: Fork & Deploy

1️⃣ **Fork the Gophish repository:**
```bash
# Fork from GitHub UI or clone and push to your repo
git clone https://github.com/gophish/gophish.git
```

2️⃣ **Create new Railway project:**
- Click **+ New Project** → **Deploy from GitHub repo**
- Select your forked repository

3️⃣ **Configure domain:**
- Go to **Settings** → **Domains**
- Click **Generate domain**

4️⃣ **Set environment variables:**
```
PORT=3333
```

5️⃣ **Update `config.json`:**
```json
{
  "admin_server": {
    "listen_url": "0.0.0.0:3333",
    "use_tls": false
  },
  "phish_server": {
    "listen_url": "0.0.0.0:80",
    "use_tls": false
  },
  "trusted_origins": ["xxx.up.railway.app"]
}
```

---

## 🎓 Skills Demonstrated

### Technical Skills
- ☁️ **Cloud Deployment** — Railway platform configuration and management
- 🐳 **Containerization** — Docker deployment and configuration
- 🔧 **Server Administration** — Gophish server setup and maintenance
- 📧 **Email Infrastructure** — SMTP configuration and email delivery
- 🔒 **TLS/SSL Management** — Certificate configuration and security
- 🌐 **DNS & Domains** — Custom domain setup and management

### Security Knowledge
- 🎣 **Phishing Techniques** — Understanding of social engineering tactics
- 🛡️ **Security Awareness** — Employee training methodologies
- 📊 **Risk Assessment** — Measuring organizational security posture
- 🔍 **Threat Simulation** — Realistic attack scenario creation
- 📋 **Compliance** — Security awareness training requirements

### Professional Competencies
- 📈 **Project Management** — End-to-end campaign execution
- 📝 **Technical Documentation** — Clear setup and usage guides
- 🎯 **Strategic Planning** — Campaign design and targeting
- 📊 **Data Analysis** — Interpreting simulation results
- 🗣️ **Communication** — Reporting findings to stakeholders

---

## 🏆 Project Achievements

### What This Project Demonstrates
- ✅ Complete phishing simulation platform deployment
- ✅ Cloud-based infrastructure setup on Railway
- ✅ Email campaign creation and management
- ✅ Real-time tracking and analytics implementation
- ✅ Security awareness testing methodology

### Business Value
- 💰 **Cost Savings** — Open-source alternative to expensive commercial tools
- 📉 **Risk Reduction** — Identify vulnerable employees before real attacks
- 📈 **Measurable Results** — Track improvement in security awareness
- 🎓 **Training Enhancement** — Data-driven security training programs
- ✅ **Compliance Support** — Meet security awareness training requirements

---

## 📊 Key Metrics & Performance

### Campaign Capabilities

| Metric | Value |
|--------|-------|
| **Email Delivery** | Real-time sending |
| **Tracking** | Opens, clicks, submissions |
| **Templates** | Unlimited custom templates |
| **Groups** | Unlimited user groups |
| **Campaigns** | Concurrent campaign support |
| **Reporting** | Real-time dashboard |

### Simulation Results Tracking

| Event Type | What It Measures |
|------------|------------------|
| 📧 **Email Sent** | Successful delivery |
| 👁️ **Email Opened** | User engagement |
| 🖱️ **Link Clicked** | Phishing susceptibility |
| 📝 **Data Submitted** | Credential capture |
| 🚨 **Reported** | Security awareness |

---

## 🙏 Acknowledgments

**Open-Source Projects:**
- [Gophish](https://getgophish.com/) — Open-source phishing framework
- [Go Programming Language](https://golang.org/) — Backend runtime
- [SQLite](https://sqlite.org/) — Embedded database

**Cloud Platforms:**
- [Railway](https://railway.app/) — Modern app hosting platform
- [Docker](https://docker.com/) — Containerization platform

**Security Community:**
- Security awareness training best practices
- Phishing simulation methodologies
- Social engineering research

---

## 🎬 Project Summary

This Phishing Attack Simulation project represents a **complete, production-ready security awareness testing platform** that combines:

✅ **Open-source technology** (Gophish framework)
✅ **Cloud deployment** (Railway platform)
✅ **Real-time analytics** (Campaign tracking dashboard)
✅ **Professional templates** (Email and landing pages)
✅ **Scalable infrastructure** (Docker containerization)

**Demonstrates:**
- Cloud deployment expertise
- Security awareness methodology
- Email infrastructure knowledge
- Campaign management skills
- Data analysis capabilities

**Delivers:**
- Cost-effective phishing simulations
- Measurable security metrics
- Employee training insights
- Compliance documentation
- Risk assessment data

**Perfect For:**
- Security Analyst roles
- IT Administrator positions
- Penetration Testing opportunities
- Security Awareness programs
- Portfolio demonstration

---

## 📞 Contact & Support

- **Project Repository**: https://github.com/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish
- **Issues**: https://github.com/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish/issues
- **Discussions**: https://github.com/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish/discussions

---

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish?style=social)
![GitHub forks](https://img.shields.io/github/forks/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish?style=social)
![GitHub issues](https://img.shields.io/github/issues/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish)
![GitHub pull requests](https://img.shields.io/github/issues-pr/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish)

---

<div align="center">

**Built with ❤️ for Security Awareness**

**Empowering Organizations to Test Their Human Firewall**

**Open-Source Tools • Enterprise Results • Production-Ready**

[⬆ Back to Top](#-phishing-attack-simulation-with-gophish)

</div>
