## NorthStar Insurance Platform

A full-stack insurance management system with Role-Based Access Control (RBAC), built using **Next.js (frontend)** and a REST API backend.

The platform supports policies, claims, amendments, reductions, and administrative workflows with secure authentication and role-based permissions.

## Setup Instructions

### Prerequisites
- Node.js (v18+ recommended)
- npm or yarn
- Backend API running (required for full functionality)

## Frontend Setup

1. Clone the repository:
2. git clone <your-repo-url>
cd frontend

2. Install dependencies:
npm install
3. Create environment file:
NEXT_PUBLIC_API_BASE_URL=http://localhost:5000
4. Run the development server:
npm run dev
5. Open:
http://localhost:3000
## Authentication
Users authenticate using username and password
JWT token is stored in localStorage
Supports:
Local authentication
Keycloak session mode (optional)
## Features
## Authentication & Authorization
Login / Logout system
JWT authentication
Persistent session storage
Role-Based Access Control (RBAC)
## Roles
- ADMIN
- CUSTOMER
- UNDERWRITER
- CLAIMS_ADJUSTER

# Features:

Route protection with RoleGuard
Conditional sidebar navigation
Role-based access to review pages
Admin-only management pages
## UI System
Application shell layout (PageShell)
Sidebar navigation
Topbar with user info
Section headers
Empty state and status badge components
## Core Modules
# Policies
View insurance policies
Life, Car, Home insurance support
# Claims
Create and manage claims
Claim review workflow
# Amendments
Request policy changes
Underwriter/Admin review system
# Reductions
Request coverage reductions
Approval workflow
## API Integration
Centralized API client (apiRequest)
Typed API responses
Automatic token injection
Error handling system
Safe JSON parsing
## API Endpoints
# Auth
POST /auth/login
# Policies
GET /policies

GET /policies/:id
# Claims
GET /claims

POST /claims

PUT /claims/:id

DELETE /claims/:id
# Amendments
GET /amendments

POST /amendments

GET /amendments/:id
# Reductions
GET /reductions

POST /reductions

GET /reductions/:id
# Admin
GET /admin/users

GET /admin/roles

GET /admin/rbac
## Architecture
Frontend: Next.js

State: React Context (Auth)

API Layer: Fetch wrapper

Security: RBAC system

UI: Modular components

