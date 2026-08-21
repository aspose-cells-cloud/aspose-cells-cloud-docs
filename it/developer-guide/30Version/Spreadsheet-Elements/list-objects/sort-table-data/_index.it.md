---
title: "Ordina i dati di ListObject in un foglio di lavoro Excel"
second_title: "Document"
linktitle: "Ordina"
type: docs
url: /list-objects/sort-data/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/, /tables/sort-data/]
keywords: "Aspose.Cells Cloud, Excel, ListObject, Ordina dati, REST API, Foglio di lavoro"
description: "Scopri come ordinare i dati di un ListObject (tabella) in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, richiesta cURL di esempio ed esempi di SDK."
weight: 40
ArticleTitle: "Ordina i dati di ListObject in un foglio di lavoro Excel – Aspose.Cells Cloud API"
---

**Prerequisiti**  
Per chiamare questa API è necessario disporre di un token di accesso JWT valido di Aspose Cloud e il file di lavoro deve essere caricato nello storage di Aspose Cloud. Includere l'intestazione `Authorization: Bearer <jwt token>` in ogni richiesta.

Questa API REST ordina i dati di una tabella in un foglio di lavoro Excel.  
Per utilizzare questa operazione, fornire il nome del file di lavoro, il nome del foglio di lavoro e l'indice dell'oggetto ListObject target, insieme a un corpo JSON `dataSorter` che definisce i criteri di ordinamento.

## API PostWorksheetListObjectSortTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome Parametro  | Tipo    | Path/Query String/HTTPBody | Descrizione                                                                                                     |
| --------------- | ------- | -------------------------- | --------------------------------------------------------------------------------------------------------------- |
| name            | string  | path                       | Nome del file Excel archiviato nello storage di Aspose Cloud.                                                  |
| sheetName       | string  | path                       | Nome del foglio di lavoro contenente il ListObject.                                                            |
| listObjectIndex | integer | path                       | Indice in base zero dell’oggetto ListObject (tabella) all’interno del foglio di lavoro.                         |
| dataSorter      | object  | body                       | Oggetto JSON che specifica le opzioni di ordinamento (es. `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`). |
| folder          | string  | query                      | Percorso della cartella nello storage in cui è situato il file Excel.                                          |
| storageName     | string  | query                      | Nome dello storage di Aspose Cloud.                                                                             |

**Note**  
Il corpo della richiesta deve essere un oggetto JSON valido che corrisponda allo schema `dataSorter`. Assicurarsi che il file di lavoro, il foglio di lavoro e il ListObject esistano prima di invocare l’operazione di ordinamento.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) definiscono un’interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
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

**Codici di stato HTTP**

| Codice di stato | Descrizione                               |
|----------------|-------------------------------------------|
| 200            | OK – ordinamento completato con successo. |
| 400            | Richiesta non valida – parametri non validi. |
| 401            | Non autorizzato – autenticazione non riuscita. |
| 404            | Non trovato – file di lavoro, foglio di lavoro o ListObject non trovato. |
| 500            | Errore interno del server – problema lato server. |

**Parametri della risposta**

| Parametro | Tipo    | Descrizione                                      |
|-----------|---------|--------------------------------------------------|
| Code      | integer | Codice di stato HTTP restituito dall'API.       |
| Status    | string  | Descrizione testuale del risultato (es. "OK").  |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sulle attività del proprio progetto. Consultare il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[Torna alla panoramica dei ListObjects](/list-objects/)