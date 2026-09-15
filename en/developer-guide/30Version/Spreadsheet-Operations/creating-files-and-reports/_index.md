---
title: "Create Excel Files and Build Excel Reports"
second_title: "Document"
date: 2024-05-15
type: docs
url: /creating-files-and-reports/
aliases: [/workbook/create/]
linktitle: "Create Excel and Report"
tags: ["excel", "cloud", "reporting"]
categories: ["cells", "tutorials"]
description: "Step-by-step guide to create Excel workbooks and build dynamic reports using Aspose.Cells Cloud API, including SmartMarker template processing and code examples."
ArticleTitle: "Create Excel Files and Build Excel Reports – Aspose.Cells Cloud API"
---

Using the Aspose.Cells Cloud API, you can effortlessly create new Excel workbooks and generate workbooks from template files. It also supports creating advanced Excel reports with the SmartMarker feature, which can handle a variety of data‑processing and reporting needs.

**Prerequisites**: Before you begin, ensure you have a valid Aspose Cloud API key and the Aspose.Cells Cloud SDK installed for your development language.

- ✅ An Aspose Cloud account with valid [API key and App SID](https://dashboard.aspose.cloud/)  
- ✅ Aspose.Cells Cloud SDK for your language (e.g., `pip install aspose-words-cloud` for Python)  
- ✅ Basic familiarity with Excel file structure and JSON data formats  

## Create an Excel file and build a report

- [Create an empty Excel workbook using Aspose.Cells Cloud API](/cells/create-an-empty-excel-file/)
- [Generate Excel files from template (.xlsx) using Aspose.Cells Cloud](/cells/create-an-excel-file-with-template-file/)
- [Build dynamic Excel reports with SmartMarker data binding](/cells/build-report-with-smart-marker/)
- [Assemble structured data sources for SmartMarker-based Excel reports](/cells/assembly-data-for-the-creation-of-an-excel-report/)

### Example: Create an empty Excel workbook (Python)

```python
from aspose.cells.cloud import CellsApi
import os

client_id = "xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
client_secret = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"

api = CellsApi(client_id, client_secret)

response = api.cells_workbook_put_create_workbook(name="EmptyWorkbook.xlsx")
print("Workbook created:", response)
```

### Example: Generate report using SmartMarker (Node.js)

```javascript
const { CellsApi, Workbook } = require("aspose-cells-cloud");

const clientId = "xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx";
const clientSecret = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx";
const cellsApi = new CellsApi(clientId, clientSecret);

const templateFile = "ReportTemplate.xlsx";
const dataFile = "reportData.json";

const response = await cellsApi.cellsWorkbookPostSmartMarkers(
  templateFile,
  dataFile,
  outPath = "ReportWithMarkers.xlsx"
);
console.log("Report generated:", response);
```

The SmartMarker feature processes your template file and populates it with structured data (e.g., JSON, XML, or database records) to produce a final Excel report — ideal for dynamic reporting, dashboards, and data exports.

For a visual overview, see the SmartMarker workflow below:

![SmartMarker data assembly and template processing flow](/images/smartmarker-flow.png)

*alt="Diagram: Template file, data source, and SmartMarker engine producing final Excel report"*

Related Resources:
- [Aspose.Cells Cloud API Reference](https://reference.aspose.cloud/cells/)
- [SDK Source Code & Samples](https://github.com/aspose-cells-cloud)
- [SmartMarker Syntax Guide](/cells/smartmarker-syntax/)