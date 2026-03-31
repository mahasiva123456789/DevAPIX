# 🚀 DevAPIX

**API Productization and Developer Collaboration Platform**


## 📌 Overview

DevAPIX is a full-stack developer platform designed to **publish, manage, test, and collaborate on APIs and projects**. It combines **API marketplace features (like RapidAPI)** with **developer collaboration tools (like GitHub)** into a unified system.


# 🧩 Modules

1. Signup / Login
2. API Publishing with Documentation
3. Free / Paid API Access
4. API Sandbox Testing Tool
5. Project Upload
6. Inviting People
7. Project Contribution
8. Contribution Tracking
9. Project Discussion / Doubt Forum


# ⚙️ Features

## 🔐 Signup / Login

* Spring Security 6
* BCrypt password hashing
* JWT + Refresh Token
* Role-Based Access Control (RBAC)
* CSRF protection
* HTTPS secure cookies
* Input validation
* Security headers


## 📡 API Publishing with Documentation

### 🔹 API Types

* REST API *(primary support)*
* Optional: GraphQL APIs, Webhooks, Microservice Endpoints

**Concepts Used:**

* Transactions
* Logging
* DTO (Data Transfer Objects)
* Validation


### 🔹 Basic API Details

* API Name
* Description
* Category
* Version
* Base URL
* Visibility (Public / Private / Paid)


### 🔹 API Definition

* Upload Swagger/OpenAPI file (`.yaml`, `.json`)
* Paste Swagger URL

**Concepts Used:**

* Swagger Parser
* Logging
* Exception Handling


### 🔹 Authentication Details

* JWT Token-based authentication


### 🔹 Sample Request & Response

* Auto-generated from Swagger/OpenAPI schema
* Fallback generation using schema

**Concept Used:**

* Jackson (JSON processing)


### 🔹 Headers & Parameters

* Auto-detected from API definition

**Concept Used:**

* DTO Mapping


### 🔹 Status Codes

* Extracted from Swagger/OpenAPI responses

**Concepts Used:**

* Enum
* DTO
* Exception Handling


### 🔹 API Discovery

* Search APIs by category
* Filtering and sorting
* Pagination support

**Concepts Used:**

* Pagination
* Sorting
* Filtering


## 💰 Free / Paid API Access

* Subscription-based API plans (Free / Paid tiers)
* Secure API access using JWT

**Concepts Used:**

* Transactions (subscription + payment handling)
* AOP / Interceptor → track API usage
* Scheduler → reset free quota daily
* Pagination → subscription history
* Logging → billing and quota exceeded logs


## 🧪 API Sandbox Testing Tool

* Select HTTP methods (GET, POST, PUT, DELETE)
* Add JWT token and custom headers
* Configure query parameters and path variables
* Pre-filled request body from Swagger examples
* Execute API requests with logging
* View live response with:

  * Status code
  * Latency
  * Response size
* Error handling with detailed messages
* Request history and re-execution support


# 🏗️ Architecture (High-Level)

```text
Client (React / Frontend)
        ↓
Spring Boot Backend (DevAPIX)
        ↓
Modules:
- Auth Service
- API Catalog Service
- Subscription/Billing Service
- Sandbox Service
        ↓
Database (MySQL / PostgreSQL)
```



