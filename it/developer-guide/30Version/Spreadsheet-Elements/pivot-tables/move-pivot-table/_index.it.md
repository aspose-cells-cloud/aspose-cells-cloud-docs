---
title: "Sposta una tabella pivot in un file Excel"
second_title: "Document"
linktype: Sposta
type: docs
url: /it/pivot-tables/move/
aliases: [  /it/move-pivot-table/ ]
keywords: "Aspose.Cells Cloud, sposta tabella pivot, Excel, REST API, SDK, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per spostare una tabella pivot all'interno di un workbook Excel. Gli SDK sono disponibili per Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift."
weight: 120
---

Questa REST API sposta una tabella pivot all'interno di un workbook Excel.

**Prerequisiti:** Prima di chiamare questa operazione devi disporre di un token di accesso JWT valido e il workbook deve essere memorizzato nello storage di Aspose Cloud. Specifica i parametri `folder` e `storageName` secondo le necessità.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Move
```

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                              |
| --------------- | ------- | --------- | -------------------------------------------------------- |
| name            | string  | path      | Nome del file Excel.                                     |
| sheetName       | string  | path      | Nome del foglio di calcolo contenente la tabella pivot.  |
| pivotTableIndex | integer | path      | Indice in base zero della tabella pivot da spostare.     |
| fieldIndex      | integer | query     | Indice del campo pivot da spostare.                      |
| from            | string  | query     | Area di origine del campo (ad esempio, `Row` o `Column`).|
| to              | string  | query     | Area di destinazione del campo (ad esempio, `Row` o `Column`). |
| folder          | string  | query     | Cartella nello storage in cui è posizionato il file.     |
| storageName     | string  | query     | Nome del servizio di storage.                            |

Lo [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldMoveTo) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Move?fieldIndex=0&from=C1&to=C10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Family di SDK Cloud

Utilizzare un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Utilizzare endpoint HTTPS in produzione.
public void Run_PivotTable_Move()
{
    url = @"https://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null}, ... ],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/Move?row=10&column=10&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Move?fieldIndex=1&from=Row&to=Column&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "60360c7d035abd1b2c9e36c68c9f00fb" >}}

{{< /tab >}}

{{< /tabs >}}