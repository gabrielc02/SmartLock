# SmartLock System
> **A high-consistency backend engine for intelligent locker management.**

## The Goal
I built this project to transition from a "coder" mindset to a **Software Architect** mindset. The goal wasn't just to make a locker open or close, but to solve a real-world problem—physical security and logistics—using a rigorous engineering checklist. 

This project demonstrates how to handle **state integrity**, **low-latency communication**, and **defensive programming** using Golang.

## The Checklist
To ensure the quality, I followed an architectural checklist:

1.  **Domain-Driven Design (DDD):** Isolating the business rules from the technology.
2.  **Finite State Machine (FSM):** Preventing invalid state transitions (e.g., an available locker cannot be "opened" without being reserved).
3.  **Consistency over Speed:** Utilizing Go’s strong typing and database transactions to ensure zero data corruption.
4.  **Observability:** Structured logging and health metrics to understand "why" a failure happened in the field.
5.  **Simulated Environment:** A Blender 3D integration to validate backend logic against a physical-style interface.

## Architectural Breakdown (C4 Model)
Instead of a monolithic 100-page document, I’ve structured the documentation to be "zoomable" and actionable:

*   **[L1: Context](/docs/context.md)** - The Problematic: Why this system exists and who uses it.
*   **[L2: Containers](/docs/containers.md)** - The Tech Stack: Why Go, Docker, and SQLite were chosen.
*   **[L3: Components](/docs/components.md)** - The Logic: Deep dive into the State Machine and Service layers.
*   **[L4: Code](/docs/code.md)** - Implementation: API Specs and testing strategies.
*   **[ADR: Decision Records](/docs/decisions/)** - The "Why": My justifications for every major technical choice.

## Tech Stack
- **Language:** Golang (Performance & Strict Typing)
- **Containerization:** Docker & Docker Compose
- **Database:** SQLite (Relational integrity for edge computing)
- **Simulation:** Blender 3D (via Python bridge)
- **CI/CD:** GitHub Actions (Automated testing & linting)

## Quick Start
```bash
# Clone the repository
git clone https://github.com

# Initialize dependencies
go mod download

# Run the system
docker-compose up -d
```

---
*Created with a focus on solving real problems through disciplined software architecture.*
