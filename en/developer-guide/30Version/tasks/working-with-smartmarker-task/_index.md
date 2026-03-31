---
title: "Working with SmartMarker Task in Aspose.Cells Cloud API"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "SmartMarker task, Aspose.Cells Cloud, REST API, Excel, spreadsheet automation"
description: "Learn how to use the SmartMarker task of Aspose.Cells Cloud API with cURL and SDK examples, including request schema and error handling."
weight: 60
---

## REST API

**SmartMarker** is a feature of the Aspose.Cells Cloud API that merges data from XML or JSON sources into placeholders within an Excel template, producing a fully populated workbook. It is typically used for report generation, mail‑merge, and data‑driven spreadsheet creation.

**Prerequisites**

- Aspose.Cells Cloud API version 3.0 or later.  
- A valid OAuth2/JWT access token (passed in the `Authorization: Bearer <token>` header).  
- Source files (template workbook and data file) uploaded to the Aspose Cloud storage or accessible via a supported file‑system type.  
- HTTPS endpoint (all requests must use TLS).

| **API** | **Type** | **Description** | **Resource Link** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Run Task | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to run a SmartMarker task and subsequently save the result workbook.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <your_access_token>" \
     -d '{
  "TaskData": {
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "SmartMarker",
          "SmartMarkerTaskParameter": {
            "SourceWorkbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "Designer.xlsx"
            },
            "DestinationWorkbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "Temp.xlsx"
            },
            "xmlFile": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "DataSet.xml"
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "SaveResult",
          "SaveResultTaskParameter": {
            "ResultSource": "InMemoryFiles",
            "ResultDestination": {
              "DestinationType": "OutputStream",
              "InputFile": "Temp.xlsx",
              "OutputFile": "Output.xlsx"
            }
          }
        }
      }
    ]
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HttpResponseMessage with the operation result.
```

{{< /tab >}}

{{< /tabs >}}

### Request schema (excerpt)

| Element | Type | Required | Description |
| ------- | ---- | -------- | ----------- |
| `TaskData` | object | Yes | Root element that contains one or more `TaskDescription` objects. |
| `Tasks` | array of objects | Yes | Collection of tasks to be executed in order. |
| `TaskDescription.TaskType` | string | Yes | The type of task (`SmartMarker`, `SaveResult`, etc.). |
| `SmartMarkerTaskParameter.SourceWorkbook` | object | Yes | Specifies the template workbook location. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | object | Yes | Specifies where the intermediate workbook is stored. |
| `SmartMarkerTaskParameter.xmlFile` | object | Yes | Data source (XML/JSON) used by SmartMarker. |
| `SaveResultTaskParameter.ResultDestination` | object | Yes | Defines how the final workbook is returned (e.g., `OutputStream`). |

### Error handling

The API may return the following HTTP status codes:

- **400 Bad Request** – malformed request payload or missing required fields.  
- **401 Unauthorized** – invalid or missing authentication token.  
- **404 Not Found** – one of the specified source files cannot be located.  
- **500 Internal Server Error** – an unexpected server‑side error occurred.

Check the response body for an `Error` object that includes a `Code` and a descriptive `Message`.

Using an SDK is the best way to speed up the development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="1" tabID="4" tabName1="C#" >}}

{{< tab tabNum="1" >}}
```csharp
var xml = @"<TaskData>
    <Tasks>
        <TaskDescription>
            <TaskType>SmartMarker</TaskType>
            <SmartMarkerTaskParameter>
                <SourceWorkbook>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>Designer.xlsx</FilePath>
                </SourceWorkbook>
                <DestinationWorkbook>
                    <FileSourceType>InMemoryFiles</FileSourceType>
                    <FilePath>Temp.xlsx</FilePath>
                </DestinationWorkbook>
                <xmlFile>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>DataSet.xml</FilePath>
                </xmlFile>
            </SmartMarkerTaskParameter>
        </TaskDescription>
        <TaskDescription>
            <TaskType>SaveResult</TaskType>
            <SaveResultTaskParameter>
                <ResultSource>InMemoryFiles</ResultSource>
                <ResultDestination>
                    <DestinationType>OutputStream</DestinationType>
                    <InputFile>Temp.xlsx</InputFile>
                    <OutputFile>Output.xlsx</OutputFile>
                </ResultDestination>
            </SaveResultTaskParameter>
        </TaskDescription>
    </Tasks>
</TaskData>";

ServiceHelper helper = new ServiceHelper(sid, key);
using (HttpWebResponse response = helper.CallPost(
       "https://api.aspose.cloud/v3.0/cells/task/runtask",
       xml,
       "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("OK");
        using (Stream st = response.GetResponseStream())
        using (FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate))
        {
            st.CopyTo(fs);
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}