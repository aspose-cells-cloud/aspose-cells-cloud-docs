---
title: "Batch processing of Excel files: Convert, Lock, Protect, Split, and Unlock"
second_title: "Document"
linktitle: "Batch Excel files"
type: docs
url: /batch/
keywords: "Batch processing, Excel, conversion, lock, protect, split, unlock, Aspose.Cells Cloud API, API reference, batch operations"
description: "Aspose.Cells Cloud API enables batch processing of multiple Excel files for conversion, locking, protection, splitting, and unlocking. Includes detailed API specifications and SDK support for Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and Swift."
weight: 35
ArticleTitle: "Batch Processing of Excel Files – Convert, Lock, Protect, Split, Unlock with Aspose.Cells Cloud API"
---

The Aspose.Cells Cloud API provides batch endpoints that allow you to perform common operations on multiple Excel files in a single request. Below is a quick overview of the available batch operations together with concise API specifications for each.

- **["Batch Convert Excel Files"](https://docs.aspose.cloud/cells/batch/convert "Batch Convert Excel Files")**  
  *Convert multiple Excel files to a chosen output format in one request.*  

  **API Details**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **Parameters**  

  | Name          | Type     | Description                                    |
  |---------------|----------|------------------------------------------------|
  | files         | file[]   | One or more Excel files to convert.            |
  | outputFormat  | string   | Desired output format (e.g., pdf, csv, html). |
  | storage       | string   | (Optional) Cloud storage name.                 |

  **Responses**  

  | Code | Description                                 |
  |------|---------------------------------------------|
  | 200  | Conversion successful; returns files.       |
  | 400  | Invalid parameters supplied.                |
  | 401  | Unauthorized – missing or invalid token.    |
  | 500  | Internal server error.                      |

- **["Batch Lock Excel Files"](https://docs.aspose.cloud/cells/batch/lock "Batch Lock Excel Files")**  
  *Apply a password lock to multiple Excel files simultaneously.*  

  **API Details**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parameters**  

  | Name     | Type   | Description                              |
  |----------|--------|------------------------------------------|
  | files    | array  | List of file identifiers or URLs.        |
  | password | string | Password to lock the workbooks with.    |
  | storage  | string | (Optional) Cloud storage name.           |

  **Responses**  

  | Code | Description                                 |
  |------|---------------------------------------------|
  | 200  | Files locked successfully.                  |
  | 400  | Missing or invalid parameters.              |
  | 401  | Unauthorized access.                        |
  | 500  | Server error.                               |

- **["Batch Protect Excel Files"](https://docs.aspose.cloud/cells/batch/protect "Batch Protect Excel Files")**  
  *Add protection settings (e.g., read‑only, structure) to multiple workbooks.*  

  **API Details**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parameters**  

  | Name          | Type   | Description                                          |
  |---------------|--------|------------------------------------------------------|
  | files         | array  | List of file identifiers or URLs.                    |
  | protection    | object | Protection options (e.g., readOnly, structure).     |
  | storage       | string | (Optional) Cloud storage name.                       |

  **Responses**  

  | Code | Description                                 |
  |------|---------------------------------------------|
  | 200  | Protection applied successfully.            |
  | 400  | Invalid request data.                       |
  | 401  | Authentication failed.                     |
  | 500  | Unexpected server error.                    |

- **["Batch Split"](https://docs.aspose.cloud/cells/batch/split "Batch Split")**  
  *Divide large Excel workbooks into smaller files based on worksheets or row ranges.*  

  **API Details**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parameters**  

  | Name        | Type   | Description                                      |
  |-------------|--------|--------------------------------------------------|
  | files       | array  | Files to be split.                               |
  | splitBy     | string | Criteria: "worksheet" or "rowRange".             |
  | criteria    | object | Details for the chosen split method.            |
  | storage     | string | (Optional) Cloud storage name.                   |

  **Responses**  

  | Code | Description                                 |
  |------|---------------------------------------------|
  | 200  | Split operation completed; returns parts.   |
  | 400  | Incorrect split parameters.                 |
  | 401  | Unauthorized request.                       |
  | 500  | Processing error.                           |

- **["Batch Unlock"](https://docs.aspose.cloud/cells/batch/unlock "Batch Unlock")**  
  *Remove password protection from multiple Excel files in one call.*  

  **API Details**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parameters**  

  | Name     | Type   | Description                              |
  |----------|--------|------------------------------------------|
  | files    | array  | List of locked file identifiers or URLs. |
  | password | string | Current password of the files.           |
  | storage  | string | (Optional) Cloud storage name.           |

  **Responses**  

  | Code | Description                                 |
  |------|---------------------------------------------|
  | 200  | Files unlocked successfully.                |
  | 400  | Wrong password or missing files.            |
  | 401  | Unauthorized access.                        |
  | 500  | Server side failure.                        |