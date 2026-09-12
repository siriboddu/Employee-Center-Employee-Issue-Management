# Employee Center Portal

## Overview

A dedicated ServiceNow Employee Center portal was configured to provide employees with a simple and user-friendly interface for raising issues.

## Portal Details

| Property | Value |
|---|---|
| Portal Name | Requesting portal |
| URL Suffix | employee_request |
| Homepage | ec_standard_home |
| Main Menu | Employee Center Menu |
| Theme | Employee Center Coral Theme |
| Login Page | login |
| 404 Page | 404 |

## Live Portal

[Open Employee Center Portal](https://dev196740.service-now.com/employee_request)

> Note: Access to the portal may require the appropriate ServiceNow instance access and permissions.

## Portal Components

The portal contains:

- Employee Center homepage
- Commercial Widget
- Link Redirect Widget
- Raise Ticket navigation
- Raise Employee Issue Record Producer

## Page Layout

The two custom widgets were placed in a two-column layout:

| Column | Widget |
|---|---|
| Left | Commercial Widget |
| Right | Link Redirect Widget |

## User Navigation

The employee can:

1. Open the Employee Center portal.
2. View the available portal content.
3. Click **Raise Ticket**.
4. Open the **Raise Employee Issue** form.
5. Enter the required issue details.
6. Submit the issue.

## Testing

The portal was tested using the live portal URL.

The Raise Ticket navigation successfully opened the Raise Employee Issue Record Producer, and test submission successfully created a backend issue record.
