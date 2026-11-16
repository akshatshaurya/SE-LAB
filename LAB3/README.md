# Lab 3 – Component Modelling & Architectural Pattern Selection

**Project:** Project Management System  
**Author:** Akshat Shaurya  
**SRN:** PES2UG24CS047  

## Overview
This lab designs the software architecture for the Project Management System specified in Lab 1. It includes a UML component diagram, the choice of an architectural pattern (Layered Architecture) with a written justification, and a full Software Architecture and Design (SAD) specification.

## Contents

| File | Description |
| :--- | :--- |
| [PES2UG24CS047_LAB3_SAD.pdf](PES2UG24CS047_LAB3_SAD.pdf) | Software Architecture and Design Specification |
| [PES2UG24CS047_Component_Diagram.pdf](PES2UG24CS047_Component_Diagram.pdf) | UML component diagram (layered architecture) |
| [PES2UG24CS047_System_Justification.pdf](PES2UG24CS047_System_Justification.pdf) | Written justification for the chosen architecture |

## Chosen Architecture: Layered

| Layer | Components | Responsibility |
| :--- | :--- | :--- |
| **Presentation** | Web UI (Dashboard, Project & Task Views, Forms, Reports) | User interaction, navigation and presentation of data |
| **Business** | Authentication Service, Project Service, Task Service, Notification Service | Core business logic: authentication & RBAC, project and member management, task assignment & status tracking, alerts and reminders |
| **Data** | PMS Database | Persistent storage of users, projects, tasks, memberships and notifications |

The UI talks to the business services over HTTPS/REST. Each service exposes its own interface (Auth API, Project API, Task API, Notification API) and reaches the database only through the data layer.

## Why Layered?
- **Clear separation of concerns:** authentication, project management, tasks, notifications and storage stay independent, so each is easier to maintain and test.
- **Fits the system:** a traditional business application with central rules and structured data doesn't need the operational overhead of microservices.
- **Security:** authentication and role-based access control are enforced in the business layer before any request reaches the database, and HTTPS protects client–server traffic.
- **Performance:** queries and business logic can be optimized without changing the UI.

## What the SAD covers
- **Introduction:** purpose, scope, audience, definitions
- **Document Overview:** how to use the document, related documents
- **Architecture:** goals & constraints, stakeholders, component diagram & descriptions, pattern rationale, technology stack, risks, traceability, security architecture, ADRs
- **Design:** design overview, UML sequence diagrams, API design, error handling/logging/monitoring, UX design, deployment view, open issues
- **Appendices:** glossary, references, completeness checklist
