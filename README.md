# NestLance – AI-Powered Freelancer CRM & Automation

This repository is a **showcase project** for my **portfolio and CV**, demonstrating expertise in **full-stack development** using **Nx, NestJS, Swagger, and Angular**.
It is designed to manage **freelancers & consultants** by automating client interactions, invoicing, and project management with AI-powered features.

## 🚀 Purpose
This project is built for **learning and demonstration purposes**, showcasing:

✅ **Microservices Architecture** – Scalable backend with **NestJS & Fastify**  
✅ **AI-Powered Proposal Generator** – Automates client proposals using **OpenAI**  
✅ **Smart Invoicing & Payments** – **Stripe & PayPal integration** for automated billing  
✅ **Task & Project Management** – **Kanban board, deadlines, milestones**  
✅ **Time Tracking & Expense Management** – Logs billable hours & financial insights  
✅ **Event-Driven System** – Uses **RabbitMQ** for async microservice communication  
✅ **Containerized Deployment** – **Docker & Kubernetes** integration  
✅ **Dynamic Module Federation** – **Nx workspace optimization** for microfrontends  
✅ **Environment Management** – Secure **env validation & configuration**

This project serves as a **technical showcase** to highlight **full-stack development, DevOps, and AI automation skills** perfect for my **CV & portfolio**. 🚀🔥

Check out the source code and **see how its built!** 💼💡

## User story

## Architecture
    
```mermaid
flowchart LR
  %% Defining Styles
  classDef ui fill:#D9B3FF,stroke:#333,stroke-width:1px; 
  classDef api fill:#FFA07A,stroke:#333,stroke-width:1px;
  classDef db fill:#4682B4,stroke:#333,stroke-width:1px; 
  classDef test fill:#20B2AA,stroke:#333,stroke-width:1px; 

  %% UI Services
  subgraph UI Services
    shell["Shell (UI)"]:::ui
    auth["Auth UI"]:::ui
    crm["CRM UI"]:::ui
  end

  %% API Services
  subgraph API Services
    ms-auth["Auth API"]:::api
    ms-auth-db[(MySQL - Auth)]:::db
    ms-crm["CRM API"]:::api
    ms-crm-db[(MySQL - CRM)]:::db
  end

  %% E2E Tests
  subgraph End-to-End Testing
    shell-e2e["Shell E2E"]:::test
    auth-e2e["Auth E2E"]:::test
    crm-e2e["CRM E2E"]:::test
    ms-auth-e2e["MS-Auth E2E"]:::test
    ms-crm-e2e["MS-CRM E2E"]:::test
  end

  %% Dependencies & Connections
  ms-auth-e2e --> ms-auth
  ms-crm-e2e --> ms-crm
  shell-e2e --> shell
  auth-e2e --> auth
  crm-e2e --> crm
  shell --> auth
  shell --> crm
  crm --> ms-crm  
  
  %% CRM UI connects to CRM API

  %% Database Connections
  ms-auth --> ms-auth-db
  ms-crm --> ms-crm-db
```
