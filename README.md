# GymTrackerApp

> **Master your progress.** A full-stack solution for tracking gym performance, managing workout routines, and visualizing strength progression over time.

### Backend
[![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.5-6DB33F?style=for-the-badge&logo=springboot)](https://spring.io/projects/spring-boot)
[![Flyway](https://img.shields.io/badge/Flyway-Migrations-CC0200?style=for-the-badge&logo=flyway)](https://flywaydb.org/)

### Frontend
[![React](https://img.shields.io/badge/React-19.x-61DAFB?style=for-the-badge&logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7.x-646CFF?style=for-the-badge&logo=vite)](https://vitejs.dev/)
[![TanStack Query](https://img.shields.io/badge/TanStack_Query-5.x-FF4154?style=for-the-badge&logo=reactquery)](https://tanstack.com/query/latest)

### Infrastructure & Tools
[![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?style=for-the-badge&logo=docker)](https://www.docker.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-DATABASE-4169E1?style=for-the-badge&logo=postgresql)](https://www.postgresql.org/)

---

## Preview

*An intuitive, mobile-responsive dashboard built with Tailwind CSS to track your progress at a glance.*

![GymTrackerApp Dashboard](./assets/dashboard.png)


---

## Features

### Track your progress
*Monitor your strength gains and volume metrics with interactive, real-time data visualization.*

<p style="text-align: center">
  <img src="assets/track-progress.gif" alt="Progress Visualization" width="800" style="border-radius: 8px; border: 1px solid #ddd;">
</p>

---

### Log your workouts
*Streamlined interface for logging exercises, sets, and reps. Optimized for quick entry during active rest periods.*

<p style="text-align: center">
  <img src="assets/log-workout.gif" alt="Workout Logging" width="800" style="border-radius: 8px; border: 1px solid #ddd;">
</p>

---

### Custom Routine Management
*Define your own workout templates and exercises. The system handles complex relational data to keep your history organized.*

<p style="text-align: center">
  <img src="assets/add-exercise.gif" alt="Adding Exercise" width="800" style="border-radius: 8px; border: 1px solid #ddd;">
</p>

<p style="text-align: center">
  <img src="assets/add-workout.gif" alt="Adding Workout" width="800" style="border-radius: 8px; border: 1px solid #ddd;">
</p>

---

### Mobile-First Experience
*Designed with mobile-first mindset, ensuring the UI is perfectly responsive for use on the gym floor.*

<p style="text-align: center">
  <img src="assets/mobile.gif" alt="Mobile Responsiveness Visualization" width="300" style="border-radius: 8px; border: 1px solid #ddd;">
</p>

---

## System Architecture
The **GymTrackerApp** ecosystem is built as a federated system of repositories, managed via Git Submodules for maximum modularity and independent deployment.

```mermaid
graph TD
    User((User)) -->|Interacts| FE[React + TS Frontend]
    FE -->|JSON/REST| BE[Spring Boot API]
    BE -->|Hibernate/JPA| DB[(PostgreSQL)]
    
    subgraph " "
    BE
    DB
    end
```

* **Frontend:** A Type-safe React application utilizing **Tailwind CSS** for a modern UI and **TypeScript** to ensure robust data handling.
* **Backend:** A robust **Spring Boot 3** service implementing a RESTful API, following SOLID principles and Clean Architecture.
* **Data Layer:** **PostgreSQL** handles complex relational data between users, workout templates, and historical logs.

---

### Quick Start (Local Development)
This repository acts as the **System Orchestrator**. You can spin up the entire stack locally with a single command.

#### 1. Prerequisites
* **Docker Desktop** installed and running.
* **Git** installed.

#### 2. Installation & Setup
```bash

git clone --recursive https://github.com/GymTrackerApp/GymTrackerApp.git
cd GymTrackerApp
cp .env.example .env
docker-compose up --build
```

#### 3. Access Points
| Component       | URL                                            |
|:----------------|:-----------------------------------------------|
| **Frontend UI** | [http://localhost:3000](http://localhost:3000) |
| **Backend API** | [http://localhost:8080](http://localhost:8080) |
| **Database**    | `localhost:5432`                               |

---

### Technical Key Features
* **Full CRUD Lifecycle:** Create custom workout templates, exercises and log individual training sessions with persistence. Use predefined workout templates and exercises if needed. Track your progress using historical data.
* **Type-Safe Integration:** Shared interfaces between the TypeScript frontend and Java DTOs to ensure 100% contract reliability.
* **Relational Mapping:** Advanced JPA mapping for complex relationships (Users ↔ Workouts ↔ Exercises ↔ Sets). 
* **Responsive UI:** Fully optimized for mobile devices, allowing users to log sets comfortably on the gym floor.
* **Containerized Orchestration:** Fully orchestrated via Docker Compose for a seamless "production-like" local environment.

---

### Project Ecosystem
This project is split into specialized repositories to demonstrate real-world development workflows:

* **/frontend** — The [React/TypeScript source code](https://github.com/GymTrackerApp/frontend)
* **/backend** — The [Spring Boot source code](https://github.com/GymTrackerApp/backend)
* **/GymTrackerApp** — The [Main Orchestrator Repository](https://github.com/GymTrackerApp/GymTrackerApp)

---
