﻿---
title: Arbeta med pivottabell med CellsObjectOperate tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: REST API, pivot table, spreadsheets, exce
description: "Cells.Cloud API för Excel fungera: skapa pivottabell med hjälp av uppgiften CellsObjectOperate"
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Arbeta med pivottabell med uppgiften CellsObjectOperate
---
Detta REST API skapa `pivot table` med hjälp av cells object operation `task`.

**PivotTableOperateParameter**


|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| DestCellName| sträng||
| Källdata| sträng||
| Tabellnamn| sträng||
| UseSameSource| sträng| sant falskt|
| PivotTableIndex| heltal||
| PivotFieldRows|heltal[]||
| Pivotfältkolumner|heltal[]||
| PivotFieldData|heltal[]||


## REST API

|**API**|**Typ**|**Beskrivning**|**Resurslänk**|
|:- |:- |:- |:- |
|/cells/task/runtask|POSTA|Kör uppgift|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL**kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.


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

## Cloud SDK-familj

 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:

