---
title: "Split Text API – Suddividi le celle Excel in colonne | Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Suddivisore di testo Excel – Suddividi il contenuto delle celle in più colonne | Aspose.Cells Cloud"
linktitle: "Suddividi il testo"
type: docs
url: /it/split-text/
keywords: "Aspose, Cells, API di suddivisione testo, Excel, delimitatore, segmentazione testo, API cloud"
description: "Suddividi facilmente il testo delle celle Excel in colonne o righe separate utilizzando Aspose.Cells Cloud. Supporta delimitatori personalizzati, maschere, interruzioni di riga e opzione per mantenere o meno i delimitatori. Inizia subito con curl o SDK in pochi minuti."
weight: 100
---

Suddividi il testo delle celle Excel in più colonne utilizzando regole di segmentazione personalizzate. Suddividi il contenuto per delimitatore e scrivi il risultato in intervalli specificati con l’API Web di Aspose.Cells Cloud per la suddivisione del testo.

## **Introduzione**: Suddividi il testo

L'API per la segmentazione del testo suddivide il contenuto delle celle in celle multiple in base a delimitatori, modelli o interruzioni di riga specificati, scrivendo i risultati in un intervallo di destinazione. Supporta metodi flessibili di suddivisione, output direzionale (in colonne o righe) e opzioni per mantenere i delimitatori—ideale per analizzare dati concatenati, contenuti in stile CSV o testo multilinea in formati strutturati.

- **Suddividi la cella per carattere specifico** – suddividi il contenuto della cella in celle multiple selezionando qualsiasi carattere come delimitatore (virgola, spazio, punto e virgola, ecc.).
- **Suddividi le celle per stringa** – separa le celle utilizzando qualsiasi combinazione di caratteri da te specificata.
- **Suddividi il testo per maschera** – utilizza i caratteri jolly per suddividere il testo in base a un particolare modello, offrendo un metodo ancora più flessibile e potente per dividere il testo.
- **Suddividi il contenuto delle celle per interruzione di riga** – crea una presentazione più organizzata suddividendo per interruzioni di riga.
- **Suddividi le celle in colonne o righe** – scegli se i risultati della suddivisione vengono scritti in colonne o righe consecutive.
- **Rimuovi o mantieni i delimitatori** – decide se i delimitatori vengono rimossi o mantenuti all'inizio o alla fine delle celle risultanti.

## **API SplitText**

**Prerequisiti**: Per utilizzare questa API è necessaria una valid token di accesso Aspose Cloud, e il foglio di calcolo da elaborare deve essere caricato nello storage Aspose Cloud o fornito direttamente nella richiesta. L’API supporta formati di foglio di calcolo comuni come XLSX, XLS, ODS e CSV.

### API Web

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### I parametri di richiesta dell’API **splitText** sono

