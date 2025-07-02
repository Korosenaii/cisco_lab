# Cisco DSE – Network Configuration Automation Lab

This lab simulates a virtual network environment to experiment with configuration management automation using gNMI/gNOI protocols. It is inspired by a Cisco-style Distributed Systems Engineering (DSE) project.

## 📌 Objectives

- Automate the retrieval, validation, and deployment of network configurations
- Simulate routers using **FRRouting (FRR)** inside Docker containers
- Use **gNMI** for state/config retrieval and **gNOI** for secure configuration application
- Integrate automated testing with **PyTest**
- Set up a CI/CD pipeline using **Jenkins**

---

## 🖼️ Architecture Overview

(NOT DONE YET)

## 🛠️ Tech Stack

- ⚙️ **Go** (gRPC, gNMI/gNOI clients)
- 🐍 **Python** (PyTest for validation)
- 🐳 **Docker & Docker Compose**
- 🔐 **TLS Certificates**
- 🧪 **Jenkins** (CI/CD pipeline)
- 🖧 **FRRouting** (router simulation)

---

## 🚀 Installation

### 1. Dependencies

```bash
sudo apt install -y docker.io docker-compose golang-go python3-pip
