## Medpoint Backend

**Medpoint Backend** is the core API service of the Medpoint platform, built with **Golang** using the **Raiden Framework**. This backend handles authentication, medical reservations, scheduling, and integrates with **Supabase** as the backend-as-a-service (BaaS).

---

## Tech Stack

- Golang
- Raiden Framework
- Supabase (PostgreSQL, Auth, RESTful API)

---

## Project Structure

```bash
├── build
│   ├── backend_medpoint
│   ├── import
│   └── state      # Bytecode containing raiden state
├── cmd
│   └── backend_medpoint
│       └── backend_medpoint.go    # Main project
│   ├── apply/main.go
│   └── import/main.go
├── configs
│   ├── app.yaml          # App configuration file
│   └── modules/          # Module configuration file
│       ├── module_a.yaml
│       ├── module_b.yaml
│       └── ...
├── internal
│   ├── bootstrap
│   │   ├── route.go
│   │   ├── rpc.go
│   │   ├── roles.go
│   │   ├── models.go
│   │   └── storages.go
│   ├── controllers
│   │   └── hello.go    # Example controller
│   ├── roles           # ACL/RLS definition
│   │   ├── members.go
│   │   └── ...
│   ├── models          # All model will auto-sync
│   │   ├── users.go
│   │   └── ...
│   ├── rpc             # RPC
│   │   └── get_user.go
│   ├── topics          # Real-time
│   │   ├── notification.go
│   │   └── inbox.go
│   │
│   └── storages
│       └── avatar.go
├── go.sum
├── go.mod
└── README.md
```

---

## Quick Start

### Installation

```bash
sh -c "$(curl -fsSL https://raiden.sev-2.com/install.sh)"   # Install Raiden CLI

raiden version                                              # Verify installation
```

### Run this Project

```bash
git clone https://github.com/azkizaini/Backend_Medpoint.git  # HTTPS
```
or
```bash
git clone git@github.com:azkizaini/Backend_medpoint.git      # SSH
```

then
```bash
cd Backend_Medpoint

go mod tidy
raiden run
```

---
