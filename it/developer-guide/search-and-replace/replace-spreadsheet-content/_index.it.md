---
title: "Aspose.Cells Cloud – Sostituisci testo in file Excel locali (API Trova e Sostituisci)"
second_title: "Documento"
ArticleTitle: "Sostituzione massiva di testo in file Excel locali – API Trova e Sostituisci"
linktitle: "Sostituisci contenuto del foglio di calcolo"
type: docs
url: /it/replace-spreadsheet-content/
keywords: "sostituisci testo in Excel, Aspose.Cells Trova e Sostituisci, API foglio di calcolo locale, sostituisci file Excel, API sostituisci contenuto"
description: "Sostituisci il testo nei file Excel locali senza caricarli nel cloud. Usa l'API Trova e Sostituisci di Aspose.Cells Cloud per aggiornare intervalli specifici, fogli di lavoro o file completi in una singola chiamata."
weight: 100
---

Sostituisci il testo specificato nei file Excel locali senza caricarli nel cloud. Aggiorna il contenuto dei file di lavoro in modo efficiente utilizzando l'API Trova e Sostituisci di Aspose.Cells Cloud per la modifica offline.

## **API per la sostituzione del contenuto del foglio di calcolo**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                                                                                                                  |
| :------------- | :----- | :----------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                             | Il file locale del foglio di calcolo da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                                               |
| searchText     | String | Query                                | La stringa di testo da cercare all'interno del foglio di lavoro e dell'area di celle specificate.                                                                          |
| replaceText    | String | Query                                | La stringa di testo che sostituirà tutte le occorrenze di `searchText` all'interno dell'intervallo specificato.                                                            |
| worksheet      | String | Query                                | _(Opzionale)_ Il nome del foglio di lavoro in cui verrà eseguita l'operazione di trova e sostituisci. Se omesso, l'operazione verrà applicata al primo foglio di lavoro.     |
| cellArea       | String | Query                                | _(Opzionale)_ L'intervallo specifico di celle (ad es. `"A1:D20"`, `"B5:F15"`) in cui verranno eseguite la ricerca e la sostituzione del testo. Se omesso, l'operazione verrà applicata a tutte le celle utilizzate nel foglio di lavoro specificato. |
| region         | String | Query                                | _(Opzionale)_ Imposta il locale per la gestione del testo, che potrebbe influenzare la distinzione tra maiuscole e minuscole e la codifica dei caratteri nelle ricerche (ad es. `"en-US"`, `"fr-FR"`). |
| password       | String | Query                                | _(Opzionale)_ Se il foglio di calcolo caricato è protetto da password, fornire la password per aprirlo ed elaborarlo.                                                      |

### **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

La risposta è un flusso binario contenente il file di lavoro aggiornato. Salvalo con l'estensione appropriata (ad es. `.xlsx`).

### **Codici di errore**

- **400 Bad Request** – URI dell'API Aspose.Cells Cloud non valido o parametri malformati.
- **401 Unauthorized** – Token di accesso non valido o mancante; ottieni un nuovo token.
- **404 Not Found** – Il file del foglio di calcolo non è accessibile o il foglio di lavoro specificato non esiste.
- **500 Server Error** – Si è verificato un errore interno durante l'elaborazione del foglio di calcolo; contattare il supporto se il problema persiste.

## Dove dovremmo utilizzare l'API per la sostituzione del contenuto del foglio di calcolo?

- **Elaborazione batch di file Excel locali** – Automatizza il trova e sostituisci su molti file di lavoro memorizzati on-premise.
- **Pipeline di dati on-premise** – Integra l'API in processi pianificati che modificano report prima che vengano archiviati o distribuiti.
- **Generazione locale di report** – Inserisci dinamicamente valori nei file di lavoro modello senza caricarli nel cloud.

## Perché dovresti utilizzare l'API per la sostituzione del contenuto del foglio di calcolo?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e documentazione completa. Rispetto alla creazione di soluzioni personalizzate, ciò riduce significativamente lo sforzo di sviluppo.
- **Riduzione dei costi del personale** – Riduce la necessità di personale dedicato per eseguire manualmente la consolidazione dei documenti.
- **Pay-per-use** – Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.
- **Costi zero di manutenzione** – Nessun server da mantenere, nessun aggiornamento software e nessun problema di compatibilità.
- **Preserva la formattazione complessa di Excel** – La formattazione, le formule e i grafici del file di lavoro originale rimangono inalterati dopo la sostituzione.

## Come utilizzare l'API per la sostituzione del contenuto del foglio di calcolo con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) definiscono un'interfaccia di programmazione accessibile pubblicamente, consentendo di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare le operazioni di sostituzione del contenuto con un codice minimo. Consulta il repository ufficiale **Aspose.Cells Cloud SDK su GitHub** per un elenco completo dei linguaggi supportati.

I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}