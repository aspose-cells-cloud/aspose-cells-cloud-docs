---
title: "Cercare testo in fogli di calcolo Excel remoti – Aspose.Cells Cloud API"
second_title: "Documento"
ArticleTitle: "Cercare testo in fogli di calcolo Excel remoti – Trovare dati specifici"
linktitle: "Cercare contenuto in fogli di calcolo remoti"
type: docs
url: /search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, API di ricerca Excel, foglio di calcolo cloud, ricerca testo, REST"
description: "Cerca testo, numeri o formule in file Excel memorizzati in archiviazione cloud mediante Aspose.Cells Cloud. Supporta query case-insensitive, selezione cartelle e cartelle di lavoro protette da password."
weight: 100
---

### **Cercare contenuto in fogli di calcolo remoti tramite API**

Cerca programmaticamente un testo specifico all’interno di qualsiasi foglio di calcolo Excel utilizzando l’API Aspose.Cells Cloud. Trova testo, numeri o formule in file memorizzati in archiviazione cloud. Questa API RESTful consente di automatizzare flussi di lavoro per individuazione dati, analisi dei contenuti e audit dei fogli di calcolo.

### **API Web**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome parametro | Tipo    | Percorso/Query string/Corpo HTTP | Descrizione                                                                                                                                                      |
| :------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | Stringa | Percorso                       | **Obbligatorio**. Nome del file della cartella di lavoro Excel (inclusa l’estensione) in cui verrà eseguita la ricerca del testo, ad esempio `sales_data.xlsx`. |
| searchText     | Stringa | Query                      | **Obbligatorio**. Stringa, numero o porzione di contenuto esatto da individuare in tutta la cartella di lavoro o nei fogli di lavoro.                            |
| ignoringCase   | Booleano | Query                      | **Facoltativo**. Determina se la ricerca distingue maiuscole/minuscole. Impostare su `true` per abilitare la corrispondenza case-insensitive (ad es. “Report” trova anche “REPORT”); il valore predefinito è `false`. |
| folder         | Stringa | Query                      | **Facoltativo**. Percorso della directory all’interno dell’archiviazione cloud che contiene la cartella di lavoro target. Se omesso, si assume la cartella radice. |
| storageName    | Stringa | Query                      | **Facoltativo**. Identificatore di un servizio di archiviazione cloud configurato personalizzato. Se non specificato, l’API utilizza l’archiviazione predefinita associata all’account. |
| region         | Stringa | Query                      | **Facoltativo**. Impostazione locale (ad es. `it-IT`) applicata durante la ricerca, che può influenzare la normalizzazione o le regole di confronto del testo.     |
| password       | Stringa | Query                      | **Facoltativo**. Password di decrittazione necessaria per accedere a un file Excel protetto da password. Omettere questo parametro se il file non è crittografato. |

**Glossario**

- **searchText** – La stringa esatta da individuare; può essere una corrispondenza parziale.
- **ignoringCase** – `true` rende la ricerca case-insensitive; `false` impone la distinzione tra maiuscole e minuscole.
- **folder** – Percorso della directory che contiene la cartella di lavoro.
- **storageName** – Identificatore di una configurazione di archiviazione personalizzata.
- **region** – Codice locale che influisce sulle regole di confronto del testo.
- **password** – Password di decrittazione per cartelle di lavoro protette.

### **Risposta**

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

La risposta contiene un elenco delle celle (`CellName`) in cui è stato trovato il testo cercato, insieme al nome del foglio di lavoro e al testo corrispondente. Se non vengono trovate corrispondenze, l’array `Cells` è vuoto, ma la richiesta restituisce comunque HTTP 200 OK.

### Codici di errore

- **400 Bad Request** – URI API Aspose.Cells Cloud non valido.  
  ```json
  {"code":400,"message":"URI della richiesta non valido"}
  ```
- **401 Unauthorized** – Token di accesso, client ID o client secret non validi.  
  ```json
  {"code":401,"message":"Token di accesso non valido"}
  ```
- **404 Not Found** – Il file del foglio di calcolo non è accessibile.  
  ```json
  {"code":404,"message":"File non trovato"}
  ```
- **500 Server Error** – Una condizione imprevista ha impedito all’API di completare la richiesta.  
  ```json
  {"code":500,"message":"Errore interno del server"}
  ```

## Dove utilizzare la funzionalità di ricerca del contenuto all’interno di un foglio di calcolo tramite l’API?

- **Audit di conformità completo della cartella di lavoro** – Scansiona rapidamente l’intero file Excel per identificare tutti i termini sensibili (ad es. “Clausola Confidenziale”, “Dati Interni”) per controlli di sicurezza aziendale e conformità.
- **Ricerca di associazione dati tra fogli** – Quando le informazioni di progetto sono disperse su più fogli di lavoro, cerca un numero di progetto o un nome cliente specifico e localizza immediatamente tutti i dati correlati.
- **Verifica batch dei contenuti dei modelli** – Dopo la generazione automatica di report, scansiona più file Excel in batch per confermare che tutti i segnaposto predefiniti (come `{{Data}}`) siano stati correttamente sostituiti, garantendo completezza e accuratezza del report.
- **Archiviazione e mining di dati storici** – Analizza file legacy, cerca codici di evento specifici o termini aziendali e comprendi rapidamente la logica aziendale storica per l’archeologia dei dati.

## Perché utilizzare la funzionalità di ricerca del contenuto all’interno di un foglio di calcolo tramite l’API?

- **Facile per gli sviluppatori** – Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido con documentazione completa. Rispetto alla creazione di soluzioni personalizzate, riduce notevolmente lo sforzo di sviluppo.
- **Riduzione dei costi del lavoro** – Automatizza attività di ricerca ripetitive, liberando gli sviluppatori da compiti manuali di estrazione dati.
- **Pay-per-use** – Nessun investimento iniziale; si paga solo per le chiamate API effettivamente utilizzate.
- **Nessuna manutenzione richiesta** – Aspose gestisce server, aggiornamenti e compatibilità, consentendoti di concentrarti sulla logica della tua applicazione.
- **Preserva la formattazione complessa di Excel** – I risultati possono essere esportati in formato PDF universalmente accessibile, mantenendo lo stile originale.

## Come utilizzare la ricerca per link interrotti all’interno di un intervallo del foglio di calcolo tramite le SDK

### Specifica OpenAPI

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un’interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

### Utilizzare le SDK Aspose.Cells Cloud

L’utilizzo dell’SDK è il modo migliore per accelerare lo sviluppo. L’SDK gestisce i dettagli sottostanti, consentendoti di implementare semplicemente la ricerca di contenuti all’interno dei fogli di calcolo per le celle con un numero minimo di righe di codice. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo delle SDK Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come richiamare i servizi web Aspose.Cells Cloud utilizzando varie SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---