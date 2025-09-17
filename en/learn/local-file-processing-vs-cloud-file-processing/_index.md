---
title: "What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud?"
second_title: "Document"
ArticleTitle: "What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud?"
linktitle: "Local File Processing vs. Cloud File Processing"
type: docs
url: /learn/local-file-processing-vs-cloud-file-processing/
description: "What is the difference between local file processing and cloud file processing? Local file processing and cloud file processing are two fundamentally different data management paradigms, with significant differences in storage infrastructure, business processing, access, cost structure, security, and applicable scenarios."
weight: 10
kwords: Excel Cloud API, REST, Spreadsheet, PDF, CSV, Json, Markdown, Local File Processing vs. Cloud File Processing
---

Local file processing and cloud file processing are different data management paradigms, with significant differences in file storage infrastructure, business processing, access, cost structure, security, and applicable scenarios. The main differences between the two are:

## 1. File storage location and infrastructure

- Local file:

  - Files are stored on physical devices that the user owns or manages, such as the hard drive of a personal computer, internal servers, or external mobile hard drives. These devices can be accessed directly by the Cells Cloud client.
  - The customer has complete physical control over the hardware.
  - The purchase, maintenance, upgrade and retirement of the infrastructure is the responsibility of the user or their organization.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- Cloud file:

  - Files are stored in remote data centers operated by third-party cloud service providers (Aspose cloud storage, Dropbox, AWS, Google Cloud, Microsoft Azure). AWS, Dropbox, Google Cloud, and Microsoft Azure can all connect people to Aspose cloud storage.
  - Customers access these files over the Internet, regardless of the location and maintenance of the underlying hardware.
  - The infrastructure is the responsibility of the cloud service provider, and users use it on demand.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import UploadFileRequest, ExportSpreadsheetAsFormatRequest, SaveSpreadsheetAsRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Upload local file to cloud storage
api.upload_file( UploadFileRequest("D:\\Data\\EmployeeSalesSummary.xlsx", "PythonSDK/EmployeeSalesSummary.xlsx"))
# Export cloud file to specified format file to local storage
api.export_spreadsheet_as_format( ExportSpreadsheetAsFormatRequest( "EmployeeSalesSummary.xlsx","pdf" ,folder= "PythonSDK"  ) , local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf" )
# Or Save an Excel file of Cells Cloud as another format file of Cells Cloud. 
api.save_spreadsheet_as( SaveSpreadsheetAsRequest (  "EmployeeSalesSummary.xlsx","pdf" ,folder= RemoteFolder ) )

```

## 2. Business processing

Regardless of local file processing or cloud file processing, all business processing is completed in the Cells Cloud server, **so Internet support is required**.

## 3. Data Access

- Local file processing:

  - Access is usually limited to the device itself.
  - Multi-person collaboration is difficult.
  - Inconvenience in changing equipment or location.

- Cloud file processing:

  - Access files from any device (computer, phone, tablet) anytime, anywhere, as long as you have an Internet connection.
  - Natural support for multi-person real-time collaboration, multiple users can edit the same document at the same time, the system automatically handles version control.
  - Strong mobility, flexible office support, and remote work.
  
## 4. Cost structure and security

- Local file:
  
  - High capital expenditure in the early stage requires certain costs for operational support in the later stage.
  - Physical security and network security are both controlled by the users themselves.

- Cloud file:

  - Low upfront investment, mainly operating expenses, pay on demand.
  - Security and integrity are the responsibilities of the cloud service provider.

## 5. Applicable scenarios

- Local file: File operations can only be performed locally.
- Cloud file: File operations can be performed locally or in the cloud.
