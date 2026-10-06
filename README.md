# Video Classroom

A real-time video classroom platform designed to provide a simple and scalable environment for online classes.

The project is being developed as a full-stack cloud-oriented application, with a focus on backend development, real-time communication, containerization, and AWS infrastructure.

## Project Status

🚧 **In development — Week 1**

Current focus:

* Project architecture
* React frontend
* FastAPI backend
* PostgreSQL database
* Docker-based local environment
* Frontend ↔ Backend ↔ Database integration

Real-time video communication will be introduced in a later development phase.

---

## Objectives

The main goal of this project is to build a functional online classroom platform while applying production-oriented development practices.

The project will progressively incorporate:

* Full-stack development
* REST APIs
* Relational database design
* Containerization
* Real-time communication
* WebRTC
* Scalable video infrastructure
* AWS cloud services
* Infrastructure as Code
* Monitoring and CI/CD

---

## Planned Architecture

The project will evolve progressively throughout the development roadmap.

### Current architecture — Week 1

```text
┌─────────────────────────────────────────────┐
│                  Local                      │
│                                             │
│   ┌───────────┐       ┌──────────────┐     │
│   │   React   │──────▶│   FastAPI    │     │
│   │ Frontend  │ HTTP  │   Backend    │     │
│   └───────────┘       └──────┬───────┘     │
│                              │              │
│                             SQL             │
│                              │              │
│                       ┌──────▼───────┐      │
│                       │  PostgreSQL  │      │
│                       │   Database   │      │
│                       └──────────────┘      │
│                                             │
│                  Docker Compose             │
└─────────────────────────────────────────────┘
```

The application is currently designed to run locally using Docker Compose.

---

## Technology Stack

### Frontend

* React
* JavaScript / TypeScript
* HTML
* CSS

### Backend

* Python
* FastAPI
* REST API
* Pydantic

### Database

* PostgreSQL
* SQL

### Development & Infrastructure

* Docker
* Docker Compose
* Git
* GitHub

### Planned Technologies

The following technologies will be introduced in later phases:

* WebRTC
* WebSocket
* STUN / TURN
* LiveKit / SFU
* Redis
* AWS
* Amazon S3
* Amazon RDS
* Amazon Cognito
* Amazon ECS
* Amazon EKS
* Terraform
* CI/CD
* CloudFront
* Monitoring

---

## Development Roadmap

| Week | Objective              | Main Technologies                  |
| ---- | ---------------------- | ---------------------------------- |
| 1    | Project foundation     | React, FastAPI, PostgreSQL, Docker |
| 2    | Users and courses      | FastAPI, PostgreSQL, JWT/Cognito   |
| 3    | Basic video calling    | WebRTC, WebSocket, STUN            |
| 4    | Multi-user video       | LiveKit / SFU                      |
| 5    | Classroom features     | React, LiveKit, Redis              |
| 6    | AWS deployment         | S3, ECS, RDS, Cognito              |
| 7    | Kubernetes             | EKS, Docker, Terraform             |
| 8    | Production & portfolio | CI/CD, monitoring, CloudFront      |

---

## Week 1 Goals

The first development phase focuses exclusively on establishing the application foundation.

### Tasks

* [ ] Define project requirements
* [ ] Define initial architecture
* [ ] Initialize React application
* [ ] Initialize FastAPI application
* [ ] Design PostgreSQL schema
* [ ] Configure PostgreSQL
* [ ] Create Dockerfiles
* [ ] Create Docker Compose configuration
* [ ] Connect FastAPI to PostgreSQL
* [ ] Connect React to FastAPI
* [ ] Add basic API health check
* [ ] Document local development setup

### Expected Result

At the end of Week 1, the complete local stack should be operational:

```text
React
  │
  │ HTTP / JSON
  ▼
FastAPI
  │
  │ SQL
  ▼
PostgreSQL
```

All services should be executable through Docker Compose.

---

## Project Structure

The initial project structure will follow this organization:

```text
video-classroom/
│
├── frontend/
│   └── React application
│
├── backend/
│   └── FastAPI application
│
├── database/
│   └── Database scripts and schema
│
├── docs/
│   └── Architecture and technical documentation
│
├── docker-compose.yml
├── README.md
└── .gitignore
```

This structure may evolve as new services and infrastructure components are introduced.

---

## Local Development

### Prerequisites

Before running the project locally, install:

* Git
* Docker
* Docker Compose
* Node.js
* Python

### Start the application

```bash
docker compose up --build
```

The exact ports and service configuration will be documented as the implementation progresses.

---

## Development Principles

The project follows a few principles throughout development:

* Keep the architecture simple before introducing complexity.
* Introduce technologies only when they solve a specific problem.
* Keep services independently testable.
* Use environment variables for configuration and secrets.
* Document architectural decisions.
* Use Git commits to track meaningful changes.
* Prefer reproducible development environments through Docker.
* Progressively move from local development toward AWS deployment.

---

## Future Architecture

As the project evolves, the architecture will progressively incorporate real-time communication and cloud infrastructure.

The final architecture is expected to include:

```text
                    ┌──────────────┐
                    │    React     │
                    │   Frontend   │
                    └──────┬───────┘
                           │
                      API / WebSocket
                           │
                    ┌──────▼───────┐
                    │   Backend    │
                    │   FastAPI    │
                    └───┬──────┬───┘
                        │      │
                     SQL      Real-time
                        │      │
                 ┌──────▼──┐   │
                 │PostgreSQL│   │
                 └─────────┘   │
                               ▼
                         Video Platform
                         WebRTC / SFU
                               │
                         AWS Infrastructure
```

The architecture above represents the **target direction**, not the current implementation.

---

## License

This project is currently intended as a personal learning and portfolio project.
