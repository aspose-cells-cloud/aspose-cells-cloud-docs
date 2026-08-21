---
title: "Arbeiten mit Pivot-Tabellen mithilfe der CellsObjectOperate-Aufgabe"
type: docs
url: /tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "Aspose Cells Pivot-Tabellen-API, CellsObjectOperate, Excel REST API"
description: "Erfahren Sie, wie Sie mit der CellsObjectOperate-Aufgabe von Aspose.Cells Cloud eine Pivot-Tabelle in Excel generieren. Enthält ein cURL-Beispiel, einen Parameterleitfaden und SDK-Verweise."
weight: 10
---

Diese REST API **erstellt** eine Pivot-Tabelle mithilfe der **CellsObjectOperate**-Aufgabe.

**PivotTableOperateParameter**

| Parametername       | Typ           | Beschreibung                                                                 |
|---------------------|---------------|------------------------------------------------------------------------------|
| DestCellName        | string        | Obere linke Zelle der Pivot-Tabelle (z. B. `C1`).                            |
| SourceData          | string        | Bereich, der die Quelldaten enthält (z. B. `Sheet2!A1:E8`).                 |
| TableName           | string        | Name, der der neuen Pivot-Tabelle zugewiesen wird.                           |
| UseSameSource       | string        | `true` / `false` – gibt an, ob die Pivot-Tabelle dieselbe Quelldatei verwendet. |
| PivotTableIndex     | integer       | Index der Pivot-Tabelle, wenn mehrere Tabellen im Arbeitsblatt vorhanden sind. |
| PivotFieldRows      | integer[]     | Nullbasierte Indizes der Felder, die im Zeilenbereich platziert werden.     |
| PivotFieldColumns   | integer[]     | Nullbasierte Indizes der Felder, die im Spaltenbereich platziert werden.    |
| PivotFieldData      | integer[]     | Nullbasierte Indizes der Felder, die als Daten aggregiert werden sollen.    |

## REST API

| **API**               | **Typ** | **Beschreibung** | **Ressourcenlink** |
|-----------------------|---------|------------------|--------------------|
| /cells/task/runtask   | POST    | Aufgabe ausführen  | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Voraussetzungen
Bevor Sie die API aufrufen, müssen Sie Folgendes tun:

1. Einen Aspose.Cloud-Account registrieren und eine Anwendung erstellen, um eine **Client-ID** und einen **Client-Geheimnis** zu erhalten.  
2. Ein **JWT-Token** vom `/connect/token`-Endpunkt mithilfe der Clientanmeldedaten anfordern.  
3. Das Token in den Header `Authorization: Bearer <jwt token>` jeder Anfrage einbinden.  

Sie können nun das **cURL**-Befehlszeilentool verwenden, um auf Aspose.Cells-Webdienste zuzugreifen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# cURL-Beispiel – Daten importieren (Schritt 1)
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
            <!-- Beispielzeilen – nur einige zur Kürze aufgeführt -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Sport</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Year</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Quarter</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Sales</value></CellValue>
            <!-- …weitere Zeilen der Kürze halber weggelassen… -->
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
Mögliche HTTP-Statuscodes:
- **200 OK** – Pivot-Tabelle erfolgreich erstellt. Der Antworttext enthält eine `TaskId`, mit der der Vorgangsstatus abgefragt werden kann.
- **400 Bad Request** – Ungültiges XML-Payload oder fehlende erforderliche Parameter.
- **401 Unauthorized** – Fehlendes oder ungültiges JWT-Token.
- **500 Internal Server Error** – Unerwarteter Serverfehler.

Beispiel für eine erfolgreiche Antwort (XML):

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

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene und lässt Sie sich auf Ihre Projekt-Aufgaben konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:
---