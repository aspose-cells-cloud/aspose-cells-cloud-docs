---
title: "Aspose.Cells Cloud Web API – Traduci file di testo con conversione linguistica basata su intelligenza artificiale"
second_title: "Documento"
ArticleTitle: "Come tradurre file di testo utilizzando l'API di traduzione AI di Aspose.Cells Cloud"
linktitle: "Traduci file di testo"
type: docs
url: /it/translate-text-file/
keywords: "Aspose.Cells, API cloud, traduzione AI, traduci file di testo, conversione multilingue, REST PUT, codice linguistico di destinazione, traduzione caricamento file, traduzione testo grezzo, foglio di calcolo AI"
description: "Scopri come utilizzare l'endpoint AI TranslateTextFile di Aspose.Cells Cloud per convertire file di testo in qualsiasi lingua supportata. Supporta sia il caricamento multipart di file che il payload di testo grezzo, conserva la formattazione e restituisce un file tradotto scaricabile."
weight: 100
---

L'endpoint **TranslateTextFile** sfrutta i servizi AI di Aspose.Cells Cloud per tradurre il contenuto di un file di testo in una lingua di destinazione specificata. Supporta due modalità operative: (1) **Modalità caricamento file** – invia un file di testo tramite multipart/form-data e ricevi un file tradotto; (2) **Modalità contenuto diretto** – invia testo grezzo nel corpo della richiesta e ottieni direttamente il testo tradotto. Il servizio conserva le interruzioni di riga e la formattazione originali, aggiunge automaticamente il suffisso "\_translated" al nome del file e restituisce il risultato come flusso scaricabile. Ideale per la traduzione in batch di documenti, l'integrazione in flussi di lavoro multilingue o la traduzione in tempo reale di contenuti generati dagli utenti.

## **API per la traduzione di file di testo**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Posizione | Obbligatorio/opzionale | Descrizione                                                                                                                                                                                                 |
| :------------- | :----- | :-------- | :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | Obbligatorio | FormData               | Il file di testo sorgente da tradurre. Deve essere un file di testo semplice (.txt) o un formato foglio di calcolo supportato. Esempio: carica `document.txt` tramite il campo "file" di multipart/form-data. |
| targetLanguage | String | Obbligatorio | Query                  | Codice linguistico ISO-639-1 della lingua di output desiderata (ad esempio, "es" per spagnolo, "fr" per francese, "de" per tedesco). Il codice è case-insensitive.                                        |
| region         | string | Opzionale    | Query                  | Identificatore regionale del foglio di calcolo che influisce sulla formattazione specifica della localizzazione, come date, numeri e valuta. Valori comuni: "US", "EU", "CN". Se omesso, viene utilizzata l'impostazione regionale originale del foglio di calcolo. |
| password       | String | Opzionale    | Query                  | Password necessaria per aprire file di fogli di calcolo crittografati. Non necessaria per file di testo semplice.                                                                                           |

### **Risposta**

Risposta corretta (200 OK)
Intestazioni:
Content-Type: application/octet-stream // flusso binario del file tradotto
Content-Disposition: attachment; filename="<nome_originale>\_translated.txt"
Content-Length: <dimensione in byte>

Corpo: flusso binario contenente il testo tradotto, che conserva le interruzioni di riga e la formattazione originali.

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato).      |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Dove utilizzare l'API per la traduzione di file di testo?

- **Portali documentali multilingue** – Traduci automaticamente manuali utente o file di aiuto caricati come documenti di testo, fornendo versioni localizzate su richiesta.
- **Sistemi di gestione dei contenuti (CMS)** – Integra in un flusso di lavoro CMS per tradurre post di blog o articoli prima della pubblicazione a un pubblico internazionale.
- **Pipeline di dati aziendali** – Utilizza in processi batch che elaborano grandi quantità di report CSV o TXT, convertendoli nella lingua degli uffici regionali mantenendo la formattazione originale.
- **Piattaforme di supporto clienti** – Traduci in tempo reale ticket o log di chat in testo grezzo in ingresso per supportare gli agenti di supporto che operano in diverse lingue.

## Perché utilizzare l'API per la traduzione di file di testo?

- **Precisione guidata dall'AI** – Sfrutta modelli neurali all'avanguardia per output naturali e contestualmente accurati.
- **Flessibilità di input duplice** – Accetta sia caricamenti di file che payload di testo grezzo, semplificando l'integrazione con applicazioni client eterogenee.
- **Conserva il layout originale** – Mantiene interruzioni di riga, rientri e caratteri speciali, eliminando la necessità di pulizie post-traduzione.
- **Gestione file senza attriti** – Restituisce un file pronto per il download con un suffisso "\_translated" generato automaticamente, riducendo la complessità del codice lato client.

## Come utilizzare l'API per la traduzione di file di testo con gli SDK

### Specifica dell'API per la traduzione di file di testo

La [Specifiche dell'API per la traduzione di file di testo](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile) fornisce un'interfaccia di programmazione pubblicamente accessibile per eseguire interazioni REST direttamente da un browser web.

## SDK per API Excel

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di unire un foglio di calcolo in un altro con poche righe di codice.
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.
I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}

---