---
title: "Aggiungi un filtro a icone a un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Aggiungi filtro a icone"
type: docs
url: /it/autofilter/add-icon-filter/
aliases: [  /it/add-an-icon-filter/ , /it/autofilter/add-an-icon-filter/ ]
keywords: "Aspose.Cells Cloud, Excel, Filtro a icone, Filtro automatico, API REST"
description: "Scopri come aggiungere un filtro a icone a un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud, con i dettagli della richiesta, un esempio cURL, campioni di codice SDK e gestione degli errori."
weight: 65
ArticleTitle: "Aggiungi un filtro a icone a un foglio di lavoro Excel – Documentazione Aspose.Cells Cloud"
---

## API REST

Questa API REST aggiunge un **filtro a icone** a un foglio di lavoro Excel utilizzando l'**API REST di Aspose.Cells Cloud**.

**Contesto:** Un filtro a icone applica un insieme visivo di icone alle celle in base ai loro valori, consentendo un'analisi rapida dei trend dei dati tramite rappresentazione visiva. I casi d'uso più comuni includono l'evidenziazione di metriche di prestazione, indicatori di stato o la categorizzazione dei valori con icone a semaforo direttamente all'interno dei fogli di lavoro Excel.


```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.


### Parametri della richiesta:

| Nome parametro | Tipo    | Posizione | Descrizione |
|----------------|---------|-----------|-------------|
| name           | string  | Path      | Nome del workbook. |
| sheetName      | string  | Path      | Nome del foglio di lavoro. |
| range          | string  | Query     | Intervallo di celle (ad esempio, `A1:B1`) a cui verrà applicato il filtro. |
| fieldIndex     | integer | Query     | Indice in base zero della colonna interessata dal filtro. |
| iconSetType    | string  | Query     | Insieme di icone da utilizzare. Valori ammessi: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId         | integer | Query     | Identificatore dell'icona specifica all'interno dell'insieme selezionato. |
| matchBlanks    | boolean | Query     | Determina se le celle vuote vengono incluse (`true` o `false`). |
| refresh        | boolean | Query     | Indica se il filtro deve essere aggiornato dopo l'applicazione (`true` o `false`). |
| folder         | string  | Query     | Cartella contenente il workbook originale. |
| storageName    | string  | Query     | Nome dello storage in cui risiede il workbook. |

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
| 500    | Errore interno del server   | Errore imprevisto del server. |

## Come utilizzare l'API PutWorksheetIconFilter con gli SDK

### Specifica dell'API PutWorksheetIconFilter

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
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

Possibili codici di stato della risposta:

| Codice | Descrizione |
|--------|-------------|
| 200    | Filtro applicato correttamente. |
| 400    | Richiesta non valida – parametri mancanti o non validi. |
| 401    | Non autorizzato – token di autenticazione non valido o mancante. |
| 404    | Workbook, foglio di lavoro o intervallo specificato non trovato. |
| 500    | Errore interno del server. |
{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Per ulteriori funzionalità di AutoFilter, consulta la documentazione su **[Aggiungi filtro per colore](/it/autofilter/add-color-filter/)**, **[Aggiungi filtro per data](/it/autofilter/add-date-filter/)** e **[Rimuovi filtro automatico](/it/autofilter/clear-autofilter/)**.