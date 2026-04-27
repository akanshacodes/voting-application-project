<div align="center">

# 🚀 Distributed Voting Application

<img src="https://media.giphy.com/media/3o7TKsQ8f0zQ0Q0Q0Q/giphy.gif" width="160"/>

![Docker](https://img.shields.io/badge/Docker-Multi--Container-blue?logo=docker)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Orchestration-326CE5?logo=kubernetes)
![Microservices](https://img.shields.io/badge/Architecture-Microservices-green)
![Status](https://img.shields.io/badge/Status-Demo-orange)

</div>

---

# 🌟 Overview

A simple distributed voting application running across multiple Docker containers.

This project demonstrates a **microservices-based distributed system** where different services communicate with each other to process and display votes in real time.

---

# 🏗️ Architecture

<div align="center">

<img src="https://github.com/user-attachments/assets/1394fac3-c3ca-4874-b64a-a5d5f84c25c6" width="860"/>

</div>

## 🧩 Components

- 🖥️ Front-end web app in Python which lets you vote between two options  
- 🔴 Redis which collects new votes  
- ⚙️ .NET worker which consumes votes and stores them  
- 🗄️ Postgres database backed by a Docker volume  
- 📊 Node.js web app which shows results in real time  
---

## 🔄 Data Flow

```text
User → Python Web App → Redis Queue → .NET Worker → PostgreSQL → Node.js Results App
