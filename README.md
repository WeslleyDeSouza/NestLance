# NestLance – AI-Powered Freelancer CRM & Automation

This repository is a **showcase project** for my **portfolio and CV**, demonstrating expertise in **full-stack development** using **Nx, NestJS, Swagger, and Angular**.
It is designed to manage **freelancers & consultants** by automating client interactions, invoicing, and project management with AI-powered features.

coming soon... 

## User story
...

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
