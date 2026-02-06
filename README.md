# GymTrackerApp

> **Master your progress.** A full-stack, enterprise-grade solution for tracking gym performance, managing workout routines, and visualizing strength progression over time.

[![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=springboot)](https://spring.io/projects/spring-boot)

[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)

[![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?style=for-the-badge&logo=docker)](https://www.docker.com/)

---

## 🖼️ Preview

![GymTrackerApp Dashboard](./img/dashboard.png)

*An intuitive, mobile-responsive dashboard built with Tailwind CSS to track your progress at a glance.*

---

## 🏗️ System Architecture
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