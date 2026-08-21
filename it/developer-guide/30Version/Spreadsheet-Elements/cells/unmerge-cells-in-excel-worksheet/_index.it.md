---
title: "Separa le celle in un foglio di lavoro Excel"
type: docs
url: /it/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, separa celle, API REST, SDK cloud"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per separare le celle in un foglio di lavoro Excel, con esempi di richiesta, formato della risposta e campioni di codice SDK per diversi linguaggi di programmazione."
ArticleTitle: "Separa le celle in un foglio di lavoro Excel"
---

Questa API REST separa le celle in un file Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## Sicurezza e autenticazione

Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                             |
|----------------|---------|-----------|---------------------------------------------------------|
| name           | string  | path      | Nome del file del workbook.                             |
| sheetName      | string  | path      | Nome del foglio di lavoro.                              |
| startRow       | integer | query     | Indice in base zero della prima riga da separare.     |
| startColumn    | integer | query     | Indice in base zero della prima colonna da separare.  |
| totalRows      | integer | query     | Numero di righe da includere nell'operazione di separazione. |
| totalColumns   | integer | query     | Numero di colonne da includere nell'operazione di separazione. |
| folder         | string  | query     | Percorso della cartella in cui è memorizzato il workbook. |
| storageName    | string  | query     | Nome del servizio di archiviazione.                     |

## **Risposta**

Restituisce `CellCloudResponse`.

- **Panoramica dei campi di risposta**

| Campo           | Tipo    | Descrizione                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                                                    |
| `Code`           | integer | 200, 400, 401, 500, ...                             |


```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto sul server. |
## Come utilizzare l'API PostWorksheetUnmerge con gli SDK

### Specifica dell'API PostWorksheetUnmerge

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando `cURL` per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---