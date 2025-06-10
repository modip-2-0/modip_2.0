# MODIP - Molecular Docking Integrated Platform

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker)

MODIP is an integrated platform for parallel virtual screening of bioactive compounds through molecular docking. This repository serves as a **metarepo** containing all components of the MODIP system organized as Git submodules.

## System Overview

MODIP is a webserver application designed for computer-aided drug discovery that:
- Downloads and prepares compounds from PubChem BioAssay database
- Performs virtual screening using AutoDock Vina
- Enables parallel screening of chemotherapeutic receptors and off-target proteins
- Supports local execution and adapts to other docking software/chemical databases

Key capabilities:
1. Automated compound processing for docking compatibility
2. Distributed screening across multiple protein targets
3. Extensible architecture for alternative tools/databases
4. Containerized execution environment

## Repository Setup

### Requirements
- [Git](https://git-scm.com/downloads/linux)
- [Docker](https://docs.docker.com/engine/install/)
- [Docker Compose](https://docs.docker.com/compose/install/linux/)

### 1. Cloning with Submodules
```bash
# Clone main repository (recursive to include submodules)
git clone --recursive https://github.com/modip-2-0/modip_metarepo.git

cd modip-metarepo

# If you cloned non-recursively, initialize submodules:
git submodule update --init --recursive
```

### 2. Running with Docker

```bash
# Start all services
docker compose up -d

# View running containers
docker compose ps

# Stop services
docker compose down
```

### 3. Access MODIP through your web browser 

After starting the containers, open http://localhost:8501 . The dashboard will load with the authentication interface.

















