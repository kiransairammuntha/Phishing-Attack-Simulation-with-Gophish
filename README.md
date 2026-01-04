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
- [💡 Configuration](#-configuration)
- [📁 Project Structure](#-project-structure)
- [🗺️ Roadmap](#️-roadmap)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [📬 Contact](#-contact)

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

## 💡 Configuration

### Setting Up a Phishing Campaign

```python
# Campaign Configuration Checklist

# 1. Users & Groups
users_config = {
    "group_name": "IT Department",
    "members": [
        {"email": "user1@company.com", "first_name": "John", "last_name": "Doe"},
        {"email": "user2@company.com", "first_name": "Jane", "last_name": "Smith"},
    ]
}

# 2. Email Template
email_template = {
    "name": "Password Reset Request",
    "subject": "Urgent: Password Reset Required",
    "html": "<html>...</html>",  # Full HTML editor available
    "attachments": []  # Optional attachments
}

# 3. Sending Profile (SMTP Configuration)
sending_profile = {
    "name": "Company SMTP",
    "host": "smtp.company.com:587",
    "from_address": "security@company.com",
    "username": "smtp_user",
    "password": "smtp_password"
}

# 4. Landing Page
landing_page = {
    "name": "Fake Login Portal",
    "html": "<html>...</html>",
    "capture_credentials": True,
    "redirect_url": "https://company.com/security-training"
}
```

### Campaign Launch Settings

| Setting | Description | Example |
|---------|-------------|---------|
| **Name** | Campaign identifier | Q1 Security Test |
| **Email Template** | Phishing email to send | Password Reset |
| **Landing Page** | Page shown on link click | Fake Portal |
| **URL** | Gophish listener domain | https://xxx.up.railway.app |
| **Launch Date** | Scheduled send time | 2024-01-15 09:00 |
| **Send Emails By** | Completion deadline | 2024-01-15 17:00 |
| **Groups** | Target user groups | IT Department |

---

## 📁 Project Structure

```
gophish-phishing-simulation/
├── 📂 config/
│   └── config.json              # Gophish configuration
├── 📂 templates/
│   ├── 📂 emails/               # Email templates
│   │   ├── password_reset.html
│   │   ├── invoice_notice.html
│   │   └── security_alert.html
│   └── 📂 landing_pages/        # Landing page templates
│       ├── login_portal.html
│       └── document_viewer.html
├── 📂 assets/
│   ├── banner.png               # Project banner
│   └── screenshots/             # Documentation images
├── 📂 docs/
│   ├── SETUP.md                 # Detailed setup guide
│   ├── CAMPAIGN_GUIDE.md        # Campaign creation guide
│   └── BEST_PRACTICES.md        # Security awareness tips
├── 📄 docker-compose.yml        # Docker deployment config
├── 📄 Dockerfile                # Container definition
├── 📄 railway.json              # Railway deployment config
├── 📄 README.md                 # Project documentation
└── 📄 LICENSE                   # MIT License
```

---

## 🗺️ Roadmap

- [x] Deploy Gophish on Railway
- [x] Configure TLS/SSL termination
- [x] Set up custom domain support
- [x] Create email templates
- [x] Configure landing pages
- [x] Launch test campaigns
- [ ] Integrate with Slack for notifications
- [ ] Add automated reporting dashboard
- [ ] Create template library for common scenarios
- [ ] Implement campaign scheduling automation
- [ ] Add multi-language template support
- [ ] Build integration with security awareness training platforms

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. 🍴 **Fork** the repository
2. 🌿 **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. 💾 **Commit** your changes (`git commit -m 'Add AmazingFeature'`)
4. 📤 **Push** to branch (`git push origin feature/AmazingFeature`)
5. 🔃 **Open** a Pull Request

### Contribution Ideas
- 📧 New phishing email templates
- 🌐 Landing page designs
- 📚 Documentation improvements
- 🔧 Deployment configurations for other platforms

---

📞 Contact & Support

Project Repository: https://github.com/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish
Issues: https://github.com/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish/issues
Discussions: https://github.com/kiransairammuntha/Phishing-Attack-Simulation-with-Gophish/discussions

---

<div align="center">
Built with ❤️ for Security Awareness
Empowering Organizations to Test Their Human Firewall
Open-Source Tools • Enterprise Results • Production-Ready
⬆ Back to Top
</div>
