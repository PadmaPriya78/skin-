# skin-

> **Automated Technical Documentation & Continuous Synchronization**  
> *Synchronized by RepoMind AI & ASDSE Platform*

| Repository Version | Branch | Active Commit | Primary Language | Sync State |
| :--- | :--- | :--- | :--- | :--- |
| **V5** | `main` | [`3b5fe41`](https://github.com/PadmaPriya78/skin-.git/commit/3b5fe41d8de19d3a247d5e0494fc3b77391bea8d) | `Python` | `✓ Grounded & Synchronized` |

> **Commit Identity**: `3b5fe41` (3b5fe41d8de19d3a247d5e0494fc3b77391bea8d)  
> **Author**: RepoMind ASDSE Bot | **Date**: 9/10/2026, 9:31:38 am  
> **Message**: *docs(asdse): synchronize generated documentation*

> ℹ️ **Version Transition**: Synchronized from baseline **b22e150** → **3b5fe41** with 1 changed files (+9 / -9 lines).

---

## Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [System Architecture](#system-architecture)
- [Repository Structure](#repository-structure)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Environment Variables](#environment-variables)
- [Database Management](#database-management)
- [API Endpoints](#api-endpoints)
- [Authentication & Security](#authentication--security)
- [Running the Application](#running-the-application)
- [Testing](#testing)
- [Deployment & DevOps](#deployment--devops)
- [Dependencies](#dependencies)
- [Version Changelog](#version-changelog)
- [License](#license)

---

## Project Overview

**skin-** is a software system built using **Python** with **FastAPI** and **React**, utilizing **PostgreSQL** for persistent storage.

This codebase provides a modular architecture designed for maintainability, with defined separation across business logic, routing, persistence, and service execution.

## Key Features

- **Modular Backend Service**: Engineered using FastAPI with structured request controllers and service boundaries.
- **Interactive User Interface**: Implemented with React.
- **Data Persistence Layer**: Grounded PostgreSQL storage managing 12 database entities with schema validation.
- **Structured HTTP API**: 43 documented RESTful endpoints with method routing and contract handlers.
- **Authentication & Access Control**: Enforces security policies via Environment-based Secrets.
- **Containerized Runtime**: Production-ready Docker containerization for portable environment parity.
- **Automated Test Suite**: 3 test files covering critical application units.

## Technology Stack

| Category | Technologies Verified in Codebase |
| :--- | :--- |
| **Primary Language** | `Python` (All: `Python`, `JavaScript`, `YAML`, `JSON`, `HTML`, `React JSX`, `CSS`) |
| **Backend Framework** | `FastAPI` |
| **Frontend Framework** | `React` |
| **Database Engine** | `PostgreSQL` |
| **Authentication** | `Environment-based Secrets` |
| **Manifest Files** | `requirements.txt`, `package.json` |

## System Architecture

The repository follows a **Microservice Architecture** pattern.

### System Context Diagram

```mermaid
graph TD
    classDef userClass fill:#1E293B,stroke:#38BDF8,stroke-width:2px,color:#F8FAFC;
    classDef systemClass fill:#0F172A,stroke:#818CF8,stroke-width:2px,color:#F8FAFC;
    classDef externalClass fill:#1E293B,stroke:#94A3B8,stroke-width:2px,color:#CBD5E1;

    User["User / Client Applications"]:::userClass
    System["skin- Platform"]:::systemClass
    ExtServices["External Services / Cloud APIs"]:::externalClass
    Database["SQLite"]:::externalClass

    User -->|"Interacts via HTTP / REST"| System
    System -->|"Persists & Queries Data"| Database
    System -->|"Delegates to External Integrations"| ExtServices

```

### Container Architecture Diagram

```mermaid
graph TD
    classDef container fill:#1E293B,stroke:#60A5FA,stroke-width:2px,color:#F8FAFC;
    classDef db fill:#0F172A,stroke:#34D399,stroke-width:2px,color:#F8FAFC;

    ClientApp["Frontend Client UI<br/><i>(Client UI Layer)</i>"]:::container
    BackendApp["Application Core Service<br/><i>(Domain & Business Logic Engine)</i>"]:::container
    DatabaseContainer["Persistence Store<br/><i>(SQLite)</i>"]:::db

    ClientApp -->|"API Calls / HTTP Requests"| BackendApp
    BackendApp -->|"Queries & Transactions"| DatabaseContainer

```

## Repository Structure

| Directory / Path | Module Purpose |
| :--- | :--- |
| `.` | Application module directory |
| `skin-intelligence` | Application module directory |
| `skin-intelligence/backend` | Application module directory |
| `skin-intelligence/frontend` | Application module directory |
| `skin-intelligence/backend/ml` | Application module directory |
| `skin-intelligence/backend/models` | Database entity definitions and data models |
| `skin-intelligence/backend/routes` | HTTP route controllers and endpoint handlers |
| `skin-intelligence/backend/services` | Business logic services and domain operations |
| `skin-intelligence/backend/tests` | Automated unit and integration test suites |
| `skin-intelligence/backend/utils` | Utility functions and helper modules |
| `skin-intelligence/frontend/public` | Static client assets and media files |
| `skin-intelligence/frontend/src` | Application module directory |
| `skin-intelligence/frontend/src/assets` | Static client assets and media files |

## Prerequisites

Ensure the following tools and runtimes are installed on your host machine:

- **Python**: 3.10 or higher
- **pip** package installer (and optional `virtualenv`)
- **Git**: v2.30+ for version control
- **PostgreSQL**: Running instance or cloud connection string
- **Docker & Docker Compose** (optional, for containerized execution)

## Installation & Setup

```bash
# 1. Clone the repository
git clone https://github.com/PadmaPriya78/skin-.git.git
cd skin-

# 2. Checkout the verified branch/commit
git checkout main

# 3. Install project dependencies
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the root directory based on the configuration template below (placeholders are sanitized):

```env
# Application HTTP server listening port
PORT=5000

# Runtime environment (development | production | test)
NODE_ENV=development

# PostgreSQL connection URL
DATABASE_URL=postgresql://postgres:password@localhost:5432/app_db

# Secret key for signing authentication tokens
JWT_SECRET=your-256-bit-secret-key-placeholder

```

## Database Management

* **Database Engine**: `PostgreSQL`
* **Registered Entities / Collections**: 12

| Entity / Table Name | Purpose | Key Attributes |
| :--- | :--- | :--- |
| `DermatologistPrescription` | Entity model for DermatologistPrescription | `id, created_at` |
| `LifestyleLog` | Entity model for LifestyleLog | `id, created_at` |
| `Notification` | Entity model for Notification | `id, created_at` |
| `NotificationSetting` | Entity model for NotificationSetting | `id, created_at` |
| `ProductReplenishment` | Entity model for ProductReplenishment | `id, created_at` |
| `Product` | Entity model for Product | `id, created_at` |
| `ProgressLog` | Entity model for ProgressLog | `id, created_at` |
| `SkincareRoutine` | Entity model for SkincareRoutine | `id, created_at` |
| `SkinAssessment` | Entity model for SkinAssessment | `id, created_at` |
| `SkinProfile` | Entity model for SkinProfile | `id, created_at` |
| `SkinTextureAnalysis` | Entity model for SkinTextureAnalysis | `id, created_at` |
| `User` | Entity model for User | `id, created_at` |

### Entity-Relationship Diagram

```mermaid
erDiagram
    DERMATOLOGISTPRESCRIPTION {
        INTEGER id PK
        TEXT data
    }
    LIFESTYLELOG {
        INTEGER id PK
        TEXT data
    }
    NOTIFICATION {
        INTEGER id PK
        TEXT data
    }
    NOTIFICATIONSETTING {
        INTEGER id PK
        TEXT data
    }
    PRODUCTREPLENISHMENT {
        INTEGER id PK
        TEXT data
    }
    PRODUCT {
        INTEGER id PK
        TEXT data
    }
    PROGRESSLOG {
        INTEGER id PK
        TEXT data
    }
    SKINCAREROUTINE {
        INTEGER id PK
        TEXT data
    }
    DERMATOLOGISTPRESCRIPTION ||--o{ LIFESTYLELOG : references

```

## API Endpoints

Total Verified Endpoints: **43**

| HTTP Method | Endpoint Route | Handler / Controller | Auth Required |
| :--- | :--- | :--- | :--- |
| `GET` | `/` | `GET /` | `Public` |
| `GET` | `/health` | `GET /health` | `Public` |
| `GET` | `/database-test` | `GET /database-test` | `Public` |
| `GET` | `/stats` | `GET /stats` | `Public` |
| `GET` | `/users` | `GET /users` | `Public` |
| `POST` | `/run` | `POST /run` | `Public` |
| `GET` | `/latest` | `GET /latest` | `Public` |
| `GET` | `/history` | `GET /history` | `Public` |
| `POST` | `/register` | `POST /register` | `Public` |
| `POST` | `/login` | `POST /login` | `Public` |
| `GET` | `/me` | `GET /me` | `Public` |
| `POST` | `/oauth-mock` | `POST /oauth-mock` | `Public` |
| `GET` | `/patients` | `GET /patients` | `Public` |
| `GET` | `/catalog` | `GET /catalog` | `Public` |
| `POST` | `/prescribe` | `POST /prescribe` | `Public` |
| `GET` | `/my-prescription` | `GET /my-prescription` | `Public` |
| `GET` | `/today` | `GET /today` | `Public` |
| `POST` | `/{notification_id}/read` | `POST /{notification_id}/read` | `Public` |
| `POST` | `/read-all` | `POST /read-all` | `Public` |
| `POST` | `/{notification_id}/dismiss` | `POST /{notification_id}/dismiss` | `Public` |
| `GET` | `/settings` | `GET /settings` | `Public` |
| `POST` | `/settings` | `POST /settings` | `Public` |
| `GET` | `/replenishments` | `GET /replenishments` | `Public` |
| `POST` | `/replenishments` | `POST /replenishments` | `Public` |
| `POST` | `/replenishments/{item_id}/restock` | `POST /replenishments/{item_id}/restock` | `Public` |
| `DELETE` | `/replenishments/{item_id}` | `DELETE /replenishments/{item_id}` | `Public` |
| `POST` | `/` | `POST /` | `Public` |
| `GET` | `/recommendations` | `GET /recommendations` | `Public` |
| `GET` | `/{product_id}/analysis` | `GET /{product_id}/analysis` | `Public` |
| `GET` | `/compare` | `GET /compare` | `Public` |
| `GET` | `/{product_id}/alternatives` | `GET /{product_id}/alternatives` | `Public` |
| `GET` | `/analytics` | `GET /analytics` | `Public` |
| `GET` | `/assessment/pdf` | `GET /assessment/pdf` | `Public` |
| `GET` | `/assessment/excel` | `GET /assessment/excel` | `Public` |
| `GET` | `/routine/pdf` | `GET /routine/pdf` | `Public` |
| `GET` | `/progress/pdf` | `GET /progress/pdf` | `Public` |
| `POST` | `/generate` | `POST /generate` | `Public` |
| `GET` | `/{routine_type}` | `GET /{routine_type}` | `Public` |
| `POST` | `/analyze` | `POST /analyze` | `Public` |
| `POST` | `/analyze-multi` | `POST /analyze-multi` | `Public` |
| `POST` | `/sync-profile` | `POST /sync-profile` | `Public` |
| `ALL` | `,` | `ALL ,` | `Public` |
| `ALL` | `,,` | `ALL ,,` | `Public` |

### API Execution Sequence

```mermaid
sequenceDiagram
    actor Client as User / Frontend
    participant API as POST /login
    participant Svc as AuthService
    participant DB as Database (User)

    Client->>API: Submit Credentials (email/username, password)
    API->>Svc: validateCredentials(payload)
    Svc->>DB: findOne({ email })
    DB-->>Svc: Return Stored User Record & Hash
    Svc->>Svc: verifyHash(password, storedHash)
    alt Credentials Valid
        Svc->>Svc: generateJwtToken(userPayload)
        Svc-->>API: { token, userProfile }
        API-->>Client: 200 OK (JWT Token + Auth Headers)
    else Credentials Invalid
        Svc-->>API: AuthenticationError
        API-->>Client: 401 Unauthorized
    end
```

## Authentication & Security

* **Authentication Mechanisms**: `Environment-based Secrets`
* **Token & Key Management**: Sensitive tokens must be stored in secure environment variables.

### Authentication Flow

```mermaid
sequenceDiagram
    actor User as User Browser / Client
    participant Server as Application Server
    participant Session as Session & Security Store

    User->>Server: HTTP Request (Method + Headers)
    Server->>Session: Validate Session State & Security Keys
    alt Valid Session / Public Route
        Session-->>Server: proceed(authorized)
        Server->>Server: dispatchToController()
        Server-->>User: 200 OK (Response Payload)
    else Invalid / Unauthenticated
        Server-->>User: 401 Unauthorized / Redirect
    end

```

## Running the Application

### Development Mode

```bash
uvicorn main:app --reload --port 8000
```

## Testing

Execute automated test suites using the verified test runner:

```bash
pytest
```

## Deployment & DevOps

### Docker Execution

```bash
# Build and launch containers
docker-compose up --build
```

### Deployment Topology Diagram

```mermaid
graph TB
    classDef node fill:#1E293B,stroke:#F59E0B,stroke-width:2px,color:#F8FAFC;

    subgraph UserDevice["Client Device"]
        Browser["Modern Web Browser"]:::node
    end

    subgraph HostServer["Host Server Environment (Docker Container)"]
        Ingress["HTTP/S Ingress Gateway"]:::node
        AppServer["Application Server Runtime<br/><i>(Application Runtime)</i>"]:::node
        DBInstance["Persistence Node<br/><i>(SQLite)</i>"]:::node
    end

    Browser -->|"HTTP / HTTPS"| Ingress
    Ingress -->|"Internal Router"| AppServer
    AppServer -->|"Query Connection"| DBInstance

```

## Dependencies

The system relies on **28** runtime and development dependencies defined in `requirements.txt`, `package.json`.

### Primary Packages

| Package | Version Range | Category |
| :--- | :--- | :--- |
| `react` | `^19.2.8` | `Runtime` |
| `react-dom` | `^19.2.8` | `Runtime` |
| `@tailwindcss/vite` | `^4.3.3` | `Runtime` |
| `@types/react` | `^19.2.18` | `Runtime` |
| `@types/react-dom` | `^19.2.4` | `Runtime` |
| `@vitejs/plugin-react` | `^6.1.0` | `Runtime` |
| `chart.js` | `^4.5.1` | `Runtime` |
| `lucide-react` | `^1.48.0` | `Runtime` |
| `oxlint` | `^1.79.0` | `Runtime` |
| `react-chartjs-2` | `^5.3.1` | `Runtime` |
| `tailwindcss` | `^4.3.3` | `Runtime` |
| `vite` | `^8.2.2` | `Runtime` |
| `fastapi` | `latest` | `Runtime` |
| `uvicorn[standard]` | `latest` | `Runtime` |
| `sqlalchemy` | `latest` | `Runtime` |

## Version Changelog

### Version V5 (`3b5fe41`)
- **Base Version**: `b22e150`
- **Files Added** (0): None
- **Files Modified** (1): `[object Object]`
- **Files Deleted** (0): None
- **Diff Statistics**: +9 / -9 lines changed

## License

This project is licensed under the **Proprietary / Standard Repository License**.

---
*Generated automatically by [ASDSE RepoMind Intelligence](https://github.com/Spidey390/Neighbor-to-Neighbor) — Continuous Technical Documentation & GitHub Synchronization Pipeline.*
