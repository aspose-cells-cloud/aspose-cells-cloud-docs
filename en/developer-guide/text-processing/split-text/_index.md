---
title: "Split Text API – Segment Excel Cells into Columns | Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Excel Text Splitter – Segment Cell Content into Multiple Columns | Aspose.Cells Cloud"
linktitle: "Split Text"
type: docs
url: /split-text/
keywords: "Aspose, Cells, Split Text API, Excel, delimiter, text segmentation, cloud API"
description: "Easily split Excel cell text into separate columns or rows using Aspose.Cells Cloud. Supports custom delimiters, masks, line‑breaks, and optional delimiter retention. Get started with curl or SDKs in minutes."
weight: 100
---

Segment Excel cell text into multiple columns using custom segmentation rules. Split content by delimiter and output to specified ranges with the Aspose.Cells Cloud text‑splitting Web API.

## **Introduction**: Split Text

The Text Segmentation API divides cell contents into multiple cells based on specified delimiters, patterns, or line breaks, and outputs the results to a target range. It supports flexible splitting methods, directional output (columns or rows), and options to preserve delimiters—ideal for parsing concatenated data, CSV‑style content, or multiline text into structured formats.

- **Split cell by specific character** – break down cell content into multiple cells by selecting any character as the delimiter (comma, space, semicolon, etc.).
- **Split cells by string** – separate cells by any combination of characters that you specify.
- **Split text by mask** – use wildcards to split text based on a particular pattern, offering an even more flexible and powerful method for text division.
- **Divide cell contents by line break** – create a more organized presentation by splitting on line breaks.
- **Divide cells into columns or rows** – choose whether the split results are written to successive columns or rows.
- **Remove or keep delimiters** – decide whether delimiters are removed or retained at the beginning or end of the resulting cells.

## **SplitText API**

**Prerequisites**: To use this API you need a valid Aspose Cloud access token, and the workbook to be processed must be uploaded to Aspose Cloud storage or supplied directly in the request. The API supports common spreadsheet formats such as XLSX, XLS, ODS, and CSV.

### Web API

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### The request parameters of **splitText** API are

| Parameter Name                 | Type    | Location | Required? | Default        | Description                                                                                                                                         |
| ------------------------------ | ------- | -------- | --------- | -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | File    | FormData | Yes       | —              | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc.                                                            |
| delimiters                     | String  | Query    | No        | —              | One or more delimiter characters used to split text within cells (e.g., `","`, `";"`, `Space`, `LineBreak`, `Tab`, `Pipe`, `Custom`).               |
| keepDelimitersInResultingCells | Boolean | Query    | No        | false          | When `true`, the delimiter characters are retained in the resulting split cells.                                                                    |
| keepDelimitersPosition         | String  | Query    | No        | None           | Where to retain delimiters if `keepDelimitersInResultingCells` is `true`. Options: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`. |
| howToSplit                     | String  | Query    | No        | SplitToColumns | Method of text segmentation. Options: `None`, `SplitToColumns`, `SplitToRows`.                                                                      |
| outPositionRange               | String  | Query    | Yes       | —              | Target range where the split results will be written (e.g., `"D1:F10"`).                                                                            |
| worksheet                      | String  | Query    | No        | —              | Name of the worksheet where text splitting will be applied. If omitted, the first worksheet is used.                                                |
| range                          | String  | Query    | No        | —              | Source cell range to which the split operation is applied (e.g., `"A1:A10"`). If omitted, all used cells in the worksheet are processed.            |
| outPath                        | String  | Query    | No        | —              | Cloud storage folder path where the processed workbook will be saved. If omitted, the file is saved in the source folder.                           |
| outStorageName                 | String  | Query    | No        | —              | Name of the cloud storage where the output file will be stored.                                                                                     |
| region                         | String  | Query    | No        | —              | Locale for text segmentation, which may affect delimiter interpretation and character encoding (e.g., `"en-US"`, `"ja-JP"`).                        |
| password                       | String  | Query    | No        | —              | Password for opening a password‑protected spreadsheet.                                                                                              |

### **Response**

A successful request returns **200 OK** with a file stream containing the processed workbook.

```json
{
  "status": 200,
  "description": "File stream of the workbook with split text applied.",
  "content": {
    "type": "application/octet-stream",
    "example": "Base64‑encoded binary data representing the updated workbook."
  }
}
```

The generic schema previously shown is retained for reference:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## Where should we use the Split Text API?

### **CSV & Text File Import Cleanup**

When importing data from external systems, fields are often concatenated into single cells:

- **ERP/CRM Data Imports** – split `"John Doe;johndoe@email.com;555-1234"` into separate name, email, and phone columns.
- **Database Exports** – parse combined keys like `"ORD-2024-001|Premium|Express"` into order ID, tier, and shipping method.
- **Log File Analysis** – break down semi‑structured logs such as `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` for filtering.

### **Legacy System Migration**

- Old systems dump multi‑value fields into single cells; split them to match new database schemas.
- Convert flat‑file exports into normalized Excel tables ready for Power BI or Tableau.

### **Data Cleaning & Standardization**

- **Delimiter Normalization** – convert mixed delimiters (`"A,B;C|D"`) to a uniform format using multiple‑delimiter split.
- **Whitespace Cleanup** – split by spaces to identify and remove extra spaces between words.
- **Financial Data** – split combined transaction codes like `"DEP-CHK-3847"` into transaction type, source, and reference.
- **Medical Records** – parse patient data such as `"Smith,Jane_F_1985"` into last name, first name, gender, and birth year.

## Why should you use the Split Text API?

- **Specific Characters** – split by any single character (comma, semicolon, tab, space).
- **String Combinations** – use multi‑character delimiters like `||`, `->`, or custom separators.
- **Line Breaks** – instantly parse multiline cells into separate rows (addresses, comments, descriptions).
- **Custom Delimiters** – define any character combination as a delimiter for proprietary data formats.
- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom solutions, this significantly reduces development workload.
- **Cost‑Effective** – you can remove duplicate characters without first uploading the workbook, which saves storage space and reduces costs.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement split text for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}