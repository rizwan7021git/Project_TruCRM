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
• Supabase backend integration  
• Designed for analytics and dashboard visualization

---

# System Architecture

Raw Lead Excel
↓
Python ETL Cleaning
↓
Staging Layer
↓
Normalized PostgreSQL Schema
↓
Supabase Backend
↓
CRM Application / Analytics
