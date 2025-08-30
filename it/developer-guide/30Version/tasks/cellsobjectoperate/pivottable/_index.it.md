---
title: Lavorare con la tabella pivot utilizzando CellsObjectOperate tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: REST API, pivot table, spreadsheets, exce
description: "Cells.Cloud API per Excel opera: crea tabella pivot utilizzando l'attività CellsObjectOperate"
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Utilizzo della tabella pivot tramite l'attività CellsObjectOperate
---
Questo REST API crea `pivot table` utilizzando l'oggetto cells e opera `task`.

**PivotTableOperateParameter**


|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| NomeCellaDest| corda||
| Dati di origine| corda||
| NomeTabella| corda||
| UsaSameSource| corda| vero/falso|
| IndiceTabellaPivot| intero||
| PivotFieldRows|intero[]||
| Colonne di campi pivot|intero[]||
| Dati del campo pivot|intero[]||


## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Link alla risorsa**|
|:- |:- |:- |:- |
|/cells/task/runtask|INVIARE|Esegui attività|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** Strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.


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

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

