---
title: "Elimina un filtro da un foglio di calcolo Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Elimina filtro"
type: docs
url: /it/delete-filter/
aliases: [/it/delete-a-filter-for-a-filter-column/, /it/delete-auto-filter/]
keywords: "Aspose.Cells Cloud elimina filtro, Excel, REST API, SDK"
description: "Scopri come eliminare un filtro automatico da un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud, cURL e SDK (C#, Java, Python, ecc.). Include endpoint, parametri, autenticazione e codice di esempio."
weight: 100
---

## API REST

Questa API REST elimina un **filtro automatico (AutoFilter)** su un foglio di calcolo Excel.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro           | Tipo    | Posizione | Obbligatorio? | Descrizione                                                                                   |
| ------------------------ | ------- | --------- | ------------- | --------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path      | Sì            | Nome del workbook.                                                                            |
| **sheetName**            | string  | Path      | Sì            | Nome del foglio di calcolo.                                                                   |
| **range**                | string  | Query     | No            | Intervallo di celle a cui si applica il filtro (ad es. `A1:C10`).                             |
| **fieldIndex**           | integer | Query     | Sì            | Indice in base zero della colonna a cui è applicato il filtro.                                |
| **dateTimeGroupingType** | string  | Query     | No            | Modalità di raggruppamento dei valori data/ora: `Day`, `Hour`, `Minute`, `Month`, `Second`, o `Year`. |
| **year**                 | integer | Query     | No            | Componente anno per il raggruppamento delle date.                                             |
| **month**                | integer | Query     | No            | Componente mese per il raggruppamento delle date.                                             |
| **day**                  | integer | Query     | No            | Componente giorno per il raggruppamento delle date.                                           |
| **hour**                 | integer | Query     | No            | Componente ora per il raggruppamento delle date.                                              |
| **minute**               | integer | Query     | No            | Componente minuto per il raggruppamento delle date.                                           |
| **second**               | integer | Query     | No            | Componente secondo per il raggruppamento delle date.                                          |
| **matchBlanks**          | boolean | Query     | No            | `true` / `false` – indica se le celle vuote sono incluse nel filtro.                          |
| **refresh**              | boolean | Query     | No            | `true` / `false` – indica se aggiornare il foglio di calcolo dopo l'eliminazione.             |
| **folder**               | string  | Query     | No            | Cartella originale del workbook.                                                              |
| **storageName**          | string  | Query     | No            | Nome dello storage.                                                                           |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad es. tipo di file non supportato).      |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                           |
| 500    | Errore interno del server   | Errore imprevisto nel server.                                               |

## Come utilizzare l'API DeleteWorksheetFilter con gli SDK

### Specifica dell'API DeleteWorksheetFilter

La [specificazione OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
  -X DELETE \
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

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più efficiente per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

---