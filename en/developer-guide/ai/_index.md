---
title: "Aspose.Cells Cloud AI – Task Decomposition, Spreadsheet & Text Translation"
second_title: "Improve Your AI Skills: Learn Excel Translation, Task Breakdown, and More"
ArticleTitle: "Aspose.Cells Cloud AI – Task Decomposition, Spreadsheet & Text Translation"
linktitle: "AI"
type: docs
url: /ai/
date: 2024-05-22T08:00:00Z
keywords: "Aspose.Cells, Cloud AI, Excel translation, task decomposition, REST API, AI translation Excel, task breakdown API"
description: "Aspose.Cells Cloud AI enables programmatic Excel task decomposition, spreadsheet translation, and text file translation via REST APIs. Includes code samples, request/response specs, and best practices for developers."
weight: 20
---

Aspose.Cells Cloud AI provides three powerful AI‑driven services that simplify working with Excel and text data: **Decompose User Task**, Translate Spreadsheet, and Translate Text File. These APIs enable developers to programmatically break down complex user objectives into actionable steps, translate entire workbooks or plain‑text files, and integrate the results into custom applications. Use the endpoints below to get started quickly, and refer to the detailed request/response specifications provided for each service.

- **[Decompose User Task](https://docs.aspose.cloud/cells/decompose-user-task/)** – Convert user objectives into sequential action plans with Aspose.Cells Cloud AI.
  - **POST Request to Decompose a User Task**
    - **Endpoint URL:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`
    - **Headers:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`
    - **Request Body (JSON):**
      ```json
      {
        "task": "Generate a quarterly sales report with charts and pivot tables"
      }
      ```
    - **Response:** Returns an `.xlsx` file with a worksheet named **TaskList** containing ordered steps.
    - **HTTP Response Codes and Meanings:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`
    - **Prerequisites:** A valid [access token](/cells/getting-started/authentication/) with the **[CellsAI]（https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/）** scope.
    - **Example Response (JSON snippet):**
      ```json
      {
        "fileId": "12345abcde",
        "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
      }
      ```
    - **Notes:** Rate limit: 100 requests per minute. See the [rate limits documentation](/cells/rate-limits/) for more details.

- **[Translate Spreadsheet](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Translate an entire spreadsheet using Aspose.Cells Cloud AI.
  - **POST Request to Translate a Spreadsheet**
    - **Endpoint URL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`
    - **Headers:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`
    - **Request Parameters:**
      - `file` – The Excel file to translate (binary).
      - `targetLanguage` – ISO language code (e.g., `fr`, `de`).
    - **Response:** Returns an `.xlsx` file with all cell values, comments, and sheet names translated.
    - **HTTP Response Codes and Meanings:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`
    - **Prerequisites:** Access token with **[CellsAI]（https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/）** scope and sufficient storage quota.
    - **Example Response (JSON snippet):**
      ```json
      {
        "translatedFileId": "f9d8c7b6",
        "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
      }
      ```
    - **Notes:** Rate limit: 100 requests per minute.

- **[Translate Text File](https://docs.aspose.cloud/cells/translate-text-file/)** – Translate an entire text file using Aspose.Cells Cloud AI.
  - **POST Request to Translate a Text File**
    - **Endpoint URL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text-file`
    - **Headers:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`
    - **Request Parameters:**
      - `file` – The text file to translate (binary).
      - `targetLanguage` – ISO language code (e.g., `es`, `ja`).
    - **Response:** Returns a `.txt` file (UTF-8 encoded).
    - **HTTP Response Codes and Meanings:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`
    - **Prerequisites:** Valid access token with **[CellsAI]（https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/）** scope.
    - **Example Response (JSON snippet):**
      ```json
      {
        "translatedFileId": "a1b2c3d4",
        "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
      }
      ```
    - **Notes:** Supports UTF‑8 encoded plain‑text files up to 5 MB. Rate limit: 100 requests per minute.

<!-- TODO: Add alt text to images: [Description of AI task decomposition flow: User Input → API Call → Generated Excel Workbook with TaskList worksheet] -->
