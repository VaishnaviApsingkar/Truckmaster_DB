# 🚛 Truckmaster DB

A relational database project designed to simulate and manage operations for a logistics and transportation company. This database is built using **SQL Server Management Studio**, **Erwin** and includes advanced concepts such as constraints, views, triggers, stored procedures, dynamic data masking, row-level security, and role-based permissions.

---

## 📌 Objectives

- Create a fully normalized relational database
- Implement data integrity using:
  - Primary and Foreign Keys
  - CHECK Constraints
- Implement advanced features:
  - Views with JOINs
  - Triggers to restrict invalid data
  - Stored Procedures for reusable queries
  - Dynamic Data Masking for confidential data
  - Row-Level Security for controlled access
  - Role-based user permissions

---

## 🧱 Database Schema

- **Driver**: Stores driver information (ID, name, salary, status)
- **Truck**: Truck inventory with purchase dates
- **Trip**: Travel records linking drivers and trucks
- **Expense**: Records all trip expenses
- **RoadExpenses / LivingExpenses**: Specific expense types
- **Maintenance**: Repair records for trucks

## 🧩 Data Modeling: LDM and PDM

This project follows a structured data modeling approach:

- **Logical Data Model (LDM):**  
  Abstract representation of business entities and their relationships (e.g., Driver, Truck, Trip) without database-specific details. Helps define what data is needed.

- **Physical Data Model (PDM):**  
  Implementation-ready design including table structures, data types, keys, constraints, and relationships as used in SQL Server. Represents how data is stored and accessed.

Both models ensure a clean transition from conceptual planning to practical database execution.

---

## 🧮 SQL Operations Used

This project demonstrates a wide range of SQL operations essential for building and managing relational databases:

- **DDL (Data Definition Language):**
  - Creating tables, custom data types, and constraints
  - Defining primary keys, foreign keys, and check constraints

- **DML (Data Manipulation Language):**
  - Inserting, updating, and deleting data records
  - Writing complex queries using `SELECT`, `JOIN`, `GROUP BY`, and `ORDER BY`

- **DCL (Data Control Language):**
  - Granting and revoking user access permissions
  - Enforcing role-based security with `GRANT`, `DENY`, and `REVOKE`

- **TCL (Transaction Control Language):**
  - Managing data consistency using transactions (`BEGIN`, `COMMIT`, `ROLLBACK`)

- **Advanced SQL Features:**
  - Views and stored procedures for reusability
  - Triggers for enforcing business rules
  - Dynamic Data Masking for data privacy
  - Row-Level Security (RLS) for selective access control

These operations were applied in different phases of the project to ensure a robust, secure, and well-structured database.

---

## 🔧 Steps & Key Concepts Implemented

### ✅ Step 1: Schema Design & Table Creation
- Defined custom data types for dates and monetary values
- Created normalized tables for drivers, trucks, trips, expenses, and maintenance records
- Established relationships using primary and foreign keys
- Table Creation Query:
![Example: Table Creation](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/Step2_creating_data.png)

### ✅ Step 2: Data Entry and Testing
- Loaded sample data from Excel files using INSERT queries
- Validated data types, relational integrity, and formatting

### ✅ Step 3: SQL Queries
- Developed queries to:
  - List road and living expenses
  - Count specific driver records
  - Join across related entities (drivers, trucks, trips)
  - Display relational insights
- Example Query:

![data fetching](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/step3_example.png)

### ✅ Step 4: Constraints and Triggers
- Added `CHECK` constraints to enforce business rules
- Created `AFTER INSERT` triggers to validate data thresholds and block invalid entries
- Constraint Query:

![constraint](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/Step4_constraint.png)
- Stored Procedure Query:

![Stored procedure](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/Step4_stored_procedure.png)
- Trigger Query:

![Trigger](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/Step4_trigger.png)

### ✅ Step 5: Views and Calculated Fields
- Built SQL views combining multiple tables for simplified access
- Used calculated fields to derive mileage and other operational metrics
- View Query:

![View](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/Step5_view.png)

### ✅ Step 6: Dynamic Data Masking
- Applied masking to sensitive columns such as driver names and salaries
- Created test users with restricted visibility for privacy enforcement
- Data Masking Query:

![data masking](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/Step6_data_masking.png)

### ✅ Step 7: Role-Based Permissions
- Defined views for specific expense and maintenance types
- Assigned user roles with SELECT access on relevant views
- Explicitly denied access where needed to test granular permissions
- Role assignment Query:

![Role assignment](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/Step7_role_assignment.png)

### ✅ Step 8: Row-Level Security (RLS)
- Applied RLS policies based on user and driver status (Full/Part-time)
- Allowed selective access to driver data through security predicates
- Role based access and Row Level Security Query:

![Role based Access and Security](https://github.com/VaishnaviApsingkar/Truckmaster_DB/blob/main/images/Step8_access_security.png)

  Note: All the detailed queries and their result is available in respective files.

---

## 💼 Technologies Used

- Erwin Data Modeler for database model design and schema generation
- Microsoft SQL Server 2022 
- SSMS for database design and execution
- Microsoft Word & Excel for documentation and test data

---

## 👩‍💻 Author

**Vaishnavi Pravin Apsingkar**  

---

## 📜 License

Strictly for academic and educational use only.
