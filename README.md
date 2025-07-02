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

<pre><code>
📁 Project Structure

.
├── ca/                         # Certificate Authority (CA)
│   ├── ca.crt                  # Root certificate
│   ├── ca.key                  # Private key
│   └── ca.srl                  # Serial number file
├── certs/                      # Signed certificates per router
│   ├── router1/
│   │   ├── router1.crt
│   │   ├── router1.csr
│   │   └── router1.key
│   └── router2/
│       ├── router2.crt
│       ├── router2.csr
│       └── router2.key
├── client-go/                  # Go client for gNMI/gNOI
├── docker-compose.yml          # Docker orchestration file
├── frr1/                       # FRRouting container config (router 1)
│   └── config/
│       ├── daemons
│       └── frr.conf
├── frr2/                       # FRRouting container config (router 2)
│   └── config/
│       ├── daemons
│       └── frr.conf
├── gnmi1/                      # gNMI server configuration
│   ├── certs/
│   │   ├── ca.crt
│   │   ├── router1.crt
│   │   └── router1.key
│   ├── config/
│   │   └── gnmic-config.yml
│   └── gnmi-config.yml
├── kubernetes/                 # (Optional) Kubernetes manifests
├── README.md                   # Project documentation
└── tests/                      # PyTest validation scripts
</code></pre>


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
