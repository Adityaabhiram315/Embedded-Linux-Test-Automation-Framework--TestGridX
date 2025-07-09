# 🚀  Embedded Linux Test Automation Framework - TestGridX 

**TestGridX** is a lightweight test automation framework using [Pytest](https://pytest.org/) and [Labgrid](https://labgrid.readthedocs.io) to validate embedded Linux firmware (OpenWrt) inside a virtual environment powered by **QEMU**.

It simulates realistic boot, SSH, and VPN tunnel scenarios in CI-ready environments, helping reduce manual QA effort by over 50% and identifying boot issues 2× faster in CI.

---

## ✅ Features

- Emulates OpenWrt boot in QEMU
- SSH access & command execution validation
- Docker-based OpenVPN server setup
- PKI (certs) generation for secure tunneling
- Bi-directional VPN connectivity verification
- Simple YAML configs for test plans

---

## 🧪 Test Flow

1. Boot OpenWrt firmware in QEMU  
2. Enable and test SSH access  
3. Generate CA, server/client certs  
4. Launch VPN server in Docker  
5. Install & configure VPN client on OpenWrt  
6. Ping test across the tunnel (both directions)

---

## 🧱 Architecture

![arc](https://github.com/user-attachments/assets/776784f5-a71a-43bc-b67e-b1a86f69ddd3)

- `make test-docker` triggers a Docker Compose setup  
- QEMU boots the firmware  
- Labgrid + Pytest run automated test steps  
- PKI and OpenVPN are configured during the test  

---

## ⚙️ Requirements

- Linux host system  
- [Docker Engine](https://docs.docker.com/engine/install/debian/)  
- Docker Compose  
- GNU Make  

---

## 🚀 Quick Start
![ezgif-2115b2873a80c7](https://github.com/user-attachments/assets/1551335f-5034-4ef0-8394-1947feb88f10)
```bash
git clone https://github.com/honeytreelabs/labgrid-qemu-sample.git
cd labgrid-qemu-sample
make test-docker







