---
title: "Aggiungi filtro data a un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Aggiungi filtro data"
type: docs
url: /it/autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "Scopri come aggiungere un filtro data a un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include esempio cURL, frammenti di codice SDK (C#, Java, Python, ecc.), parametri e gestione degli errori."
weight: 65
ArticleTitle: "Aggiungi filtro data a un foglio di calcolo Excel | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, filtro data Excel, API AutoFilter, API REST, SDK cloud, cURL, automazione fogli di calcolo"
---

Questa API REST aggiunge un **filtro data** a un foglio di calcolo Excel.

**Prerequisiti:** È necessario disporre di un token JWT valido e il workbook di destinazione deve già esistere nella posizione di archiviazione specificata. La richiesta non richiede un corpo JSON.

## API PutWorksheetDateFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Sicurezza e autenticazione**

Le API REST di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta


| Nome parametro           | Tipo    | Posizione | Descrizione                                                                                                                                                     |
| ------------------------ | ------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path      | Nome del workbook.                                                                                                                                              |
| **sheetName**            | string  | Path      | Nome del foglio di calcolo.                                                                                                                                     |
| **range**                | string  | Query     | Intervallo Excel a cui viene applicato il filtro (ad es. `A1:B1`).                                                                                                     |
| **fieldIndex**           | integer | Query     | Indice in base zero della colonna da filtrare.                                                                                                                       |
| **dateTimeGroupingType** | string  | Query     | Tipo di raggruppamento per il filtro data/ora. I valori ammessi sono `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. I valori sono case-sensitive; il valore predefinito è `Day`. |
| **year**                 | integer | Query     | Componente anno del valore filtro.                                                                                                                             |
| **month**                | integer | Query     | Componente mese del valore filtro.                                                                                                                            |
| **day**                  | integer | Query     | Componente giorno del valore filtro.                                                                                                                              |
| **hour**                 | integer | Query     | Componente ora del valore filtro.                                                                                                                             |
| **minute**               | integer | Query     | Componente minuto del valore filtro.                                                                                                                           |
| **second**               | integer | Query     | Componente secondo del valore filtro.                                                                                                                           |
| **matchBlanks**          | boolean | Query     | Includi celle vuote (`true` o `false`).                                                                                                                        |
| **refresh**              | boolean | Query     | Aggiorna il filtro dopo l'applicazione (`true` o `false`).                                                                                                          |
| **folder**               | string  | Query     | Percorso della cartella del workbook originale.                                                                                                                           |
| **storageName**          | string  | Query     | Nome del servizio di archiviazione.                                                                                                                                    |

*L'richiesta PUT non richiede un corpo di richiesta; tutti i parametri vengono forniti tramite stringa di query.*

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                     | Descrizione                                      |
|--------|----------------------------------|--------------------------------------------------|
| 200    | OK                               | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida             | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato                  | Token JWT non valido o mancante. |
| 413    | Payload troppo grande            | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server        | Errore imprevisto sul server. |

## Come utilizzare l'API PutWorksheetDateFilter con gli SDK

### Specifica dell'API PutWorksheetDateFilter

La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
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

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli a basso livello in modo che tu possa concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}