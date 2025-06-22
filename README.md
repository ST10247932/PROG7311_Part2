# Agri-Energy Connect

Agri-Energy Connect is a web-based application designed for **farmers and employees** to efficiently manage agricultural product listings and farmer profiles. This application streamlines the interaction between employees and farmers through role-based access control, offering tailored views and features for each user type.

---

## 📌 Project Overview

This application was developed to assist **farmers** in listing their agricultural products and allow **employees** to manage farmer profiles and view all listings with advanced filtering capabilities.

### 👥 User Roles:
- **Farmer**: Can register or log in, add products to their personal listing, and view only their own products.
- **Employee**: Can register or log in, add new farmer profiles, view all product listings, and filter products by **date** or **category**.

---

## 🛠️ Tech Stack

- **Language & Framework**: C#, ASP.NET Core
- **Architecture**: MVC (Model-View-Controller)
- **Database**: SQL Server Management Studio (SSMS)
- **ORM**: Entity Framework Core
- **UI**: Razor Views

---

## 🧱 Architecture & Design Pattern

The application follows the **MVC (Model-View-Controller)** design pattern for a clean separation of concerns:

- **Model**: Represents the data structure (e.g., Farmer, Product).
- **View**: Razor-based UI pages tailored for different roles.
- **Controller**: Handles incoming requests and business logic.

> I used **MVC** because it's a structured, maintainable pattern that fits well with ASP.NET Core. No changes were made to the original design from Part 1.

---

## 🗃️ Database

**SQL Server (SSMS)** was chosen due to familiarity and ease of integration with Visual Studio. Migrations were used to create and update the database schema from within the codebase.

### Why SSMS?
- I’ve always used it in past projects.
- Seamless integration with Visual Studio.
- Strong tooling support for data inspection and management.

---

## ✨ Key Features

- **Authentication**:
  - Role-based registration and login.
- **Farmer Features**:
  - List products with details (name, category, production date).
  - View their own listed products.
- **Employee Features**:
  - Add new farmer profiles with essential details.
  - View all product listings from farmers.
  - Filter product listings by:
    - **Date range**
    - **Product type/category**

---

## 🎯 Challenges & Improvements

- **UI Design**: Creating a clean, user-friendly interface was time-consuming and required multiple adjustments.
- **Filtering Logic**: The product filter initially didn’t work as intended. I wrote and tested the filtering logic separately before integrating it properly into the application.

Despite these challenges, no major design changes were made from Part 1.

---

## 📦 Required NuGet Packages

Make sure the following packages are installed in your Visual Studio project:

- `Microsoft.EntityFrameworkCore`
- `Microsoft.EntityFrameworkCore.SqlServer`
- `Microsoft.EntityFrameworkCore.Tools`
- `Microsoft.AspNetCore.Identity.EntityFrameworkCore`

---

## ⚙️ Setup Instructions

To run the application locally:

1. **Clone the Repository**
   - Open in Visual Studio

2. **Install Required NuGet Packages**
   - Use the NuGet Package Manager

3. **Configure the Database**
   - Open `appsettings.json`
   - Add your local SQL Server connection string, e.g.:
     ```json
     "ConnectionStrings": {
       "DefaultConnection": "Server=localhost;Database=AgriEnergyConnectDB;Trusted_Connection=True;"
     }
     ```

4. **Apply Migrations**
   - Open the Package Manager Console:
     ```bash
     Add-Migration InitialCreate
     Update-Database
     ```

5. **Run the Application**
   - Press `F5` or click **Run**

---

## 🗄️ Manual Database Setup (If EF Fails)

If you cannot run migrations, you can manually create the database with this SQL script:

```sql
CREATE DATABASE AgriEnergyConnectDB;
GO

USE AgriEnergyConnectDB;
GO

CREATE TABLE Farmers (
    Id INT PRIMARY KEY IDENTITY,
    FirstName NVARCHAR(100),
    LastName NVARCHAR(100),
    Email NVARCHAR(256),
    PasswordHash NVARCHAR(MAX),
    Role NVARCHAR(50)
);
GO

CREATE TABLE Products (
    Id INT PRIMARY KEY IDENTITY,
    FarmerId INT FOREIGN KEY REFERENCES Farmers(Id),
    ProductName NVARCHAR(100),
    Category NVARCHAR(100),
    ProductionDate DATE
);
GO

---
## Dummy Logins
**Employee**
Username: pillay@gmail.com
Password: Preshen@1234
**Farmer**
Username: naidoo@gmail.com or mike@gmail.com
Password: Devesh@1234 or Mike@1234

## 🎥 Video Demonstration

📺 YouTube Link (Unlisted): **https://youtu.be/al7Wkjl-Kag**

The video includes:
- Project overview
- Architecture & database explanation
- Step-by-step demo of features
- UI walkthrough and challenges encountered

---

## 📫 Contact

Created for the PROG7311_PART_2 submission.  
If you have any questions, feel free to reach out.

