---
title: "Aspose.Cells Cloud Web API - Split text"
second_title: " Aspose.Cells Cloud – Online, Short-Code,"
linktitle: "Split Text"
type: docs
url: /split-text/
keywords: "Split Text"
description: "Indicates performing text segmentation on the specified area according to the segmentation method, and outputting to the designated interval. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

Indicates performing text segmentation on the specified area according to the segmentation method, and outputting to the designated interval.

## **Introduction**: Split Text

The Text Segmentation API divides cell contents into multiple cells based on specified delimiters, patterns, or line breaks, and outputs the results to a target range. It supports flexible splitting methods, directional output (columns or rows), and options to preserve delimiters—ideal for parsing concatenated data, CSV-style content, or multiline text into structured formats.

- **Split cell by specific character**: Break down cell content into multiple cells by selecting any character as the delimiter, including a comma, space, semicolon, and more.
- **Split cells by string**: Separate cells by any combination of characters that you specify.
- **Split text by mask**: Use wildcards to split text based on a particular pattern, offering an even more flexible and powerful method for text division.
- **Divide cell contents by line break**: Divide cell contents based on line breaks, creating a more organized presentation in your spreadsheet.
- **Divide cells into columns or rows**: You have the flexibility to decide whether to split cells into rows or columns, choosing the most suitable format for your sheet.
- **Remove or keep delimiters**: Tailor your results by deciding whether to remove the delimiters or retain them at the beginning or end of the resulting cells.

## **SplitText API**

```http
PUT http://api.aspose.cloud/v4.0/cells/content/split/text
```

### The request parameters of **splitText** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|delimiters|String|Query|Indicates split delimiters.|
|keepDelimitersInResultingCells|Boolean|Query|Indicates keep delimiters in resulting cells.|
|keepDelimitersPosition|String|Query|Indicates keep delimiters position.|
|HowToSplit|String|Query|Indicates|
|outPositionRange|String|Query|Indicates output position range.|
|worksheet|String|Query|Specify the worksheet of spreadsheet.|
|range|String|Query|Specify the worksheet range of spreadsheet.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|

### **Response**

```json
{
File
}
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Split Text API?

### **CSV & Text File Import Cleanup**

When importing data from external systems, fields are often concatenated into single cells:

- **ERP/CRM Data Imports**: Split `"John Doe;johndoe@email.com;555-1234"` into separate name/email/phone columns
- **Database Exports**: Parse combined keys like `"ORD-2024-001|Premium|Express"` into order ID, tier, and shipping method
- **Log File Analysis**: Break down semi-structured logs: `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` for filtering

### **Legacy System Migration**

- Old systems dump multi-value fields into single cells; split them to match new database schemas
- Convert flat-file exports into normalized Excel tables ready for Power BI or Tableau

### **Data Cleaning & Standardization**

- **Standardizing Inconsistent Entry - Delimiter Normalization**: Convert mixed delimiters (`"A,B;C|D"`) to uniform format using multiple delimiter split
- **Standardizing Inconsistent Entry - Whitespace Cleanup**: Split by spaces to identify and remove extra spaces between words
- **Compound Field Separation - Financial Data**: Split combined transaction codes: `"DEP-CHK-3847"` into transaction type, source, and reference
- **Compound Field Separation - Medical Records**: Parse patient data: `"Smith,Jane_F_1985"` into last name, first name, gender, birth year

## Why should you use the Split Text API?

### **Powerful Splitting Options**

- **Specific Characters**: Split by any single character (comma, semicolon, tab, space)
- **String Combinations**: Use multi-character delimiters like `||`, `->`, or custom separators
- **Line Breaks**: Instantly parse multiline cells into separate rows (addresses, comments, descriptions)
- **Custom Delimiters**: Define any character combination as a delimiter for proprietary data formats

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/SplitText) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Split text for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
