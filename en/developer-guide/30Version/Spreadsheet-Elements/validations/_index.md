---
title: "Working with Excel Data Validation"
second_title: "Document"
linktitle: "Validations"
type: docs
url: /validations/
keywords: "Excel data validation, Aspose.Cells Cloud, REST API, spreadsheet, Office Cloud, Excel validation API, dropdown list cell, date range validation"
description: "Programmatically manage Excel data validation rules via Aspose.Cells Cloud REST API: add, get, update, delete, and clear validations in worksheets."
date: 2024-06-15
ArticleTitle: "Working with Excel Data Validation - Aspose.Cells Cloud API Documentation"
aliases: ["/cells/validations/"]
weight: 100
---

Excel data validation is a feature in Microsoft Excel used to control what a user can enter in a cell of a worksheet. It can restrict entries to a specific date range, whole numbers only, or even create drop‑down lists that save space and display values in a single cell. You can also define a custom message that appears when a user enters an incorrect value or an invalid format.

For example, a user can specify a meeting scheduled between 9:00 AM and 6:00 PM.

Data validation can be used to ensure a value is a positive number, a date between the 15th and 30th of a month, a date occurring within the next 30 days, or a text entry containing fewer than 25 characters, and so on.

## Why Use Data Validation?

Data validation rules help enforce data integrity by restricting input types and values. This guide covers core operations via the Aspose.Cells Cloud REST API, including sample code for common languages.

### API Summary

| Operation | HTTP Method | Endpoint | Description |
|-----------|-------------|----------|-------------|
| Add | POST | `/cells/{file}/worksheets/{sheet}/validations` | Create a validation rule |
| Get | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Retrieve a specific rule |
| Get All | GET | `/cells/{file}/worksheets/{sheet}/validations` | List all rules |
| Update | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Modify a rule |
| Delete | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Remove a rule |
| Clear | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | Remove all rules |

## Working with validations on an Excel file

- [How to add a validation rule to an Excel worksheet](/cells/validations/add/)
- [How to get a validation rule from an Excel worksheet](/cells/validations/get/)
- [How to get all validation rules from an Excel worksheet](/cells/validations/get-all/)
- [How to delete a validation rule from an Excel worksheet](/cells/validations/delete/)
- [How to clear all validation rules from an Excel worksheet](/cells/validations/clear/)
- [How to update a validation rule on an Excel worksheet](/cells/validations/update/)