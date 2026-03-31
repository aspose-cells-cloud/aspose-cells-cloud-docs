---
title: "Working with Pivot Tables Using the CellsObjectOperate Task"
type: docs
url: /tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "Aspose Cells pivot table API, CellsObjectOperate, Excel REST API"
description: "Learn how to generate a pivot table in Excel using Aspose.Cells Cloud’s CellsObjectOperate task. Includes cURL example, parameter guide, and SDK references."
weight: 10
---

This REST API **creates** a pivot table using the **CellsObjectOperate** task.

**PivotTableOperateParameter**

| Parameter Name      | Type          | Description                                                                 |
|---------------------|---------------|-----------------------------------------------------------------------------|
| DestCellName        | string        | Top‑left cell of the pivot table (e.g., `C1`).                               |
| SourceData          | string        | Range that contains the source data (e.g., `Sheet2!A1:E8`).                |
| TableName           | string        | Name assigned to the new pivot table.                                       |
| UseSameSource       | string        | `true` / `false` – whether the pivot uses the same source workbook.         |
| PivotTableIndex     | integer       | Index of the pivot table when multiple tables exist in the worksheet.      |
| PivotFieldRows      | integer[]     | Zero‑based indexes of fields to place in the rows area.                     |
| PivotFieldColumns   | integer[]     | Zero‑based indexes of fields to place in the columns area.                  |
| PivotFieldData      | integer[]     | Zero‑based indexes of fields to aggregate as data.                          |

## REST API

| **API**               | **Type** | **Description** | **Resource Link** |
|-----------------------|----------|-----------------|-------------------|
| /cells/task/runtask   | POST     | Run Task        | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Prerequisites
Before invoking the API you must:

1. Register for an Aspose.Cloud account and create an application to obtain a **client ID** and **client secret**.  
2. Request a **JWT token** from the `/connect/token` endpoint using the client credentials.  
3. Include the token in the `Authorization: Bearer <jwt token>` header of every request.  

You can now use the **cURL** command‑line tool to access Aspose.Cells web services.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# cURL example – import data (step 1)
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
            <!-- Sample rows – only a few shown for brevity -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Sport</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Year</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Quarter</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Sales</value></CellValue>
            <!-- …additional rows omitted for clarity… -->
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
Possible HTTP status codes:
- **200 OK** – Pivot table created successfully. The response body contains a `TaskId` that can be used to query the operation status.
- **400 Bad Request** – Invalid XML payload or missing required parameters.
- **401 Unauthorized** – JWT token missing or invalid.
- **500 Internal Server Error** – Unexpected server‑side error.

Example success response (XML):

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

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs: