---
title: "Task API 中的支持请求文件"
second_title: "Document"
type: docs
url: /zh/tasks/support-request-file/
aliases: [  /zh/support-request-file-in-task-api/ ]
keywords: "Aspose.Cells, REST API, Excel, 云服务"
description: "Aspose.Cells Cloud API 支持以任务方式处理 Excel 工作簿的请求文件。"
weight: 10
ArticleTitle: "Aspose.Cells Task API 中的支持请求文件"
---

## REST API

| **API** | **类型** | **说明** | **资源链接** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | 运行任务 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) 定义了一个公开可访问的编程接口，让您能够直接从网页浏览器执行 REST 交互。

**请求参数**

| 参数 | 类型 | 必填 | 描述 |
|-----------|------|----------|-------------|
| TaskDescription | object | 是 | 单个任务定义的容器。 |
| TaskType | string | 是 | 任务类型，例如 `ImportData` 或 `SaveResult`。 |
| Workbook.FileSourceType | string | 是 | 工作簿文件的来源（`CloudFileSystem` 或 `InMemoryFiles`）。 |
| Workbook.FilePath | string | 是 | 所选来源中工作簿文件的路径。 |
| ImportBatchDataOption.DestinationWorksheet | string | 是 | 导入数据的目标工作表名称。 |
| ImportBatchDataOption.IsInsert | boolean | 是 | 是否插入行（`true`）或覆盖（`false`）。 |
| ImportBatchDataOption.Source.FileSourceType | string | 是 | 请求文件的来源（`RequestFiles`）。 |
| ImportBatchDataOption.Source.FilePath | string | 是 | 包含批处理数据的请求文件的路径。 |
| SaveResultTaskParameter.ResultSource | string | 是 | 结果文件的来源（`InMemoryFiles`）。 |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | 是 | 结果的输出目标类型（`CloudFileSystem`）。 |
| SaveResultTaskParameter.ResultDestination.InputFile | string | 是 | 输入工作簿文件名。 |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | 是 | 期望的输出文件名。 |

**响应**

| 字段 | 类型 | 描述 |
|-------|------|-------------|
| Code | integer | HTTP 状态码（例如，200 表示成功）。 |
| Status | string | 操作状态（`OK` 或错误消息）。 |
| Result | object | 任务执行的详细信息，包括生成的任何文件。 |

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

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

有关相关任务的更多信息，请参阅 [ImportData 任务](/zh/cells/tasks/importdata/) 和 [SaveResult 任务](/zh/cells/tasks/save-result/) 页面。

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}