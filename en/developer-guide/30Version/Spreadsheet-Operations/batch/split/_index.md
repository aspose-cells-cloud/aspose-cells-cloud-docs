---
title: "Batch Split"
second_title: "Document"
type: docs
url: /batch/split
keywords: "Batch Split, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, Spreadsheet, Cloud SDK"
description: "Documentation for the Aspose.Cells Cloud Batch Split API, which splits spreadsheet files into multiple formats such as PDF, CSV, or JSON. Includes request details, example cURL commands, and SDK usage across various programming languages."
weight: 100
---

This REST API performs a **batch split** of eligible files.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

The request parameters are:

| Parameter Name   | Type               | Path/Query/String/HTTPBody | Description                                   |
|------------------|--------------------|----------------------------|-----------------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | body                       | Request payload containing split options.     |

### **BatchSplitRequest** Properties

| Name          | Type                | Description                                 | Notes      |
|---------------|---------------------|---------------------------------------------|------------|
| SourceFolder  | string              | Folder that contains the source file.       | [optional] |
| SourceStorage | string              | Storage name where the source file resides. | [optional] |
| MatchCondition| MatchConditionRequest| Conditions used to select files for splitting.| [optional] |
| Format        | string              | Desired output format (e.g., pdf, csv).    | [optional] |
| FromIndex     | integer             | Starting index of the pages to split.       | [optional] |
| ToIndex       | integer             | Ending index of the pages to split.         | [optional] |
| OutFolder     | string              | Destination folder for the split files.     | [optional] |
| SaveOptions   | SaveOptions         | Additional options for saving the output.   | [optional] |

### **MatchConditionRequest** Properties

| Name                | Type      | Description                                 | Notes      |
|---------------------|-----------|---------------------------------------------|------------|
| RegexPattern        | string    | Regular expression to match file names.     | [optional] |
| FullMatchConditions| string[]  | List of exact match conditions.             | [optional] |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your split tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}