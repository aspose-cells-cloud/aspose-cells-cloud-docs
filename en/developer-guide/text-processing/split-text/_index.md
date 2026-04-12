---
title: "Split Text API – Segment Excel Cells into Columns | Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Excel Text Splitter – Segment Cell Content into Multiple Columns | Aspose.Cells Cloud"
linktitle: "Split Text"
type: docs
url: /split-text/
keywords: "Aspose Cells split text API, Excel text segmentation, split cell content, delimiter split, cloud API"
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

### Web API

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
# Required header: Authorization: Bearer {access_token}
```

### The request parameters of **splitText** API are

| Parameter Name                 | Type    | Location | Required? | Default        | Description                                                                                                                                         |
| ------------------------------ | ------- | -------- | --------- | -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | File    | FormData | Yes       | —              | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc.                                                           |
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

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI or malformed parameters.
- **401 Unauthorized** – Missing or invalid access token (or client‑id/secret).
- **404 Not Found** – The specified spreadsheet file could not be accessed.
- **500 Server Error** – The spreadsheet encountered an internal processing anomaly.

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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/SplitText) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

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
