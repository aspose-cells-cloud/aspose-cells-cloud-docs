---
title: "Support Request File in Task API"
second_title: "Document"
type: docs
url: /tasks/support-request-file/
aliases: [/support-request-file-in-task-api/]
keywords: "Aspose.Cells, REST API, Excel, Cloud"
description: "Aspose.Cells Cloud API enables task-based processing of request files for Excel workbooks."
weight: 10
ArticleTitle: "Support Request File in Aspose.Cells Task API"
---

## REST API

| **API** | **Type** | **Description** | **Resource Link** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Run Task | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

**Request Parameters**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| TaskDescription | object | Yes | Container for a single task definition. |
| TaskType | string | Yes | Type of task, e.g., `ImportData` or `SaveResult`. |
| Workbook.FileSourceType | string | Yes | Source of the workbook file (`CloudFileSystem`, `InMemoryFiles`). |
| Workbook.FilePath | string | Yes | Path to the workbook file in the selected source. |
| ImportBatchDataOption.DestinationWorksheet | string | Yes | Target worksheet name for imported data. |
| ImportBatchDataOption.IsInsert | boolean | Yes | Whether to insert rows (`true`) or overwrite (`false`). |
| ImportBatchDataOption.Source.FileSourceType | string | Yes | Source of the request file (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | string | Yes | Path to the request file containing batch data. |
| SaveResultTaskParameter.ResultSource | string | Yes | Source of the result file (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | Yes | Destination type for the result (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | string | Yes | Input workbook file name. |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | Yes | Desired output file name. |

**Response**

| Field | Type | Description |
|-------|------|-------------|
| Code | integer | HTTP status code (e.g., 200 for success). |
| Status | string | Operation status (`OK` or error message). |
| Result | object | Details of the task execution, including any generated files. |

You can use **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -H "x-aspose-client: Containerize.Swagger" \
  -d '{
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet1",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml.txt"
              }
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet2",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml_2.txt"
              }
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
              "DestinationType": "CloudFileSystem",
              "InputFile": "TaskBook.xlsx",
              "OutputFile": "ImpDataBook.xlsx"
            }
          }
        }
      }
    ]
  }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "GeneratedFiles": [
      {
        "FilePath": "ImpDataBook.xlsx",
        "FileUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

For more information on related tasks, see the [ImportData task](/cells/tasks/importdata/) and the [SaveResult task](/cells/tasks/save-result/) pages.

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}