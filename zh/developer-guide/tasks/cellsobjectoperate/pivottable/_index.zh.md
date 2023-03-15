---
title: 使用 CellsObjectOperate tas 处理数据透视表
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: REST API, pivot table, spreadsheets, exce
description: Cells.Cloud API for Excel 操作：使用 CellsObjectOperate 任务创建数据透视表
weight: 10
---
此 REST API 使用单元格对象操作 `task` 创建 `pivot table`。

**数据透视表操作参数**


|参数名称|类型|描述|
|:- |:- |:- |
|目的地小区名称|细绳||
|源数据|细绳||
|表名|细绳||
|使用相同的来源|细绳|真假|
|数据透视表索引|整数||
|数据透视字段行|整数[]||
|数据透视字段列|整数[]||
|数据透视表|整数[]||


## 休息 API

|**API**|**类型**|**描述**|**资源链接**|
|:- |:- |:- |:- |
|/细胞/任务/运行任务|邮政|运行任务|[后运行任务](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**用于轻松访问 Aspose.Cells Web 服务的命令行工具。以下示例显示如何使用 cURL 调用 Cloud API。


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# cURL example to create pivot table using cells object operate task
curl -v  "https://api.aspose.cloud/v3.0/cells/task/runtask" \
-X POST \
-H "accept: application/xml" \
-H "Content-Type: application/xml" \
-H "Authorization: Bearer <jwt token>" \ 
-d "{
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
        <CellValue>
          <rowIndex>0</rowIndex>
          <columnIndex>0</columnIndex>
          <type>String</type>
          <value>Sport</value>
        </CellValue>
        <CellValue>
          <rowIndex>0</rowIndex>
          <columnIndex>1</columnIndex>
          <type>String</type>
          <value>Year</value>
        </CellValue>
        <CellValue>
          <rowIndex>0</rowIndex>
          <columnIndex>2</columnIndex>
          <type>String</type>
          <value>Quarter</value>
        </CellValue>
        <CellValue>
          <rowIndex>0</rowIndex>
          <columnIndex>3</columnIndex>
          <type>String</type>
          <value>Sales</value>
        </CellValue>
        <CellValue>
          <rowIndex>0</rowIndex>
          <columnIndex>4</columnIndex>
          <type>String</type>
          <value>YearSales</value>
        </CellValue>
        <CellValue>
          <rowIndex>1</rowIndex>
          <columnIndex>0</columnIndex>
          <type>String</type>
          <value>Golf</value>
        </CellValue>
        <CellValue>
          <rowIndex>2</rowIndex>
          <columnIndex>0</columnIndex>
          <type>String</type>
          <value>Golf</value>
        </CellValue>
        <CellValue>
          <rowIndex>3</rowIndex>
          <columnIndex>0</columnIndex>
          <type>String</type>
          <value>Tennis</value>
        </CellValue>
        <CellValue>
          <rowIndex>4</rowIndex>
          <columnIndex>0</columnIndex>
          <type>String</type>
          <value>Tennis</value>
        </CellValue>
        <CellValue>
          <rowIndex>5</rowIndex>
          <columnIndex>0</columnIndex>
          <type>String</type>
          <value>Tennis</value>
        </CellValue>
        <CellValue>
          <rowIndex>6</rowIndex>
          <columnIndex>0</columnIndex>
          <type>String</type>
          <value>Tennis</value>
        </CellValue>
        <CellValue>
          <rowIndex>7</rowIndex>
          <columnIndex>0</columnIndex>
          <type>String</type>
          <value>Golf</value>
        </CellValue>
        <CellValue>
          <rowIndex>1</rowIndex>
          <columnIndex>1</columnIndex>
          <type>int</type>
          <value>2014</value>
        </CellValue>
        <CellValue>
          <rowIndex>2</rowIndex>
          <columnIndex>1</columnIndex>
          <type>int</type>
          <value>2014</value>
        </CellValue>
        <CellValue>
          <rowIndex>3</rowIndex>
          <columnIndex>1</columnIndex>
          <type>int</type>
          <value>2014</value>
        </CellValue>
        <CellValue>
          <rowIndex>4</rowIndex>
          <columnIndex>1</columnIndex>
          <type>int</type>
          <value>2013</value>
        </CellValue>
        <CellValue>
          <rowIndex>5</rowIndex>
          <columnIndex>1</columnIndex>
          <type>int</type>
          <value>2013</value>
        </CellValue>
        <CellValue>
          <rowIndex>6</rowIndex>
          <columnIndex>1</columnIndex>
          <type>int</type>
          <value>2013</value>
        </CellValue>
        <CellValue>
          <rowIndex>7</rowIndex>
          <columnIndex>1</columnIndex>
          <type>int</type>
          <value>2013</value>
        </CellValue>
        <CellValue>
          <rowIndex>1</rowIndex>
          <columnIndex>2</columnIndex>
          <type>String</type>
          <value>Qtr3</value>
        </CellValue>
        <CellValue>
          <rowIndex>2</rowIndex>
          <columnIndex>2</columnIndex>
          <type>String</type>
          <value>Qtr4</value>
        </CellValue>
        <CellValue>
          <rowIndex>3</rowIndex>
          <columnIndex>2</columnIndex>
          <type>String</type>
          <value>Qtr3</value>
        </CellValue>
        <CellValue>
          <rowIndex>4</rowIndex>
          <columnIndex>2</columnIndex>
          <type>String</type>
          <value>Qtr4</value>
        </CellValue>
        <CellValue>
          <rowIndex>5</rowIndex>
          <columnIndex>2</columnIndex>
          <type>String</type>
          <value>Qtr3</value>
        </CellValue>
        <CellValue>
          <rowIndex>6</rowIndex>
          <columnIndex>2</columnIndex>
          <type>String</type>
          <value>Qtr4</value>
        </CellValue>
        <CellValue>
          <rowIndex>7</rowIndex>
          <columnIndex>2</columnIndex>
          <type>String</type>
          <value>Qtr3</value>
        </CellValue>
        <CellValue>
          <rowIndex>1</rowIndex>
          <columnIndex>3</columnIndex>
          <type>int</type>
          <value>1500</value>
        </CellValue>
        <CellValue>
          <rowIndex>2</rowIndex>
          <columnIndex>3</columnIndex>
          <type>int</type>
          <value>2000</value>
        </CellValue>
        <CellValue>
          <rowIndex>3</rowIndex>
          <columnIndex>3</columnIndex>
          <type>int</type>
          <value>600</value>
        </CellValue>
        <CellValue>
          <rowIndex>4</rowIndex>
          <columnIndex>3</columnIndex>
          <type>int</type>
          <value>1500</value>
        </CellValue>
        <CellValue>
          <rowIndex>5</rowIndex>
          <columnIndex>3</columnIndex>
          <type>int</type>
          <value>4070</value>
        </CellValue>
        <CellValue>
          <rowIndex>6</rowIndex>
          <columnIndex>3</columnIndex>
          <type>int</type>
          <value>5000</value>
        </CellValue>
        <CellValue>
          <rowIndex>7</rowIndex>
          <columnIndex>3</columnIndex>
          <type>int</type>
          <value>6430</value>
        </CellValue>
        <CellValue>
          <rowIndex>1</rowIndex>
          <columnIndex>4</columnIndex>
          <type>int</type>
          <value>15000</value>
        </CellValue>
        <CellValue>
          <rowIndex>2</rowIndex>
          <columnIndex>4</columnIndex>
          <type>int</type>
          <value>20000</value>
        </CellValue>
        <CellValue>
          <rowIndex>3</rowIndex>
          <columnIndex>4</columnIndex>
          <type>int</type>
          <value>600</value>
        </CellValue>
        <CellValue>
          <rowIndex>4</rowIndex>
          <columnIndex>4</columnIndex>
          <type>int</type>
          <value>1500</value>
        </CellValue>
        <CellValue>
          <rowIndex>5</rowIndex>
          <columnIndex>4</columnIndex>
          <type>int</type>
          <value>4070</value>
        </CellValue>
        <CellValue>
          <rowIndex>6</rowIndex>
          <columnIndex>4</columnIndex>
          <type>int</type>
          <value>5000</value>
        </CellValue>
        <CellValue>
          <rowIndex>7</rowIndex>
          <columnIndex>4</columnIndex>
          <type>int</type>
          <value>6430</value>
        </CellValue>
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
        <PivotFieldRows>
          <int>0</int>
          <int>1</int>
        </PivotFieldRows>
        <PivotFieldColumns>
          <int>2</int>
        </PivotFieldColumns>
        <PivotFieldData>
          <int>3</int>
          <int>4</int>
        </PivotFieldData>
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
        <OutputFile>Output\ReportS004.xlsx</OutputFile>
      </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>
}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 系列

使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：

