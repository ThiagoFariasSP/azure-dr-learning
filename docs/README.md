# Docs

This folder will contain documentation files for the project.
# Azure Disaster Recovery Architecture – Learning Project

This repository demonstrates the step-by-step evolution of a cloud architecture designed for resiliency and disaster recovery on Microsoft Azure.

The project focuses on architectural design concepts rather than implementation details, following enterprise best practices.

---

## Architecture Evolution

### 1. Baseline Architecture
A simple application architecture used as a starting point.

- User
- Application
- Database

File:
- `architecture/basic-architecture.png`

---

### 2. Azure Baseline Architecture
The baseline architecture adapted to Microsoft Azure using PaaS services.

- Internet and DNS
- Azure App Service
- Azure SQL Database
- Single Azure Region

File:
- `architecture/azure-basic-architecture.png`

---

### 3. Resilient Architecture (High Availability)
The Azure architecture evolved to support high availability within a single region.

- Multiple App Service instances
- High Availability database
- No single point of failure

File:
- `architecture/azure-resilient-architecture.png`

---

### 4. Disaster Recovery Architecture (Multi-Region)
A full Disaster Recovery design protecting the application against regional outages.

- Active / Passive regional model
- Azure Traffic Manager for traffic redirection
- Cross-region data replication
- Defined failover strategy

File:
- `architecture/azure-dr-architecture.png`

---

## Disaster Recovery Strategy
The Disaster Recovery approach, including RTO, RPO, failover model, and design considerations, is documented here:

- `docs/disaster-recovery.md`

---

## Key Concepts Covered
- Cloud architecture evolution
- High availability vs Disaster Recovery
- Azure regional resiliency
- Active / Passive DR design
- RTO and RPO definition

---

## Disclaimer
This project is intended for learning and architectural demonstration purposes.
