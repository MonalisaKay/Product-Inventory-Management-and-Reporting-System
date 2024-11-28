# Product-Inventory-Management-and-Reporting-System

  

## Description  
This project is a proof-of-concept application that integrates an **Angular frontend** and a **.NET 6 Web API backend** to manage inventory and generate reports. The system provides user authentication, product management, and reporting features.  

---

## Features  

### **Authentication**  
- **Login Page**:  
  - User authentication using email and password.  
  - Redirects to the Product Listing page on successful login.  
  - Includes a "Register here" link for new users.  
- **Register Page**:  
  - Allows user registration with email and password.  
  - Passwords are securely stored using hashing.  
  - Redirects to the login page upon successful registration.  

### **Product Management**  
- **Product Listing Page**:  
  - Displays products in a table format with columns for Image, Name, Price, Description, Brand, and Product Type.  
  - Supports sorting by any column and filtering products by search terms.  
  - Pagination options to display 3, 5, or 10 items per page.  

- **Add Product Page**:  
  - Enables users to add products with validations for all input fields.  
  - Upload product images and associate products with Brands and Product Types.  
  - Redirects to the Product Listing page with a success notification upon adding a product.  

### **Reporting**  
- **Reporting Page**:  
  - Displays two bar charts:  
    - Product count grouped by Brand.  
    - Product count grouped by Product Type.  
  - Generates an "Active Products Report" using an accordion to display active products under their respective Brand and Product Type combinations.  

---

## Technologies Used  
- **Backend**:  
  - .NET 6 Web API with Entity Framework Core for database operations.  
  - MS SQL Server for data storage.  

- **Frontend**:  
  - Angular for the user interface.  
  - Angular Material for UI components like tables, forms, and accordion.  

---

## Installation  

### **Prerequisites**  
- Visual Studio 2022 or later for API development.  
- Node.js and Angular CLI for the frontend.  
- SQL Server for database management.  

### **API Setup**  
1. Navigate to the API project folder:  
   ```bash
   cd Assignment03-API


## Update the appsettings.json file with your SQL Server connection details:
json
Copy code
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=INF354Assignment3;Trusted_Connection=True;MultipleActiveResultSets=True"
}

## Run the following commands to create the database and tables:
bash
Copy code
dotnet ef migrations add InitialMigration  
dotnet ef database update 

## Run the SQL data script (SqlDataCodeScript.sql) to seed the database with initial data.
Start the API:
bash
Copy code
dotnet run  

## Angular Setup
## Navigate to the Angular project folder:
bash
Copy code
cd Assignment03-Angular
##Install dependencies:
bash
Copy code
npm install  
## Start the Angular app:
bash
Copy code
ng serve  
