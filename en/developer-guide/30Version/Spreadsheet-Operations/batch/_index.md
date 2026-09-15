---
title: "Batch Processing of Excel Files – Convert, Lock, Protect, Split, Unlock with Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Batch Excel files"
date: 2024-06-15
url: /batch/
keywords: "batch processing, Excel API, bulk convert, workbook lock, workbook unlock, Aspose.Cells Cloud"
description: "Use Aspose.Cells Cloud’s batch endpoints to convert, lock, protect, split, and unlock multiple Excel files via a single REST API call. Includes SDKs for 10+ languages."
weight: 35
ArticleTitle: "Batch Processing of Excel Files – Convert, Lock, Protect, Split, Unlock with Aspose.Cells Cloud API"
---

The Aspose.Cells Cloud API provides batch endpoints that allow you to perform common operations on multiple Excel files in a single request. Below is a quick overview of the available batch operations together with concise API specifications for each.

- ## Batch Convert Excel Files

  _Convert multiple Excel files to a chosen output format in one request._

  **API Details**

  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```

  **Parameters**

  | Name         | Type   | Description                                                                      |
  | ------------ | ------ | -------------------------------------------------------------------------------- |
  | files        | array  | List of Excel files to convert (max 20). Each item is a file upload (multipart). |
  | outputFormat | string | Desired output format (e.g., pdf, csv, html).                                    |
  | storage      | string | (Optional) Cloud storage name.                                                   |

  **Responses**

  | Code | Description                              |
  | ---- | ---------------------------------------- |
  | 200  | Conversion successful; returns files.    |
  | 400  | Invalid parameters supplied.             |
  | 401  | Unauthorized – missing or invalid token. |
  | 500  | Internal server error.                   |

- ## Batch Lock Excel Files

  _Apply a password lock to multiple Excel files simultaneously._

  **API Details**

  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```

  **Parameters**

  | Name     | Type   | Description                          |
  | -------- | ------ | ------------------------------------ |
  | files    | array  | List of file identifiers or URLs.    |
  | password | string | Password to lock the workbooks with. |
  | storage  | string | (Optional) Cloud storage name.       |

  **Responses**

  | Code | Description                    |
  | ---- | ------------------------------ |
  | 200  | Files locked successfully.     |
  | 400  | Missing or invalid parameters. |
  | 401  | Unauthorized access.           |
  | 500  | Server error.                  |

- ## Batch Protect Excel Files

  _Add protection settings (e.g., read‑only, structure) to multiple workbooks._

  **API Details**

  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```

  **Parameters**

  | Name       | Type   | Description                                     |
  | ---------- | ------ | ----------------------------------------------- |
  | files      | array  | List of file identifiers or URLs.               |
  | protection | object | Protection options (e.g., readOnly, structure). |
  | storage    | string | (Optional) Cloud storage name.                  |

  **Responses**

  | Code | Description                      |
  | ---- | -------------------------------- |
  | 200  | Protection applied successfully. |
  | 400  | Invalid request data.            |
  | 401  | Authentication failed.           |
  | 500  | Unexpected server error.         |

- ## Batch Split

  _Divide large Excel workbooks into smaller files based on worksheets or row ranges._

  **API Details**

  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```

  **Parameters**

  | Name     | Type   | Description                          |
  | -------- | ------ | ------------------------------------ |
  | files    | array  | Files to be split.                   |
  | splitBy  | string | Criteria: "worksheet" or "rowRange". |
  | criteria | object | Details for the chosen split method. |
  | storage  | string | (Optional) Cloud storage name.       |

  **Responses**

  | Code | Description                               |
  | ---- | ----------------------------------------- |
  | 200  | Split operation completed; returns parts. |
  | 400  | Incorrect split parameters.               |
  | 401  | Unauthorized request.                     |
  | 500  | Processing error.                         |

- ## Batch Unlock

  _Remove password protection from multiple Excel files in one call._

  **API Details**

  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```

  **Parameters**

  | Name     | Type   | Description                              |
  | -------- | ------ | ---------------------------------------- |
  | files    | array  | List of locked file identifiers or URLs. |
  | password | string | Current password of the files.           |
  | storage  | string | (Optional) Cloud storage name.           |

  **Responses**

  | Code | Description                      |
  | ---- | -------------------------------- |
  | 200  | Files unlocked successfully.     |
  | 400  | Wrong password or missing files. |
  | 401  | Unauthorized access.             |
  | 500  | Server side failure.             |

For authentication details, see [Authentication Overview]（https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/）.  
To use batch operations programmatically, try our [Python SDK example](/cells/sdk/python/batch-operations/).

![Batch processing workflow: client sends multipart POST to /cells/batch/convert; server processes files in parallel and returns aggregated response.](/images/batch-workflow.png "Batch conversion workflow")  
_Diagram showing client-side batch request to Aspose.Cells Cloud API, parallel processing of multiple files, and aggregated response._
