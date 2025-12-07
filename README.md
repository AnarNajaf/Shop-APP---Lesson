# Shop Application - .NET Web API

A modern **.NET-based e-commerce Web API** project implementing best practices such as **DTOs**, **interfaces**, **Entity Framework Core**, and **ASP.NET Identity**. This project serves as a backend for a shop or e-commerce platform, providing secure, maintainable, and scalable endpoints.

---

## Overview

This project demonstrates a professional .NET backend architecture for a shop application. It is designed to:

- Handle products, users, orders, and authentication securely.
- Provide access control via **ASP.NET Identity** with role-based authorization.
- Use **DTOs (Data Transfer Objects)** for safe and structured data transfer between frontend and backend.
- Leverage **interfaces** and dependency injection for maintainable, testable code.
- Use **Entity Framework Core (EF Core)** for database management with migrations.
- Support **.NET global.json** configuration for consistent SDK versions.

---

## Key Features

### 1. **DTOs (Data Transfer Objects)**
- Decouple database models from API responses.
- Ensure only required data is exposed to clients.
- Simplify validation and mapping between entities and client models.

### 2. **Interfaces & Dependency Injection**
- Define service contracts using interfaces (e.g., `IProductService`, `IUserService`).
- Implement business logic in services and inject them into controllers.
- Improves testability and maintainability.

### 3. **Web API**
- Built using **ASP.NET Core Web API**.
- RESTful endpoints for CRUD operations:
  - Products: `GET`, `POST`, `PUT`, `DELETE`
  - Users: registration, login, profile management
  - Orders: place, view, update
- Supports JSON input/output and standard HTTP response codes.

### 4. **Authentication & Authorization**
- Uses **ASP.NET Identity** for secure user authentication.
- Role-based authorization allows separation between admin and customer operations.
- Protects API endpoints using `[Authorize]` attributes.

### 5. **Entity Framework Core**
- Database-first or code-first approach supported.
- Automatic migrations to manage schema changes.
- Supports relational databases like SQL Server or PostgreSQL.

### 6. **.NET global.json**
- Ensures consistent .NET SDK across development machines.
- Helps avoid version conflicts and build issues.

---

## Libraries & Tools Used

- **.NET 7/8** – modern .NET runtime for Web API.
- **Entity Framework Core** – ORM for database operations.
- **ASP.NET Identity** – built-in authentication and user management.
- **AutoMapper** – mapping between entities and DTOs.
- **Swashbuckle / Swagger** – API documentation and testing.
- Optional: **FluentValidation**, **Serilog**, etc.

---

## Installation & Setup

1. **Clone the repository**
```bash
git clone https://github.com/YourUsername/ShopAppBackend.git
cd ShopAppBackend
Install dependencies

bash
Kodu kopyala
dotnet restore
Apply database migrations

bash
Kodu kopyala
dotnet ef database update
Ensure connection string in appsettings.json is configured correctly.

Run the application

bash
Kodu kopyala
dotnet run
API will be available at https://localhost:5001 or http://localhost:5000.

Test API with Swagger

Navigate to /swagger endpoint to test all available routes.

Usage
Register a user via Identity and login to access protected endpoints.

Role-based access allows admins to manage products and view all orders.

Customers can browse products and place orders.

Use API endpoints to manage users, products, and orders efficiently.

Architecture & Best Practices
Controllers – handle HTTP requests and responses.

Services – contain business logic.

Repositories / EF Core DbContext – handle database operations.

DTOs – define the shape of API data.

Interfaces – define contracts for services.

Middlewares – handle authentication, logging, and error handling.
