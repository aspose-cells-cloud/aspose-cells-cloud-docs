---
title: "Aggiungi un filtro in un foglio di lavoro Excel"
second_title: "Document"
linktype: "Aggiungi filtro"
type: docs
url: /it/autofilter/add-filter/
aliases: [/it/add-a-filter-for-a-filter-column/]
keywords: "Aspose.Cells, Cloud, Excel, AutoFiltro, Aggiungi Filtro, REST API, SDK"
description: "Scopri come aggiungere un autofiltro a una colonna in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi cURL, SDK e guida ai parametri."
weight: 60
ArticleTitle: "Aggiungi un filtro a un foglio di lavoro Excel utilizzando Aspose.Cells Cloud"
---

**Prerequisiti:** Prima di chiamare questa API è necessario ottenere un token JWT valido, assicurarsi che il libro di lavoro di destinazione sia caricato nell'archivio specificato e disporre delle autorizzazioni necessarie per accedere al file. Per gli esempi a riga di comando si consiglia una versione recente di cURL (7.68 o successiva).

Questa API REST aggiunge un filtro per una colonna specifica in un foglio di lavoro Excel.

## API PutWorksheetFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione |
|----------------|---------|-----------|-------------|
| name           | string  | Path      | Nome del libro di lavoro. |
| sheetName      | string  | Path      | Nome del foglio di lavoro. |
| range          | string  | Query     | Intervallo di celle che contiene il filtro (ad esempio `A1:B1`). |
| fieldIndex     | integer | Query     | Indice in base zero della colonna a cui viene applicato il filtro. |
| criteria       | string  | Query     | Criteri di filtro (ad esempio, un valore o un'espressione). |
| matchBlanks    | boolean | Query     | Impostare su `true` per includere le celle vuote nel filtro; altrimenti `false`. |
| refresh        | boolean | Query     | Impostare su `true` per aggiornare il filtro dopo l'applicazione; altrimenti `false`. |
| folder         | string  | Query     | Cartella in cui è memorizzato il libro di lavoro originale. |
| storageName    | string  | Query     | Nome del servizio di archiviazione. |

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
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

## Come utilizzare l'API PutWorksheetFilter con gli SDK

### Specifica dell'API PutWorksheetFilter

La <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
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

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
---