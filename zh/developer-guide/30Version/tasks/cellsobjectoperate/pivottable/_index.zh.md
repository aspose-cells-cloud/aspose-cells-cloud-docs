---
title: "使用 CellsObjectOperate 任务处理数据透视表"
type: docs
url: /zh/tasks/cells-object-operate/pivottable/
aliases: [/zh/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "Aspose Cells 数据透视表 API，CellsObjectOperate，Excel REST API"
description: "了解如何使用 Aspose.Cells Cloud 的 CellsObjectOperate 任务在 Excel 中生成数据透视表。包含 cURL 示例、参数说明及 SDK 参考。"
weight: 10
---

本 REST API 通过 **CellsObjectOperate** 任务 **创建** 数据透视表。

**PivotTableOperateParameter（数据透视表操作参数）**

| 参数名                | 类型          | 描述                                                                 |
|-----------------------|---------------|----------------------------------------------------------------------|
| DestCellName          | string        | 数据透视表左上角单元格（例如：`C1`）。                               |
| SourceData            | string        | 包含源数据的区域（例如：`Sheet2!A1:E8`）。                          |
| TableName             | string        | 为新数据透视表指定的名称。                                           |
| UseSameSource         | string        | `true` / `false` —— 指示数据透视表是否使用同一工作簿作为数据源。    |
| PivotTableIndex       | integer       | 当工作表中存在多个数据透视表时，该数据透视表的索引。                 |
| PivotFieldRows        | integer[]     | 要放置在“行”区域的字段的从零开始索引。                               |
| PivotFieldColumns     | integer[]     | 要放置在“列”区域的字段的从零开始索引。                               |
| PivotFieldData        | integer[]     | 要作为数据聚合的字段的从零开始索引。                                 |

## REST API

| **API**               | **类型** | **描述**       | **资源链接** |
|-----------------------|----------|----------------|--------------|
| /cells/task/runtask   | POST     | 运行任务       | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器执行 REST 交互。

### 前置条件
调用 API 前，您必须完成以下步骤：

1. 注册 Aspose.Cloud 账户并创建一个应用程序以获取 **Client ID** 和 **Client Secret**。  
2. 使用客户端凭据从 `/connect/token` 端点请求 **JWT 令牌**。  
3. 在每个请求的 `Authorization: Bearer <jwt token>` 请求头中包含该令牌。  

现在，您可以使用 **cURL** 命令行工具访问 Aspose.Cells Web 服务。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# cURL 示例 —— 导入数据（步骤 1）
curl -v "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -X POST \
  -H "accept: application/xml" \
  -H "Content-Type: application/xml" \
  -H "Authorization: Bearer <jwt token>" \
  -d '
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>Book1.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <BatchData>
            <!-- 示例数据行 —— 为简洁起见仅列出部分 -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>运动项目</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>年份</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>季度</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>销售额</value></CellValue>
            <!-- …为清晰起见省略其余行… -->
          </BatchData>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>CellsObjectOperate</TaskType>
      <CellsObjectOperateTaskParameter>
        <OperateObject>
          <OperateObjectType>ListObject</OperateObjectType>
          <Position>
            <Workbook>
              <FileSourceType>InMemoryFiles</FileSourceType>
              <FilePath>Book1.xlsx</FilePath>
            </Workbook>
            <SheetName>Sheet1</SheetName>
            <ListObjectIndex>0</ListObjectIndex>
          </Position>
        </OperateObject>

        <PivotTableOperateParameter>
          <OperateType>Add</OperateType>
          <SourceData>=Sheet2!A1:E8</SourceData>
          <DestCellName>C1</DestCellName>
          <TableName>TestPivot</TableName>
          <UseSameSource>true</UseSameSource>
          <PivotTableIndex>0</PivotTableIndex>
          <PivotFieldRows><int>0</int><int>1</int></PivotFieldRows>
          <PivotFieldColumns><int>2</int></PivotFieldColumns>
          <PivotFieldData><int>3</int><int>4</int></PivotFieldData>
        </PivotTableOperateParameter>

        <DestinationWorkbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>Book001.xlsx</FilePath>
        </DestinationWorkbook>
      </CellsObjectOperateTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>OutputStream</DestinationType>
          <InputFile>Book001.xlsx</InputFile>
          <OutputFile>Output/ReportS004.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
可能的 HTTP 状态码：
- **200 OK** —— 数据透视表创建成功。响应体包含可用于查询操作状态的 `TaskId`。
- **400 Bad Request** —— XML 负载无效或缺少必要参数。
- **401 Unauthorized** —— 缺少或无效的 JWT 令牌。
- **500 Internal Server Error** —— 服务器端意外错误。

成功响应示例（XML）：

<?xml version="1.0" encoding="UTF-8"?>
<TaskResponse>
  <TaskId>12345</TaskId>
  <Status>Completed</Status>
  <Result>
    <ResultSource>InMemoryFiles</ResultSource>
    <ResultDestination>Output/ReportS004.xlsx</ResultDestination>
  </Result>
</TaskResponse>
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：