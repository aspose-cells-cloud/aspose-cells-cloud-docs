---
title: "Get Chart Title from a Worksheet"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords: ["Aspose.Cells Cloud", "Chart Title", "Excel", "REST API", "Get Chart Title", "cURL", "SDK"]
description: "Learn how to retrieve a chart title from an Excel worksheet using Aspose.Cells Cloud REST API. Includes endpoint, parameters, authentication, sample cURL and SDK code."
---

This REST API retrieves the title of a chart that is stored in a worksheet of an Excel workbook.

**Prerequisites**  
- An Aspose.Cells Cloud account.  
- The appropriate Aspose.Cells Cloud SDK installed for your language (C#, Java, PHP, etc.).  
- A valid OAuth 2.0 access token (Bearer JWT). See the **Authentication** guide for details.

**Authentication**  
All requests must include the header `Authorization: Bearer <your‑jwt‑token>` and `Accept: application/json`. The token is obtained from the OAuth token endpoint described in the authentication documentation.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

The endpoint accepts the following parameters:

| Parameter Name | Type    | Location | Description                                   |
|----------------|---------|----------|-----------------------------------------------|
| name           | string  | path     | Name of the workbook file.                    |
| sheetName      | string  | path     | Name of the worksheet that contains the chart.|
| chartIndex     | integer | path     | Zero‑based index of the chart.                |
| folder         | string  | query    | Folder path where the workbook is stored.     |
| storageName    | string  | query    | Name of the storage service.                  |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "Sales Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Response fields**

| Field               | Description                                          |
|---------------------|------------------------------------------------------|
| `Title.Text`        | The actual text displayed as the chart title.        |
| `Title.Font.Name`   | Font family used for the title (e.g., *Arial*).      |
| `Title.Font.Size`   | Font size in points.                                 |
| `Title.Font.IsBold` | Indicates whether the title text is bold.            |

**How to extract the title in a script (using `jq`)**

```bash
# Assuming the JSON response is saved in response.json
title=$(jq -r '.Title.Text' response.json)
echo "Chart title: $title"
```

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

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

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}