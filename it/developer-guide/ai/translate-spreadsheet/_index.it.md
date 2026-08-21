---
title: "Aspose.Cells Cloud Web API – Traduci foglio di calcolo nella lingua di destinazione"
second_title: "Documento"
ArticleTitle: "Come tradurre un intero foglio di calcolo utilizzando l'API di traduzione AI di Aspose.Cells Cloud"
linktype: "Traduci foglio di calcolo"
type: docs
url: /it/translate-spreadsheet/
keywords: "Aspose.Cells Cloud, API di traduzione foglio di calcolo, traduzione AI, traduzione foglio di calcolo, targetLanguage, traduzione multi-foglio, elaborazione foglio di calcolo cloud, traduzione Aspose.Cells Cloud"
description: "Traduci un intero libro Excel con Aspose.Cells Cloud AI. Mantieni formule, grafici e formattazione durante la conversione del testo in qualsiasi lingua supportata. Scopri endpoint, parametri, esempi SDK, limiti e gestione degli errori."
weight: 100
---

L'endpoint **TranslateSpreadsheet**, parte dell'**API di traduzione foglio di calcolo**, legge ogni elemento di testo in un libro, invia il contenuto a un servizio di traduzione alimentato dall'AI e restituisce un nuovo file foglio di calcolo in cui tutti i dati testuali sono renderizzati nella **targetLanguage** specificata. L'operazione mantiene intatti la struttura originale, gli stili delle celle, le formule e la struttura multi-foglio, rendendola ideale per la globalizzazione di report, dashboard e documenti basati sui dati. I formati di file supportati includono XLS, XLSX, XLSM, CSV e ODS. Gli errori vengono restituiti per codici linguistici non validi, errori di autenticazione o disservizi del servizio di traduzione.

## **API di traduzione foglio di calcolo**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Posizione | Obbligatorio/Opzionale | Descrizione                                                                                                                                                                                                 |
| :------------- | :----- | :-------- | :-------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | Richiesto | FormData              | Il libro Excel da tradurre. Estensioni accettabili: .xls, .xlsx, .xlsm, .csv, .ods. Dimensione massima file: 50 MB. Esempio: `budget.xlsx`.                                                               |
| targetLanguage | string | Richiesto | Query                 | Codice linguistico ISO 639-1 per la lingua di output desiderata (ad esempio, "es" per spagnolo, "fr" per francese, "de" per tedesco). Deve essere una lingua supportata dal servizio AI sottostante.              |
| region         | string | Opzionale | Query                 | Identificatore di area geografica del foglio di calcolo che influisce sul formato specifico della localizzazione, come date, numeri e valuta. Valori comuni: "US", "EU", "CN". Se omesso, viene utilizzata l’impostazione regionale originale del libro. |
| password       | string | Opzionale | Query                 | Password per aprire un libro protetto. Lasciare vuoto quando il file non è protetto da password.                                                                                                             |

### **Risposta**

Risposta positiva (200 OK)  
Intestazioni:  
Content-Type: application/octet-stream // oppure text/csv quando viene richiesto l'output CSV  
Content-Disposition: attachment; filename="translated.xlsx"  
Content-Length: <dimensione in byte>

Corpo:  
<flusso binario contenente il file foglio di calcolo tradotto>

Le risposte di errore seguono il modello standard di errore di Aspose.Cells Cloud (application/json) con campi `code`, `message` e `details` opzionale.

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato).      |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                     |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                          |

## Dove dovremmo utilizzare l'API di traduzione foglio di calcolo?

- **Reso conto finanziario internazionale** – Converti report trimestrali Excel in più lingue per uffici regionali, mantenendo formule e layout dei grafici.
- **Dashboard di marketing multilingue** – Genera automaticamente versioni localizzate delle dashboard di performance delle vendite per team globali.
- **Distribuzione di contenuti educativi** – Traduci quaderni, schede di esercizi o fogli di calcolo curricolari per studenti in diversi paesi, senza copiare e incollare manualmente.
- **Conformità normativa** – Produci fogli di calcolo per la conformità specifici per lingua, mantenendo regole di convalida e liste di convalida dati.

## Perché dovresti utilizzare l'API di traduzione foglio di calcolo?

- **Precisione basata sull'AI** – Sfrutta modelli neurali di traduzione all'avanguardia per conversioni linguistiche contestualmente consapevoli e di alta qualità.
- **Nessuna alterazione della struttura** – Mantiene esattamente come nel file sorgente le formule delle celle, la formattazione condizionale, i grafici e l'ordine dei fogli.
- **Elaborazione multi-foglio in una singola chiamata** – Traduce tutti i fogli di lavoro in una sola richiesta, eliminando la necessità di cicli per foglio.
- **Integrazione cloud senza interruzioni** – Funziona con l'autenticazione di Aspose.Cells Cloud, consentendo pipeline automatizzate in CI/CD, funzioni serverless o back-end aziendali.

## Come utilizzare l'API di traduzione foglio di calcolo con gli SDK

### Specifica dell'API di traduzione foglio di calcolo

La [Specifica dell'API di traduzione foglio di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet) fornisce un'interfaccia di programmazione pubblicamente accessibile per eseguire interazioni REST direttamente da un browser web.

## SDK per API Excel

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendoti di unire un foglio di calcolo in un altro con codice minimo.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.  
I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}