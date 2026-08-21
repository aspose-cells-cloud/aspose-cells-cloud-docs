---
title: "Raggruppa righe in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Rimuovi raggruppamento"
type: docs
url: /it/rows/ungroup/
aliases: [/it/ungroup-rows-in-excel-worksheet/]
keywords: "Rimuovi raggruppamento righe, Excel, Aspose.Cells Cloud, REST API, SDK, foglio di calcolo"
description: "Scopri come rimuovere il raggruppamento delle righe in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud e gli SDK per vari linguaggi di programmazione."
weight: 70
---

Questa API REST rimuove il raggruppamento delle righe in un foglio di lavoro Excel.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
```

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                                                 |
| -------------- | ------- | --------- | --------------------------------------------------------------------------- |
| name           | string  | path      | Il nome del foglio di calcolo.                                             |
| sheetName      | string  | path      | Il nome del foglio di lavoro.                                              |
| firstIndex     | integer | query     | L'indice in base zero della prima riga da sottoporre a rimozione del raggruppamento. |
| lastIndex      | integer | query     | L'indice in base zero dell'ultima riga da sottoporre a rimozione del raggruppamento. |
| isAll          | boolean | query     | Se **true**, vengono rimosse le righe raggruppate in tutto l'intervallo specificato. |
| folder         | string  | query     | La cartella contenente il foglio di calcolo.                               |
| storageName    | string  | query     | Il nome dell'archivio in cui si trova il foglio di calcolo.                |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
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

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il modo più efficiente per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}