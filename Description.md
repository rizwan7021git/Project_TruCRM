# Multi-Tenant CRM System

A lightweight CRM platform designed to manage lead data, automate data cleaning (ETL), and provide structured analytics for sales teams.

This project demonstrates how raw lead datasets can be transformed into a normalized database structure suitable for CRM applications.

---

# Project Overview

Companies often purchase lead sheets from multiple vendors. These files usually contain:

- inconsistent phone formats
- duplicate leads
- inconsistent lead statuses
- messy timestamps
- multiple comment columns

This project solves that problem by building a **clean ETL pipeline and database schema** for a scalable CRM system.

---

# Core Features

• Lead data cleaning and normalization  
• Phone number normalization (`+91XXXXXXXXXX`)  
• Lead status standardization  
• Duplicate removal using latest timestamp  
• Multi-tenant CRM architecture  
• PostgreSQL normalized schema  


---

# Database Schema

Main entities used in the system:

### Tenants
Represents companies using the CRM.

| Column | Description |
|------|------|
| id | Tenant ID |
| name | Company name |
| industry | Business category |

---

### Users
Employees working under each tenant.

| Column | Description |
|------|------|
| user_id | Unique employee identifier |
| tenant_id | Company reference |
| name | Employee name |
| role | Admin / Agent |

---

### Leads
Customer leads assigned to employees.

| Column | Description |
|------|------|
| sl_no | Lead row number |
| mobile_norm | Normalized phone |
| employee_id | Assigned employee |
| new_status | Latest status |
| comments | Notes |
| created_timestamp | Lead creation time |
| modified_timestamp | Last update |

---

### Lead Acquisition
Tracks source/vendor of leads.

| Column | Description |
|------|------|
| id | Record ID |
| vendor_name | Data vendor |
| mobile_norm | Lead phone |
| created_at | Acquisition time |

---

# ETL Pipeline

The ETL process performs:

1. Raw data ingestion
2. Phone number normalization
3. Status standardization
4. Timestamp parsing
5. Deduplication (latest record)
6. Export cleaned dataset

Technologies used:

- Python
- Pandas
- Regex
- CSV/Excel processing

---

# Technologies Used

• Python  
• Pandas  
• PostgreSQL  
• Supabase  
• GitHub  
• Excel / CSV data processing  

---

# Example Use Case

Stock trading companies often buy lead data from multiple vendors.

This CRM system allows them to:

- clean and import large lead datasets
- assign leads to employees
- track lead status
- analyze lead source quality

---

# Future Improvements

- Real-time ETL automation
- Lead assignment engine
- CRM dashboard
- AI lead scoring
- Conversion analytics
- Vendor quality scoring

---

# Project Status

Early prototype demonstrating:

• ETL pipeline  
• Database schema  
• CRM architecture  

Application layer development in progress.

---

# Author

Rizwan

Building scalable CRM and data systems for lead-driven businesses.
• Supabase backend integration  
• Designed for analytics and dashboard visualization

---

# System Architecture
