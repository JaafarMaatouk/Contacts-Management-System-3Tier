# Contacts Management System (3-Tier Architecture)

A comprehensive desktop application for managing contacts, built with C# (WinForms) and SQL Server. This project strictly follows the **3-Tier Architecture** software design pattern to ensure scalability, maintainability, and separation of concerns.

## Project Overview
This system is designed to demonstrate professional software engineering practices. By separating the application into three distinct layers, the codebase becomes highly modular. The User Interface does not interact with the database directly; instead, it communicates through the Business Logic Layer, which in turn uses the Data Access Layer.

## Architecture (3 Layers)
The solution is divided into three independent projects:

1. **Presentation Layer (`ContactsPresentationLayer`):**
   - Contains all Windows Forms (UI).
   - Handles user interactions and displays data.
   - Does not contain any SQL queries or business rules.
2. **Business Logic Layer (`ContactsBusinessLayer`):**
   - Contains the core business rules and entities (e.g., `Contact.cs`, `Country.cs`).
   - Acts as a bridge between the UI and the Data Access Layer.
   - Validates data before sending it to the database.
3. **Data Access Layer (`ContactsDataAccessLayer`):**
   - Handles direct communication with the SQL Server Database.
   - Contains data access settings (`clsDataAccessSettings.cs`) and CRUD operations (`ContactData.cs`).
   - Executes SQL queries and returns results to the Business Layer.

## Features
- **Full CRUD Operations:** Add, Update, Delete, and List Contacts.
- **Database Integration:** Connected to SQL Server for persistent data storage.
- **Image Handling:** Support for uploading and saving contact images.
- **Data Lookup:** Dropdown lists populated from related database tables (e.g., Countries).
- **Context Menu:** Right-click on a contact to quickly Edit or Delete.

## Technical Details
- **Language:** C#
- **UI Framework:** Windows Forms (WinForms)
- **Database:** SQL Server (ADO.NET)
- **Design Pattern:** 3-Tier Architecture

## How to Run
1. Clone this repository or download it as a ZIP file.
2. Open the `.sln` file in **Visual Studio**.
3. **Important:** You must restore the SQL Server Database. Look for the `.sql` script in the repository (if included) and execute it in SQL Server Management Studio (SSMS).
4. Update the connection string in `clsDataAccessSettings.cs` to match your local SQL Server instance.
5. Press `F5` to build and run the application.

## License
This project is open-source and available under the MIT License.
