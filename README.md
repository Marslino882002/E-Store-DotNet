# EStore-DotNet-MVC-API

A comprehensive Full Stack e-commerce application focusing on two core entities: **User** and **Product**. The project is split into two main components: a secure Backend **.NET Core Web API** and a Frontend web application built with **ASP.NET Core MVC** (Razor Views).

---

## 🚀 Key Technologies

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Backend API** | .NET Core Web API | RESTful API for handling business logic and data operations. |
| **Frontend/UI** | ASP.NET Core MVC | Web application consuming the API to provide the User Interface. |
| **Database** | Microsoft SQL Server | Used for persistent data storage. |
| **ORM** | Entity Framework Core | ORM for database interactions. |
| **Authentication** | JWT & Refresh Tokens | Securing all API endpoints. |
| **Testing** | xUnit / NUnit | Implementation of **Unit Tests** and **Integration Tests**. |

---

## ✨ Project Features

### Backend API (`EStore.API`)

* **Entities:** `User` and `Product` with required properties and unique constraints.
* **Authentication:** Full implementation of **JWT (JSON Web Tokens)** for secure API access, including a **Refresh Token** mechanism to maintain sessions without re-login.
* **Product Management:** Complete set of CRUD (Create, Read, Update, Delete) endpoints for products.
* **Image Storage:** Ability to save product images to the local file system.
* **Code Quality:** Adherence to Clean Code principles, utilizing a clear architectural pattern (e.g., Repository or Service Layer).
* **Data Access:** Uses Entity Framework Core, including the option to use **Stored Procedures** for complex operations.

### Frontend MVC (`EStore.Web`)

* **User Authentication:** Fully functional **Login** page consuming the secure API.
* **Product Display:** A **Product Catalog** page to display products retrieved from the API.
* **Architecture:** Follows the standard **Model-View-Controller (MVC)** pattern for structure and separation of concerns.

---

## 🛠️ Getting Started

### 1. Prerequisites

* **.NET Core SDK** (The version used for development).
* **Microsoft SQL Server** (or SQL LocalDB installed with Visual Studio).

### 2. Database Setup

The database will be created/updated using Entity Framework Core Migrations or by executing the provided SQL Script/Backup.

1.  **Configure Connection String:**
    * Open `appsettings.json` in the `EStore.API` project.
    * Update the connection string to point to your local SQL Server instance.

2.  **Run Migrations (Preferred):**
    ```bash
    # Navigate to the API project directory
    cd EStore.API
    dotnet ef database update
    ```
    *(Alternatively, use the provided SQL Script or Database Backup to create the `EStoreDB`.)*

### 3. Running the Application

You must run both the API and the MVC application simultaneously.

#### A. Run the Backend API

```bash
# Navigate to the API directory
cd EStore.API
dotnet run
