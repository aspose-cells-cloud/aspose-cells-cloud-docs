---
title: "在 Aspose.Cells Cloud API 中使用 SmartMarker 任务"
type: docs
url: /zh/tasks/smartmarker/
aliases: [  /zh/working-with-smartmarker-task/ ]
keywords: "SmartMarker 任务, Aspose.Cells Cloud, REST API, Excel, 电子表格自动化"
description: "了解如何使用 Aspose.Cells Cloud API 的 SmartMarker 任务，并提供 cURL 和 SDK 示例，包括请求结构和错误处理。"
weight: 60
ArticleTitle: "在 Aspose.Cells Cloud API 中使用 SmartMarker 任务"
---

## REST API

**SmartMarker** 是 Aspose.Cells Cloud API 的一项功能，可将来自 XML 或 JSON 数据源的数据合并到 Excel 模板中的占位符内，从而生成完整填充的工作簿。它通常用于报表生成、邮件合并和数据驱动的电子表格创建。

**前置条件**

- Aspose.Cells Cloud API 版本为 3.0 或更高版本。  
- 有效的 OAuth2/JWT 访问令牌（通过 `Authorization: Bearer <token>` 请求头传递）。  
- 源文件（模板工作簿和数据文件）已上传至 Aspose Cloud 存储，或可通过受支持的文件系统类型访问。  
- HTTPS 端点（所有请求必须使用 TLS）。

| **API** | **类型** | **说明** | **资源链接** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | 运行任务 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何运行 SmartMarker 任务，并随后保存结果工作簿。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

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

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "FileLink": "https://api.aspose.cloud/v3.0/storage/file/Output.xlsx",
    "FileSize": 254321,
    "FileName": "Output.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 请求结构（节选）

| 元素 | 类型 | 是否必需 | 说明 |
| --- | --- | --- | --- |
| `TaskData` | object | 是 | 根元素，包含一个或多个 `TaskDescription` 对象。 |
| `Tasks` | 对象数组 | 是 | 按顺序执行的任务集合。 |
| `TaskDescription.TaskType` | string | 是 | 任务类型（如 `SmartMarker`、`SaveResult` 等）。 |
| `SmartMarkerTaskParameter.SourceWorkbook` | object | 是 | 指定模板工作簿的位置。 |
| `SmartMarkerTaskParameter.DestinationWorkbook` | object | 是 | 指定中间工作簿的存储位置。 |
| `SmartMarkerTaskParameter.xmlFile` | object | 是 | SmartMarker 使用的数据源（XML/JSON）。 |
| `SaveResultTaskParameter.ResultDestination` | object | 是 | 定义如何返回最终工作簿（例如 `OutputStream`）。 |

### 错误处理

API 可能返回以下 HTTP 状态码：

- **400 Bad Request（错误请求）**：请求体格式错误或缺少必需字段。  
- **401 Unauthorized（未授权）**：访问令牌无效或缺失。  
- **404 Not Found（未找到）**：指定的某个源文件无法找到。  
- **500 Internal Server Error（内部服务器错误）**：发生意外的服务器端错误。

请检查响应体中的 `Error` 对象，该对象包含 `Code`（错误代码）和描述性 `Message`（错误消息）。

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} 了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

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