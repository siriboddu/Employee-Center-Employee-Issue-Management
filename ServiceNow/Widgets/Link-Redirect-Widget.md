# Link Redirect Widget

## Overview

The Link Redirect Widget is a custom ServiceNow Service Portal widget created to provide employees with a direct way to raise an issue.

The widget displays a **Raise an Issue** option with a **Raise Ticket** button.

## Purpose

The main purpose of this widget is to provide quick navigation from the Employee Center homepage to the **Raise Employee Issue** Record Producer.

## User Flow

1. Employee opens the Employee Center portal.
2. Employee sees the **Raise an Issue** widget.
3. Employee clicks **Raise Ticket**.
4. The widget redirects the employee to the **Raise Employee Issue** Record Producer.
5. Employee enters the issue details.
6. Employee submits the request.

## Widget Components

### HTML

The widget contains:

- Raise an Issue heading
- Submit request/complaint description
- Raise Ticket button

### Client Controller

The widget uses ServiceNow client-side navigation to open the Record Producer.

The Record Producer is identified using its ServiceNow `sys_id`.

## Portal Placement

The Link Redirect Widget was placed in the **right column** of the Employee Center homepage.

## Technology

- HTML
- JavaScript
- AngularJS / ServiceNow Service Portal APIs
- ServiceNow Service Portal Widget framework

## Testing

The widget was tested from the Employee Center portal.

Clicking **Raise Ticket** successfully opened the **Raise Employee Issue** Record Producer.
