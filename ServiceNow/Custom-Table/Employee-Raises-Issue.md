# Employee Raises Issue – Custom Table

## Overview

The Employee Raises Issue table is a custom table created in ServiceNow to store employee-reported issues.

## Table Details

| Property | Value |
|---|---|
| Table Label | Employee raises issue |
| Table Name | x_2088391_employ_0_employee_raises_issue |
| Application | Employee Center |
| Number Prefix | EMP |

## Fields

| Field | Type | Purpose |
|---|---|---|
| Requester | Reference | Identifies the employee who raises the issue |
| Category | Choice | Defines the main issue category |
| Subcategory | Choice | Defines the specific issue |
| State | Choice | Tracks the issue state |
| Short description | String | Provides a brief description of the issue |
| Priority | Choice | Defines the issue priority |
| Assignment Group | Reference | Defines the group responsible for the issue |

## Category and Subcategory

The configured issue categories are:

| Category | Subcategory |
|---|---|
| Hardware | Laptop |
| Network | VPN |
| Access | Forgot password |
| Software | Server |

## Purpose

The table provides a centralized location for storing and managing employee issues submitted through the Employee Center portal.

## Record Generation

The table uses the `EMP` prefix for automatically generated issue numbers.

Example:

`EMP0001010`
