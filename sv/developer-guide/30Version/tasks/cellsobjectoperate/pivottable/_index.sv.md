---
title: "Arbeta med pivot-tabeller med hjälp av CellsObjectOperate-uppgiften"
type: docs
url: /sv/tasks/cells-object-operate/pivottable/
aliases: [/sv/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "Aspose Cells pivot-tabell-API, CellsObjectOperate, Excel REST API"
description: "Lär dig hur du skapar en pivot-tabell i Excel med Aspose.Cells Clouds CellsObjectOperate-uppgift. Innehåller cURL-exempel, parameterguide och SDK-referenser."
weight: 10
---

Denna REST API **skapar** en pivot-tabell med hjälp av **CellsObjectOperate**-uppgiften.

**PivotTableOperateParameter**

| Parameter namn      | Typ           | Beskrivning                                                                 |
|---------------------|---------------|-----------------------------------------------------------------------------|
| DestCellName        | string        | Övre vänstra cellen i pivot-tabellen (t.ex. `C1`).                          |
| SourceData          | string        | Omfång som innehåller källdata (t.ex. `Sheet2!A1:E8`).                     |
| TableName           | string        | Namn som tilldelas den nya pivot-tabellen.                                  |
| UseSameSource       | string        | `true` / `false` – om pivot-tabellen använder samma källarark.             |
| PivotTableIndex     | integer       | Index för pivot-tabellen när flera tabeller finns i kalkylbladet.          |
| PivotFieldRows      | integer[]     | Nollbaserade index för fält som ska placeras i radområdet.                  |
| PivotFieldColumns   | integer[]     | Nollbaserade index för fält som ska placeras i kolumnområdet.               |
| PivotFieldData      | integer[]     | Nollbaserade index för fält som ska aggregeras som data.                    |

## REST API

| **API**               | **Typ** | **Beskrivning** | **Resurslänk** |
|-----------------------|---------|-----------------|----------------|
| /cells/task/runtask   | POST    | Kör uppgift     | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

### Förutsättningar
Innan du anropar API:et måste du:

1. Registrera dig för ett Aspose.Cloud-konto och skapa ett program för att få ett **client ID** och **client secret**.  
2. Be om en **JWT-token** från `/connect/token`-slutpunkten med hjälp av klientuppgifterna.  
3. Inkludera token i `Authorization: Bearer <jwt token>`-huvudet för varje begäran.  

Du kan nu använda kommandoradsverktyget **cURL** för att komma åt Aspose.Cells-webbtjänster.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# cURL-exempel – importera data (steg 1)
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
            <!-- Exempelrader – endast några visas för kortfattadhet -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Sport</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Year</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Quarter</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Sales</value></CellValue>
            <!-- …ytterligare rader utelämnade för tydlighet… -->
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
Möjliga HTTP-statuskoder:
- **200 OK** – Pivot-tabellen skapades framgångsrikt. Svarsbrödet innehåller ett `TaskId` som kan användas för att fråga efter åtgärdens status.
- **400 Bad Request** – Ogiltig XML-payload eller saknade obligatoriska parametrar.
- **401 Unauthorized** – JWT-token saknas eller är ogiltig.
- **500 Internal Server Error** – Oväntat serverfel.

Exempel på lyckat svar (XML):

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

## Molnsdk-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:n:
---