---
title: "Aggiungi un filtro colore in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Aggiungi filtro colore"
type: docs
url: /it/autofilter/add-color-filter/
aliases: [  /it/filter-a-list-using-a-color-filter/ , /it/autofilter/add-a-color-filter/ ]
keywords: "Excel, filtro colore, Aspose.Cells Cloud, REST API, filtro automatico, autenticazione JWT"
description: "Scopri come applicare un filtro colore in un foglio di lavoro Excel con Aspose.Cells Cloud API. Include endpoint, parametri, esempio cURL, gestione errori ed esempi di SDK."
weight: 65
ArticleTitle: "Aggiungi un filtro colore in un foglio di lavoro Excel usando Aspose.Cells Cloud API"
---

Scopri come aggiungere un filtro colore in un foglio di lavoro Excel utilizzando l'API Aspose.Cells Cloud. Questa guida copre l'endpoint richiesto, i parametri, i prerequisiti di autenticazione, la richiesta cURL di esempio, gli esempi di SDK e la gestione della risposta.

Questa API REST aggiunge un **filtro colore** a un foglio di lavoro Excel.

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta:


| Nome Parametro | Tipo    | Posizione | Descrizione                                                                 |
|----------------|---------|-----------|-----------------------------------------------------------------------------|
| name           | string  | path      | Il nome del file Excel.                                                     |
| sheetName      | string  | path      | Il nome del foglio di lavoro contenente i dati da filtrare.                |
| range          | string  | query     | L'intervallo di celle a cui viene applicato il filtro (es. `A1:B10`).      |
| fieldIndex     | integer | query     | Indice in base zero della colonna su cui viene applicato il filtro colore. |
| colorFilter    | object  | body      | Oggetto JSON che definisce i colori in primo piano e in secondo piano da filtrare. |
| matchBlanks    | boolean | query     | Se le righe con celle vuote debbano essere incluse nei risultati del filtro. |
| refresh        | boolean | query     | Se `true`, il foglio di lavoro viene aggiornato dopo l'applicazione del filtro. |
| folder         | string  | query     | La cartella nello storage in cui si trova il file Excel.                    |
| storageName    | string  | query     | Il nome del servizio di storage (es. Aspose Cloud Storage).                 |

**Schema JSON di `colorFilter`**

| Proprietà         | Tipo   | Descrizione                                                                    | Obbligatoria |
|-------------------|--------|--------------------------------------------------------------------------------|--------------|
| Pattern           | string | Schema di filtro (es. `"Solid"`).                                             | Sì           |
| ForegroundColor   | object | Definisce il colore in primo piano. Contiene le sotto‑proprietà `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor` e `Type`. | No |
| BackgroundColor   | object | Definisce il colore in secondo piano. Stesse sotto‑proprietà di `ForegroundColor`. | No |

### **Risposta**

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
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

## Come usare l'API PutWorksheetColorFilter con gli SDK

### Specifica dell'API PutWorksheetColorFilter

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) definiscono un'interfaccia di programmazione accessibile pubblicamente e permettono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Vedi anche:** [Aggiungi un filtro personalizzato](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [Aggiungi un filtro per data](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [Rimuovi un filtro automatico](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/).
---