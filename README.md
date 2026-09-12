# Employee Center – Employee Issue Management System

A ServiceNow-based Employee Center portal designed to provide employees with a standardized and user-friendly way to raise workplace issues.

## 📌 Project Overview

The Employee Issue Management System provides a centralized platform for employees to submit issues through a ServiceNow Employee Center portal.

Employees can enter information such as requester, category, subcategory, state, and short description. The submitted information is stored in a custom ServiceNow table for further processing and issue management.

## 🎯 Objectives

- Provide a simple employee issue submission process.
- Standardize issue categorization.
- Reduce manual effort and data inconsistencies.
- Apply business rules using UI Policies.
- Provide a dedicated Employee Center portal.
- Automatically create backend issue records.
- Improve issue visibility and resolution.

## 🛠️ Technologies Used

- ServiceNow
- Service Portal / Employee Center
- Custom Scoped Application
- Custom Tables
- Record Producers
- UI Policies
- Catalog Client Scripts
- ServiceNow Widgets
- JavaScript

## 🏗️ Project Components

### 1. Custom Scoped Application

A custom scoped application named **Employee Center** was created to contain the project-specific configuration.

### 2. Employee Raises Issue Table

A custom table was created to store employee issues.

**Table:** `Employee raises issue`

Main fields:

| Field | Type |
|---|---|
| Requester | Reference |
| Category | Choice |
| Subcategory | Choice |
| State | Choice |
| Short Description | String |
| Priority | Choice |
| Assignment Group | Reference |

The table uses an **EMP** prefix for automatically generated issue numbers.

### 3. Category and Subcategory

The project uses the following issue classification:

| Category | Subcategory |
|---|---|
| Hardware | Laptop |
| Network | VPN |
| Access | Forgot password |
| Software | Server |

### 4. Record Producer

A Record Producer named **Raise Employee Issue** was created to allow employees to submit issues from the portal.

The Record Producer contains:

- Requester
- Category
- Subcategory
- State
- Short Description

The variables are mapped to the corresponding fields in the Employee raises issue table.

### 5. UI Policies

UI Policies were configured to control field behavior and enforce business rules during issue submission.

They help control:

- Field visibility
- Mandatory fields
- Read-only behavior
- Form restrictions

### 6. Employee Center Portal

A dedicated Service Portal named **Requesting portal** was configured for employees.

**Portal URL:**

`https://dev196740.service-now.com/employee_request`

The portal provides access to the issue submission process through a customized Employee Center experience.

### 7. Custom Widgets

#### Commercial Widget

Displays information about the services provided through the Employee Center experience.

Features include:

- 24/7 Customer Support
- Faster Issue Resolution
- Transparent Tracking
- Secure & Reliable

#### Link Redirect Widget

Provides a **Raise an Issue / Raise Ticket** option.

When the user clicks the button, the widget opens the **Raise Employee Issue** Record Producer.

## 🔄 System Workflow

```text
Employee
   ↓
Employee Center Portal
   ↓
Raise an Issue
   ↓
Raise Employee Issue Record Producer
   ↓
Enter Issue Details
   ↓
Submit
   ↓
Employee Raises Issue Table
   ↓
Issue Number Generated
🧪 Testing

The following functionality was tested:

Employee Center portal navigation
Custom widget display
Raise Ticket navigation
Record Producer form
Issue submission
Backend record creation
Automatic issue number generation

A test submission successfully created the record:

EMP0001010

**⚠️ Known Limitation**

The Category → Subcategory dependency works at the custom table configuration level, but the same dependency does not automatically apply to variables inside the Record Producer.

This requires a separate Record Producer-specific dependency/filtering configuration.

The issue was identified during testing and discussed with the project mentor for the appropriate implementation approach.

**📈 Project Outcomes**

Created a custom ServiceNow scoped application.
Implemented an employee issue management table.
Created a dedicated Employee Center portal.
Implemented a Record Producer for issue submission.
Added custom widgets for portal navigation.
Applied UI Policies for business rules.
Successfully tested end-to-end issue submission and record creation.

**🚀 Future Enhancements**

Implement the final Category/Subcategory dependency in the Record Producer.
Add automatic notifications to assignment groups.
Add employee issue tracking.
Create dashboards and reports.
Add knowledge articles for common issues.
Improve responsive and accessibility features.

**👩‍💻 Author**

Boddu Siri

ServiceNow Employee Center – Employee Issue Management System


