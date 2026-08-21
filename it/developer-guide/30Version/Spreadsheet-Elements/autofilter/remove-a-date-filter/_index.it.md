---
title: "Elimina un filtro data – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Elimina filtro data"
type: docs
url: /autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, elimina filtro data, filtro automatico Excel, API REST, SDK"
description: "Scopri come eliminare un filtro data da un foglio Excel utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri, esempio HTTPS cURL, payload di risposta e codice di esempio per SDK."
ArticleTitle: "Elimina un filtro data – Documentazione API Aspose.Cells Cloud"
---

Questa API REST elimina un filtro data su un foglio Excel.

**Prerequisiti:** Assicurati di avere un token JWT valido, che il file di lavoro sia archiviato in Aspose Cloud Storage e che tu disponga delle autorizzazioni appropriate per modificare il foglio.

## API DeleteWorksheetDateFilter

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome parametro       | Tipo    | Posizione | Descrizione                                                                                     |
|----------------------|---------|-----------|-------------------------------------------------------------------------------------------------|
| name                 | string  | path      | Nome del file Excel.                                                                            |
| sheetName            | string  | path      | Nome del foglio di lavoro.                                                                      |
| fieldIndex           | integer | query     | Indice in base zero della colonna a cui viene applicato il filtro.                             |
| dateTimeGroupingType | string  | query     | Tipo di raggruppamento per il filtro data (es. Year, Month, Day).                              |
| year                 | integer | query     | Componente anno del filtro (valore predefinito 0).                                              |
| month                | integer | query     | Componente mese del filtro (valore predefinito 0).                                              |
| day                  | integer | query     | Componente giorno del filtro (valore predefinito 0).                                            |
| hour                 | integer | query     | Componente ora del filtro (valore predefinito 0).                                               |
| minute               | integer | query     | Componente minuto del filtro (valore predefinito 0).                                            |
| second               | integer | query     | Componente secondo del filtro (valore predefinito 0).                                           |
| folder               | string  | query     | Percorso della cartella nello storage in cui si trova il file.                                  |
| storageName          | string  | query     | Nome dello storage Aspose Cloud.                                                                |

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
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato).         |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                           |
| 500    | Errore interno del server   | Errore imprevisto del server.                                               |

L'API restituisce codici di stato HTTP standard che indicano il risultato dell'operazione di eliminazione.

| Codice | Significato             | Descrizione                                                                 |
|--------|-------------------------|-----------------------------------------------------------------------------|
| 200    | OK                      | Filtro data eliminato correttamente; la risposta contiene lo stato dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (es. tipo di file non supportato).         |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                            |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                           |
| 500    | Errore interno del server | Errore imprevisto del server.                                               |

## Come utilizzare l'API DeleteWorksheetDateFilter con gli SDK

### Specifica dell'API DeleteWorksheetDateFilter

La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">specificazione OpenAPI</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
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

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}