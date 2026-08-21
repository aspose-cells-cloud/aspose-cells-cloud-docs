---
title: "Copia di un intervallo in un foglio di calcolo con opzioni di incolla"
second_title: "Document"
linktype: "Copy"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Aspose.Cells Cloud, REST API, Excel, copia intervallo, foglio di calcolo, opzioni di incolla"
description: "Utilizza l'API REST di Aspose.Cells Cloud per copiare un intervallo all'interno di un foglio di calcolo Excel con il supporto completo delle opzioni di incolla. Include esempi di SDK per diversi linguaggi di programmazione."
weight: 20
ArticleTitle: "Copia di un intervallo in un foglio di calcolo con opzioni di incolla – Aspose.Cells Cloud API"
---

Questa API REST consente di copiare un intervallo in un foglio di calcolo di un file Excel. Per operazioni correlate, consulta la documentazione **Ottieni intervallo** e **Aggiorna intervallo**.

**Prerequisiti:** Per utilizzare questo endpoint è necessario disporre di un token OAuth 2.0 / JWT valido e assicurarsi che la versione dell'API corrisponda all'URL della richiesta.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **Parametri della richiesta**

| Nome del parametro | Tipo   | Posizione | Descrizione                                                                                  |
| ------------------ | ------ | --------- | -------------------------------------------------------------------------------------------- |
| name               | string | path      | Il nome del file Excel (workbook).                                                           |
| sheetName          | string | path      | Il nome del foglio di calcolo (worksheet).                                                   |
| rangeOperate       | string | body      | L'operazione da eseguire: `copydata`, `copystyle`, `copyto` o `copyvalue`.                   |
| folder             | string | query     | La cartella contenente il file Excel.                                                        |
| storageName        | string | query     | Il nome del servizio di archiviazione.                                                       |

**Note:** Il campo `rangeOperate` determina cosa viene copiato. Utilizzare `copydata` per copiare solo i valori delle celle, `copystyle` per lo stile/formattazione, `copyto` per sia dati che stile, e `copyvalue` per copiare i valori senza formule. L'API supporta intervalli fino a 1 milione di celle; intervalli più ampi potrebbero causare un timeout.

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopy) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Una risposta corretta restituisce lo stato `200 OK`. In caso di errore, l'API potrebbe restituire payload come:

```json
{
  "Code": 400,
  "Message": "Bad Request – parametri non validi."
}
```

oppure

```json
{
  "Code": 401,
  "Message": "Unauthorized – token di autenticazione mancante o non valido."
}
```

Questi oggetti di errore includono un codice di stato HTTP e un messaggio descrittivo per aiutare a diagnosticare i problemi.

{{< /tab >}}

{{< /tabs >}}

Puoi scaricare un file Excel di esempio per testare l'operazione di copia [qui](https://example.com/sample.xlsx).

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}