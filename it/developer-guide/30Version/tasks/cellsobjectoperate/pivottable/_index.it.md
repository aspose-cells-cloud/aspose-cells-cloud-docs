---
---
title: "Lavorare con tabelle pivot utilizzando l'attività CellsObjectOperate"
type: docs
url: /it/tasks/cells-object-operate/pivottable/
aliases: [/it/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "API Aspose Cells per tabelle pivot, CellsObjectOperate, API REST per Excel"
description: "Scopri come generare una tabella pivot in Excel utilizzando l'attività CellsObjectOperate di Aspose.Cells Cloud. Include un esempio cURL, una guida ai parametri e riferimenti agli SDK."
weight: 10
---

Questa API REST **crea** una tabella pivot utilizzando l'attività **CellsObjectOperate**.

**PivotTableOperateParameter**

| Nome parametro      | Tipo          | Descrizione                                                                 |
|---------------------|---------------|-----------------------------------------------------------------------------|
| DestCellName        | string        | Cella in alto a sinistra della tabella pivot (es. `C1`).                   |
| SourceData          | string        | Intervallo contenente i dati di origine (es. `Sheet2!A1:E8`).              |
| TableName           | string        | Nome assegnato alla nuova tabella pivot.                                   |
| UseSameSource       | string        | `true` / `false` – indica se la tabella pivot utilizza lo stesso workbook di origine. |
| PivotTableIndex     | integer       | Indice della tabella pivot quando più tabelle sono presenti nel foglio di lavoro. |
| PivotFieldRows      | integer[]     | Indici in base zero dei campi da posizionare nell’area righe.              |
| PivotFieldColumns   | integer[]     | Indici in base zero dei campi da posizionare nell’area colonne.            |
| PivotFieldData      | integer[]     | Indici in base zero dei campi da aggregare come dati.                      |

## API REST

| **API**               | **Tipo** | **Descrizione** | **Link alla risorsa** |
|-----------------------|----------|-----------------|-----------------------|
| /cells/task/runtask   | POST     | Esegui attività   | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definisce un’interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

### Prerequisiti
Prima di chiamare l’API è necessario:

1. Registrarsi su un account Aspose.Cloud e creare un’applicazione per ottenere un **client ID** e un **client secret**.  
2. Richiedere un **token JWT** dall’endpoint `/connect/token` utilizzando le credenziali del client.  
3. Includere il token nell’intestazione `Authorization: Bearer <jwt token>` di ogni richiesta.  

A questo punto puoi utilizzare lo strumento a riga di comando **cURL** per accedere ai servizi web di Aspose.Cells.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Esempio cURL – importazione dati (passo 1)
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
            <!-- Righe di esempio – solo alcune mostrate per brevità -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Sport</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Anno</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Trimestre</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Vendite</value></CellValue>
            <!-- …altri record omessi per chiarezza… -->
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
Codici di stato HTTP possibili:
- **200 OK** – Tabella pivot creata correttamente. Il corpo della risposta contiene un `TaskId` che può essere utilizzato per interrogare lo stato dell’operazione.
- **400 Bad Request** – Payload XML non valido o parametri obbligatori mancanti.
- **401 Unauthorized** – Token JWT mancante o non valido.
- **500 Internal Server Error** – Errore imprevisto lato server.

Esempio di risposta positiva (XML):

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

## Famiglia di SDK cloud

L’utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:
---