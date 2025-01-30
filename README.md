# Employee Retention System

## Overview
The key to success in any organization is attracting and retaining top talent. However, the ongoing trend of employee attrition—the gradual reduction in workforce size—poses a significant challenge. Attrition occurs when employees leave at a faster rate than they are hired, impacting productivity and stability.

The **Employee Retention System** is designed to help companies enhance their employee retention rates by leveraging both **Employee Data** and **HR Data**. By integrating and analyzing these datasets, the system provides deeper insights into workforce trends, helping organizations make data-driven decisions to improve employee satisfaction and reduce turnover.

This system will be developed using **MySQL** for efficient data storage and management, ensuring scalability and performance.

---

## ER Diagram
The **Employee Database ER Diagram** provides a structured representation of employee-related data within an organization. It defines relationships between key entities, enabling efficient management of employee records, job details, payroll, absenteeism, satisfaction ratings, and departmental information.

### Database Entities and Relationships

### **1. Employee Details**
- **Primary Key:** `Employee ID`
- **Attributes:** First Name, Last Name, Gender, Age, SSN (FK), Marital Status, Address, State, Country, Phone Number.

### **2. Employee Profile**
- **Primary Key:** `Employee ID`
- **Foreign Keys:** `Department ID`, `Job ID`, `Manager ID`
- **Attributes:** Location, Date of Joining (DOJ), Education, Education Level.

### **3. Department Details**
- **Primary Key:** `Department ID`
- **Attributes:** Department Name, Count, Revenue, Investment Cost, Location, Standard Hours.

### **4. Job Details**
- **Primary Key:** `Job ID`
- **Foreign Key:** `Department ID`
- **Attributes:** Job Title, Job Description, Job Level.

### **5. Payroll Data**
- **Primary Key:** `SSN`
- **Attributes:** Base Pay, Overtime Pay, Other Pay, Benefits, Total Pay, Total Pay Benefits, Year, Percentage Salary Hike, Stock Option Level.

### **6. Absenteeism**
- **Foreign Key:** `Employee ID`
- **Attributes:** Month of Absence, Day of Week, Transportation Expense, Distance from Residence, Work Hours, Disciplinary Failure, Social Drinker, Social Smoker, Reason for Absence, Business Travel.

### **7. Employee Satisfaction Rating**
- **Foreign Key:** `Employee ID`
- **Attributes:** Manager ID, Job Satisfaction, Performance Rating, Relationship Satisfaction, Years with Manager.

---

## Relationships
- **Employee Details** is linked to **Payroll Data** through `SSN`.
- **Employee Profile** connects employees to **Departments** and **Jobs**.
- **Absenteeism** references employees through `Employee ID`.
- **Employee Satisfaction Rating** links to **Employees** and their **Managers**.
- **Departments** and **Jobs** have a relationship via `Department ID`.

---

## Technologies Used
- **Database Management System:** MySQL
- **Data Model:** Relational Database Model (RDBMS)

---

## Use Cases
- Track employee demographics and career progression.
- Monitor absenteeism trends and analyze factors affecting attendance.
- Evaluate employee job satisfaction and performance.
- Manage payroll and benefits efficiently.
- Optimize HR policies based on data-driven insights.

---



