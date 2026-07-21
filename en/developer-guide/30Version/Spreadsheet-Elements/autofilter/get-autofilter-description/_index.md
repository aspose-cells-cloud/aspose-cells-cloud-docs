---
title: "Get an AutoFilter in an Excel worksheet"
second_title: "Document"
linktitle: "Get AutoFilter"
type: docs
url: /autofilter/get/
aliases: [/get-autofilter-description/]
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Retrieve the AutoFilter description from an Excel worksheet using the Aspose.Cells Cloud REST API. The endpoint is compatible with SDKs for C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, and more."
weight: 50
---

## REST API

This REST API retrieves the **AutoFilter** description from an Excel worksheet.

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```
### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type   | Path/Query | Description |
|----------------|--------|------------|-------------|
| name           | string | path       | Excel file name (including extension). |
| sheetName      | string | path       | Worksheet name. |
| folder         | string | query      | Folder path in storage where the file is located. |
| storageName    | string | query      | Name of the storage to use. |


### **Response**

```json
{
    "Status":"OK",
    "Code":200,
    AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          }
        },
        "CustomFilters": [
          {
            "FilterOperatorType": "string"
          }
        ],
        "DynamicFilter": {
          "DynamicFilterType": "string"
        },
        "IconFilter": {
          "IconId": 0,
          "IconSetType": "string"
        },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 0,
          "SortOrder": "string",
          "CustomList": "string"
        }
      ],
      "SortLeftToRight": true
    }
  }
}
```

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |


## How to Use the GetWorksheetAutoFilter API with SDKs

### GetWorksheetAutoFilter API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "string",
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          }
        },
        "CustomFilters": [
          {
            "FilterOperatorType": "string"
          }
        ],
        "DynamicFilter": {
          "DynamicFilterType": "string"
        },
        "IconFilter": {
          "IconId": 0,
          "IconSetType": "string"
        },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 0,
          "SortOrder": "string",
          "CustomList": "string"
        }
      ],
      "SortLeftToRight": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetAutoFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetAutoFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetAutoFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetAutoFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetAutoFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetAutoFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetAutoFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetAutoFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}