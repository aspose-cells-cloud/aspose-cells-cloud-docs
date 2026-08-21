---
title: "Cerca nel contenuto del foglio di calcolo – API Aspose.Cells Cloud (trova testo in Excel)"
second_title: "Documento"
ArticleTitle: "Cerca testo nei fogli di calcolo Excel locali – Trova dati specifici"
linktitle: "Cerca nel contenuto del foglio di calcolo"
type: docs
url: /it/search-spreadsheet-content/
keywords: "Aspose.Cells, API di ricerca Excel, ricerca contenuto foglio di calcolo, API foglio di calcolo cloud, ricerca testo"
description: "Utilizza l'API Aspose.Cells Cloud per cercare testo, numeri o formule nei file Excel locali. Supporta query non distingue tra maiuscole e minuscole, ambito a livello di foglio di calcolo e autenticazione sicura."
weight: 100
---

## **API per la ricerca nel contenuto del foglio di calcolo**

Cerca programmaticamente testo specifico in qualsiasi foglio di calcolo Excel utilizzando l'API Aspose.Cells Cloud. L'API può individuare testo, numeri o formule in file locali archiviati nel cloud, abilitando flussi di lavoro automatizzati per il rilevamento dati, l'analisi dei contenuti e il controllo dei fogli di calcolo.

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

Se preferisci utilizzare HTTP grezzo, il seguente esempio cURL illustra la stessa richiesta:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta**

| Parametro    | Tipo    | Posizione | Descrizione                                                                                |
| ------------ | ------- | --------- | ------------------------------------------------------------------------------------------ |
| spreadsheet  | File    | FormData  | Il file Excel da cercare.                                                                  |
| searchText   | Stringa | Query     | Il testo (o valore numerico) da individuare nel foglio di calcolo.                        |
| ignoringCase | Booleano| Query     | Imposta su `true` per eseguire una ricerca che non distingue tra maiuscole e minuscole.    |
| worksheet    | Stringa | Query     | Nome del foglio di calcolo in cui limitare la ricerca. Se omesso, vengono esaminati tutti i fogli. |
| cellArea     | Stringa | Query     | Intervallo in stile A1 (es. `A1:C10`) che limita l'area di ricerca.                       |
| region       | Stringa | Query     | Regione geografica del servizio (es. `us-east-1`).                                        |
| password     | Stringa | Query     | Password necessaria per aprire un foglio di calcolo protetto.                             |

### **Risposta**

L'API restituisce un oggetto `SearchResult` che contiene un array di celle corrispondenti. Ogni elemento fornisce il nome del foglio di calcolo, l'indirizzo della cella e il testo corrispondente.

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Totale",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Totale",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### Codici di errore

- **400 Richiesta non valida** – L'URI della richiesta o i parametri non sono validi.
- **401 Non autorizzato** – Token di accesso mancante, non valido o credenziali client errate.
- **404 Non trovato** – Il foglio di calcolo specificato non può essere accesso.
- **500 Errore interno del server** – Si è verificato un errore imprevisto del server durante l'elaborazione del foglio di calcolo.

## Dove dovremmo utilizzare la funzionalità di ricerca nel contenuto del foglio di calcolo?

- **Audit completo di conformità del foglio di calcolo** – Scansiona l'intero foglio di calcolo per individuare termini sensibili (ad esempio, “Clausola riservata”, “Dati interni”) per controlli di sicurezza dei dati e conformità.
- **Query di associazione dati tra fogli** – Trova un numero di progetto o un nome cliente che appare su più fogli di calcolo, consentendo un'integrazione rapida tra fogli.
- **Verifica del contenuto dei modelli in batch** – Dopo aver generato report, verifica che tutti i segnaposto come `{{Data}}` siano stati correttamente sostituiti in un batch di file Excel.
- **Archiviazione e estrazione di dati storici** – Cerca nei file Excel legacy codici di evento o termini aziendali specifici per accelerare l'archeologia e l'analisi dei dati.

## Perché dovresti utilizzare la funzionalità di ricerca nel contenuto del foglio di calcolo?

- **Facile da usare per sviluppatori** – Sono disponibili SDK per molti linguaggi, riducendo lo sforzo di sviluppo rispetto alla creazione di una soluzione personalizzata.
- **Riduzione dei costi di manodopera** – Automatizza attività che altrimenti richiederebbero un'ispezione manuale dei fogli di calcolo.
- **Pagamento in base all'uso** – Paghi solo per le chiamate API effettivamente effettuate.
- **Nessuna manutenzione richiesta** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.
- **Preserva la formattazione complessa** – I risultati possono essere esportati in PDF mantenendo il layout originale di Excel.

## Come utilizzare la funzionalità di ricerca per link interrotti all'interno dell'API del foglio di calcolo con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per integrare la funzionalità di ricerca. L'SDK astrae il livello HTTP, consentendo di richiamare l'API con un codice minimo. Consulta l'elenco completo di SDK nel [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come richiamare l'operazione di ricerca nel contenuto del foglio di calcolo con vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}