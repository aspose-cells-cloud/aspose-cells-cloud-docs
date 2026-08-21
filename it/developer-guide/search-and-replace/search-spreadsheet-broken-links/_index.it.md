---
title: "Cerca Link Rotti nel Foglio di Calcolo – API di Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Trova e Ripara Link Rotti in Excel – Verificatore di Link per Fogli di Calcolo Cloud"
linktype: "Cerca Link Rotti nel Foglio di Calcolo"
type: docs
url: /it/search-spreadsheet-broken-links/
keywords: "Aspose Cells, link rotti, audit del foglio di calcolo, API Excel, foglio di calcolo cloud, verificatore di link"
description: "Rileva e risolvi link rotti nei file Excel tramite l'API Aspose.Cells Cloud. Analizza intervalli, ottieni risultati dettagliati in formato JSON e integra con qualsiasi SDK linguistico."
weight: 100
---

## **API per la Ricerca di Link Rotti nei Fogli di Calcolo**

Rileva automaticamente i link rotti nei file Excel. La nostra API analizza intervalli specificati per individuare riferimenti esterni rotti, formule non valide e fonti di dati mancanti. Supporta l’audit remoto dei fogli di calcolo, controlli di qualità automatizzati e l’integrazione con provider di archiviazione cloud. API RESTful per l’automazione dei flussi di lavoro aziendali.

**Sommario:** Utilizza questo endpoint per identificare e riparare rapidamente link non validi nei file di lavoro, garantendo l’integrità dei dati in modelli finanziari, set di dati per fusioni e acquisizioni e pacchetti pronti per gli investitori.

### **API Web**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Foglio1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@esempio.xlsx"
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della Richiesta

| Nome Parametro | Tipo   | Posizione             | Descrizione                                                                                                           |
| -------------- | ------ | -------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData (multipart) | **Obbligatorio.** Il file di lavoro Excel (`.xlsx`, `.xls`, ecc.) da analizzare.                                    |
| worksheet      | String | Query                | **Opzionale.** Il nome del foglio di calcolo da analizzare. Se omesso, viene utilizzato il primo foglio.            |
| cellArea       | String | Query                | **Opzionale.** Intervallo di celle target in notazione A1 (es. `B2:D10`). Se non specificato, viene analizzata l’intera area utilizzata. |
| region         | String | Query                | **Opzionale.** Impostazione di localizzazione (es. `it-IT`) che può influenzare l’interpretazione di date, numeri o valute. |
| password       | String | Query                | **Opzionale.** Password per file di lavoro crittografati. Lasciare vuoto se il file non è protetto.                  |

### Risposta

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "File non trovato",
      "Status": "Broken"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 Not Found",
      "Status": "Broken"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Codici di Errore

| Codice | Descrizione |
|------|-------------|
| **400 Bad Request** | URI API Aspose.Cells Cloud non valido. |
| **401 Unauthorized** | Token di accesso, client ID o client secret non validi. |
| **404 Not Found** | Il file del foglio di calcolo non è accessibile. |
| **429 Too Many Requests** | Limite di richieste superato (60 chiamate / minuto). |
| **500 Server Error** | Si è verificata un’anomalia durante il recupero dei dati di calcolo dal foglio di calcolo. |


## Dove utilizzare la funzionalità di Ricerca Link Rotti nell’API per Fogli di Calcolo?

- **Audit Regolare di Grandi Modelli Finanziari**: Prima della pubblicazione di report mensili o trimestrali, analizza automaticamente le aree chiave di calcolo (es. `Dashboard!B5:K50`) contenenti molti riferimenti esterni per verificare che tutti i link puntino a file sorgenti validi.  
- **Integrazione Dati per Fusioni e Acquisizioni**: Durante la fusione di più file di fogli di calcolo rappresentanti unità aziendali, analizza il foglio “Panoramica” dopo l’integrazione per identificare link resi invalidi da percorsi dei file modificati o da problemi di permessi.  
- **Preparazione di Pacchetti Dati per Investitori**: Prima della finalizzazione dei materiali di presentazione contenenti grafici e tabelle collegati a database esterni o fonti di dati di mercato, verifica la validità di tutti i link.

## Perché utilizzare la funzionalità di Ricerca Link Rotti nell’API per Fogli di Calcolo?

- **Facile da Usare per gli Sviluppatori** – Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e documentazione esaustiva. Rispetto alla creazione di soluzioni personalizzate, riduce significativamente il carico di lavoro di sviluppo.  
- **Riduzione dei Costi del Lavoro** – Elimina la necessità di personale dedicato alla verifica manuale dei link nei documenti.  
- **Pagamento in Base all’Utilizzo** – Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.  
- **Costi di Manutenzione Nullo** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.  
- **Mantiene la Formattazione Complessa di Excel** – I risultati vengono restituiti in formato JSON universalmente accessibile, preservando la struttura originale del file di lavoro.

## Come Utilizzare la Ricerca Link Rotti nell’API per Fogli di Calcolo con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} definiscono un’interfaccia di programmazione pubblicamente accessibile, consentendo di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare gli SDK è il modo migliore per velocizzare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendoti di implementare facilmente la funzionalità di ricerca link rotti con un numero minimo di righe di codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}