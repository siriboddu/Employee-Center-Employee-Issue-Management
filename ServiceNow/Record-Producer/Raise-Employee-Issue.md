# Raise Employee Issue – Record Producer

## Overview

The **Raise Employee Issue** Record Producer provides employees with a simple form to submit workplace issues through the ServiceNow Employee Center portal.

## Record Producer Details

| Property | Value |
|---|---|
| Name | Raise Employee Issue |
| Application | Employee Center |
| Target Table | Employee raises issue |
| Table Name | x_2088391_employ_0_employee_raises_issue |

## Variables

| Order | Question | Variable Name | Type |
|---:|---|---|---|
| 100 | What is the Requester name | requester | Reference |
| 200 | Which Category | category | Select Box |
| 300 | What is Subcategory | subcategory | Select Box |
| 400 | Which State is this issue | which_state_is_this_issue | Select Box |
| 500 | Short description | short_description | Single Line Text |

## Field Mapping

The Record Producer variables are mapped to the corresponding fields in the Employee raises issue table.

This allows information entered by the employee to be stored as a backend issue record.

## Submission Process

1. Employee opens the Employee Center portal.
2. Employee selects **Raise Ticket**.
3. The **Raise Employee Issue** Record Producer opens.
4. Employee enters the required issue information.
5. Employee clicks **Submit**.
6. ServiceNow creates a record in the Employee raises issue table.
7. An issue number with the `EMP` prefix is generated.

## Testing

The Record Producer was successfully tested.

Example generated issue:

`EMP0001010`

This confirmed that the Record Producer can successfully create records in the custom Employee raises issue table.

## Category and Subcategory Dependency

The Category and Subcategory dependency is configured at the table level.

However, the table-level dependency does not automatically apply to variables inside the Record Producer. A separate Record Producer-specific approach is required to filter Subcategory based on the selected Category.

This behavior was identified during testing and discussed with the project mentor.

## Purpose

The Record Producer provides a standardized and user-friendly method for employees to submit issues while ensuring that the information is stored in the custom issue-management table.
