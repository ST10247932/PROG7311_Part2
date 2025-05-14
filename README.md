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

> These steps are only necessary if you are not watching the video demonstration.

1. **Clone the repository** into Visual Studio.
2. **Install all NuGet packages** listed above.
3. Create a database in **SQL Server Management Studio (SSMS)**.
4. Configure your connection string in `appsettings.json`.
5. Run the following command in the Package Manager Console to apply migrations:
6. Press `F5` or click **Run** to launch the web application in your browser.

---

## 🎥 Video Demonstration

📺 YouTube Link (Unlisted): **[To Be Added]**

The video includes:
- Project overview
- Architecture & database explanation
- Step-by-step demo of features
- UI walkthrough and challenges encountered

---

## 📫 Contact

Created for the PROG7311_PART_2 submission.  
If you have any questions, feel free to reach out.

