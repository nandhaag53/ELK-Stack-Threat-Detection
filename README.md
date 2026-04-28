# 🔐 ELK Stack — Centralized Log Monitoring & Threat Detection

![Cyber Security](https://img.shields.io/badge/Cyber%20Security-ELK%20Stack-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Docker-orange)

## 📌 Project Overview

This is my **Major Project** for B.A. Criminology & Police Administration at Kamaraj College, Thoothukudi. It implements a **Centralized Log Monitoring and Threat Detection System** using the ELK Stack deployed on a REMnux Linux VM using Docker Compose.

---

## 🛠️ Technologies Used

| Tool | Version | Purpose |
|------|---------|---------|
| Elasticsearch | 9.3.2 | Log storage & search engine |
| Kibana | 8.x | Dashboard & visualization |
| Filebeat | 8.19.13 | Log shipping & collection |
| Docker Compose | Latest | Container orchestration |
| REMnux Linux | Latest | Security-focused Linux VM |
| VirtualBox | Latest | Virtual machine host |

---

## 🎯 Key Features

- ✅ **Centralized Log Collection** using Filebeat system module
- ✅ **Real-time Log Indexing** with Elasticsearch
- ✅ **SOC Security Monitoring Dashboard** built in Kibana
- ✅ **SSH Brute Force Alert Rule** using KQL (Kibana Query Language)
- ✅ **Brute Force Attack Simulation** for testing detection
- ✅ **Docker Compose** deployment for easy setup

---

## 📊 Architecture

```
[Linux VM - REMnux]
       |
   [Filebeat] ──── collects system logs
       |
[Elasticsearch] ── stores & indexes logs
       |
   [Kibana] ─────── SOC Dashboard + Alerts
```

---

## 🚨 SSH Brute Force Detection

- **Alert Rule:** Detects multiple failed SSH login attempts
- **Query (KQL):** `system.auth.ssh.event: "Failed" AND system.auth.ssh.method: "password"`
- **Threshold:** 5+ failed attempts trigger alert
- **Simulation:** Brute force attack tested locally using repeated SSH login attempts

---

## 📁 Project Structure

```
elk-stack-threat-detection/
├── docker-compose.yml        # ELK Stack container setup
├── filebeat.yml              # Filebeat configuration
├── README.md                 # Project documentation
└── screenshots/              # Dashboard & alert screenshots
```

---

## ⚙️ How to Run

```bash
# 1. Clone this repository
git clone https://github.com/nandakumarr2002/elk-stack-threat-detection

# 2. Start ELK Stack with Docker Compose
docker-compose up -d

# 3. Open Kibana Dashboard
# Go to: http://localhost:5601

# 4. Start Filebeat
sudo systemctl start filebeat
```

---

## 📸 Screenshots

> Dashboard and alert screenshots will be added here.

---

## 👨‍💻 Author

**Nandakumar R**
- 🎓 B.A. Criminology & Police Administration — Kamaraj College, Thoothukudi
- 🔐 Unlox Edge Certified — Cyber Security
- 🔍 Field Investigator — Spartan Detective Agency
- 📍 Thoothukudi, Tamil Nadu, India
- 💼 [LinkedIn](https://linkedin.com/in/nandakumar-r)

---

## 📄 License

This project is for educational purposes — Major Project submission 2023.