| Nome parametro                 | Tipo    | Posizione | Obbligatorio? | Predefinito    | Descrizione                                                                                                                                         |
| ------------------------------ | ------- | --------- | ------------- | -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | File    | FormData  | Sì            | —              | Il file del foglio di calcolo da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                               |
| delimiters                     | String  | Query     | No            | —              | Uno o più caratteri delimitatori utilizzati per suddividere il testo all’interno delle celle (es. `","`, `";"`, `Space`, `LineBreak`, `Tab`, `Pipe`, `Custom`). |
| keepDelimitersInResultingCells | Boolean | Query     | No            | false          | Se impostato su `true`, i caratteri delimitatori vengono mantenuti nelle celle risultanti della suddivisione.                                     |
| keepDelimitersPosition         | String  | Query     | No            | None           | Posizione in cui mantenere i delimitatori se `keepDelimitersInResultingCells` è `true`. Opzioni: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`. |
| howToSplit                     | String  | Query     | No            | SplitToColumns | Metodo di segmentazione del testo. Opzioni: `None`, `SplitToColumns`, `SplitToRows`.                                                               |
| outPositionRange               | String  | Query     | Sì            | —              | Intervallo di destinazione in cui verranno scritti i risultati della suddivisione (es. `"D1:F10"`).                                                |
| worksheet                      | String  | Query     | No            | —              | Nome del foglio di calcolo su cui verrà applicata la suddivisione del testo. Se omesso, viene utilizzato il primo foglio di calcolo.              |
| range                          | String  | Query     | No            | —              | Intervallo di celle di origine a cui viene applicata l’operazione di suddivisione (es. `"A1:A10"`). Se omesso, vengono elaborate tutte le celle utilizzate nel foglio. |
| outPath                        | String  | Query     | No            | —              | Percorso della cartella nello storage cloud in cui verrà salvato il foglio di calcolo elaborato. Se omesso, il file viene salvato nella cartella di origine. |
| outStorageName                 | String  | Query     | No            | —              | Nome dello storage cloud in cui verrà salvato il file di output.                                                                                   |
| region                         | String  | Query     | No            | —              | Impostazioni locali per la segmentazione del testo, che possono influenzare l’interpretazione dei delimitatori e la codifica dei caratteri (es. `"en-US"`, `"ja-JP"`). |
| password                       | String  | Query     | No            | —              | Password per aprire un foglio di calcolo protetto da password.                                                                                     |

### **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Codici di errore

- **400 Bad Request** – URI dell’API Aspose.Cells Cloud non valido o parametri malformati.
- **401 Unauthorized** – Token di accesso mancante o non valido (o client-id/secret).
- **404 Not Found** – Il file del foglio di calcolo specificato non può essere accessibile.
- **500 Server Error** – Si è verificato un’anomalia interna durante l’elaborazione del foglio di calcolo.

## Dove utilizzare l’API di suddivisione del testo?

### **Pulizia importazione CSV e file di testo**

Quando si importano dati da sistemi esterni, i campi vengono spesso concatenati in celle singole:

- **Importazioni ERP/CRM** – suddividi `"John Doe;johndoe@email.com;555-1234"` in colonne separate per nome, email e telefono.
- **Esportazioni database** – analizza chiavi combinate come `"ORD-2024-001|Premium|Express"` in ID ordine, livello e metodo di spedizione.
- **Analisi file di log** – suddividi log semistrutturati come `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` per filtrarli.

### **Migrazione di sistemi legacy**

- I vecchi sistemi memorizzano campi multi-valore in celle singole; suddividili per adattarli ai nuovi schemi di database.
- Converti esportazioni da file flat in tabelle Excel normalizzate, pronte per Power BI o Tableau.

### **Pulizia e standardizzazione dei dati**

- **Normalizzazione delimitatori** – converti delimitatori misti (`"A,B;C|D"`) in un formato uniforme utilizzando la suddivisione con delimitatori multipli.
- **Pulizia spazi bianchi** – suddividi per spazi per identificare e rimuovere spazi extra tra le parole.
- **Dati finanziari** – suddividi codici transazione combinati come `"DEP-CHK-3847"` in tipo di transazione, origine e riferimento.
- **Record medici** – analizza dati paziente come `"Smith,Jane_F_1985"` in cognome, nome, genere e anno di nascita.

## Perché utilizzare l’API di suddivisione del testo?

- **Caratteri specifici** – suddividi per qualsiasi singolo carattere (virgola, punto e virgola, tabulazione, spazio).
- **Combinazioni di stringhe** – utilizza delimitatori multi-carattere come `||`, `->` o separatori personalizzati.
- **Interruzioni di riga** – analizza immediatamente celle multilinea in righe separate (indirizzi, commenti, descrizioni).
- **Delimitatori personalizzati** – definisci qualsiasi combinazione di caratteri come delimitatore per formati di dati proprietari.
- **Facile da usare per sviluppatori** – Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate, riduce notevolmente il carico di lavoro di sviluppo.
- **Conveniente** – puoi rimuovere caratteri duplicati senza prima caricare il foglio di calcolo, risparmiando spazio di archiviazione e riducendo i costi.

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText) definiscono un’interfaccia di programmazione accessibile pubblicamente e permettono di effettuare interazioni REST direttamente da un browser web.

### Utilizza gli SDK di Aspose.Cells Cloud

L’utilizzo degli SDK è il modo migliore per accelerare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendoti di implementare semplicemente la suddivisione del testo nelle celle con pochissimo codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l’elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}