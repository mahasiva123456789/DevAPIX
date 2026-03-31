# 🚀 DevAPIX

**API Productization and Developer Collaboration Platform**


## 📌 Overview

DevAPIX is a full-stack developer platform designed to **publish, manage, test, and collaborate on APIs and projects**. It combines **API marketplace features (like RapidAPI)** with **developer collaboration tools (like GitHub)** into a unified system.


# 🧩 Core Modules

1. Signup / Login
2. API Publishing with Documentation
3. Free / Paid API Access
4. API Sandbox Testing Tool
5. Project Upload
6. Inviting People
7. Project Contribution
8. Contribution Tracking
9. Project Discussion / Doubt Forum

👥 User Roles
OWNER
Creates APIs and Projects
Invites contributors
Approves contributions
Manages pricing and access
CONTRIBUTOR
Contributes to projects
Participates in discussions
Uses APIs
REVIEWER
Reviews contributions
Provides feedback
Participates in discussions

# ⚙️ Complete Feature Architecture

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
* Auto-generate API documentation
Extract:
Endpoints
Headers
Parameters
Status codes
Sample request/response

**Concepts Used:**

* Swagger Parser
* File Upload (MultipartFile)
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

📂 Project Upload
Features
Upload ZIP or GitHub link
Store project metadata
Manage project lifecycle
Concepts
File Upload (MultipartFile)
Validation
Logging
Transaction Management
Soft Delete / Archive
🤝 Inviting People
Features
Invite users to project
Accept / Reject invites
Assign roles
Concepts
Transaction
Notification Trigger (Async optional)
Pagination
Audit Logging
🛠️ Project Contribution
Features
Upload contribution files
Submit changes
Approval workflow:
Pending → Approved → Merged / Rejected
Concepts
File Upload
Transactions
Workflow Management
Logging
Enum-based Status
📊 Contribution Tracking
Features
Track every action:
Created
Updated
Approved
Rejected
Merged
Concepts
Audit Logs
Event Tracking
Pagination
Sorting (latest activity)
💬 Project Discussion / Doubt Forum
Features
Ask questions
Reply to threads
Nested discussions
Attach images/files
Mark as resolved
Structure
Question
   ↳ Reply
      ↳ Nested Reply
Concepts
Self-referencing Entity (parent_id)
Threaded Discussion Model
Pagination
Real-time extension (WebSocket optional)
👥 Project Roles
OWNER
CONTRIBUTOR
REVIEWER
Concepts
RBAC (Role-Based Access Control)
Authorization checks
Secure resource access
🔄 End-to-End Workflow
User Signup/Login
        ↓
JWT Authentication & Role Assignment
        ↓
----------------------------------------
API FLOW
----------------------------------------
Owner publishes API (Swagger Upload)
        ↓
System parses & generates documentation
        ↓
Users discover APIs (Search + Pagination)
        ↓
Subscribe to API (Free/Paid)
        ↓
Usage tracked via Interceptor
        ↓
Test API in Sandbox
        ↓
Monitor usage & limits

----------------------------------------
PROJECT FLOW
----------------------------------------
Owner uploads project (ZIP/GitHub)
        ↓
Invites contributors/reviewers
        ↓
Contributors submit contributions
        ↓
Owner/Reviewer approves or rejects
        ↓
All actions tracked (audit logs)
        ↓
Team discusses in forum
        ↓
Project evolves collaboratively
🏗️ System Architecture
Frontend (React)
        ↓
Spring Boot Backend
        ↓
Core Services:
- Auth Service
- API Catalog Service
- Subscription Service
- Sandbox Service
- Project Collaboration Service
        ↓
Database (MySQL / PostgreSQL)
🧠 Backend Concepts Summary
Spring Security (JWT + RBAC)
Pagination, Sorting, Filtering
Transaction Management
Global Exception Handling
Logging (SLF4J)
File Upload Handling
AOP / Interceptors
Scheduler (Quota Reset)
REST Client (WebClient / RestTemplate)
DTO Pattern
Layered Architecture
Audit Logging
Workflow State Management


