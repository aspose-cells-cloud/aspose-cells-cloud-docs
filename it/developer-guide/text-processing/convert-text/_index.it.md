---
title: "Aspose.Cells Cloud Web API - Convertire testo in numeri in Excel e pulire i caratteri speciali"
second_title: "Documento"
ArticleTitle: "Excel Data Cleaner - Converti testo in numeri e rimuovi caratteri indesiderati"
linktitle: "Converti testo"
type: docs
url: /it/convert-text/
keywords: "Aspose.Cells converti testo, testo di Excel in numeri, rimuovi caratteri speciali da Excel, sostituisci interruzioni di riga in Excel, normalizza caratteri accentati, API per la pulizia dei dati Excel"
description: "Converti numeri formattati come testo in valori numerici, sostituisci caratteri e interruzioni di riga indesiderati, e normalizza i caratteri accentati nei file Excel utilizzando l'API Aspose.Cells Cloud."
weight: 100
---

Pulisci i dati Excel convertendo numeri formattati come testo in valori numerici, sostituendo caratteri e interruzioni di riga indesiderati, e normalizzando i caratteri accentati in lettere standard con l'API Aspose.Cells.

## Panoramica

**Converti numeri memorizzati come testo, rimuovi caratteri indesiderati, sostituisci accenti—una sola chiamata, zero formule.**

- **Converti numeri memorizzati come testo in numeri**: Trasforma dati numerici memorizzati come testo in veri numeri, garantendo calcoli accurati e una rappresentazione corretta dei dati.
- **Sostituisci caratteri specifici**: Sostituisci tutte le occorrenze di caratteri specificati nelle celle selezionate in un'unica operazione per standardizzare i dati.
- **Converti interruzioni di riga in spazi, virgole o punti e virgola**: Migliora la leggibilità convertendo le interruzioni di riga in spazi, virgole o punti e virgola, creando una presentazione più organizzata e visivamente accettabile.
- **Sostituisci caratteri accentati**: Se i tuoi dati sono in lingue diverse, puoi sostituire caratteri accentati come “é” o “ü” con le loro controparti non accentate, migliorando coerenza e chiarezza.

## API **ConvertText**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### I parametri della richiesta dell'API **convertText** sono:

| Nome Parametro   | Tipo   | Percorso/Query String/HTTPBody | Descrizione                                                                                                                                                      |
| ---------------- | ------ | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | File   | FormData                       | Il file del foglio di calcolo da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                                             |
| convertTextType  | String | Query                          | Specifica il tipo di conversione di testo da applicare, ad esempio la conversione di numeri formattati come testo in valori numerici o la conversione di caratteri accentati nelle loro forme non accentate. |
| sourceCharacters | String | Query                          | Specifica i caratteri, le stringhe o i pattern da sostituire o rimuovere dal testo (ad esempio: `"é,è,ê"`, `"#N/A"`, `"\\n"` per le interruzioni di riga).       |
| targetCharacters | String | Query                          | Specifica i caratteri o le stringhe di sostituzione che sostituiranno quelli di origine (ad esempio: `"e"` per le lettere accentate, `""` per la rimozione, `" "` per le interruzioni di riga). |
| worksheet        | String | Query                          | _(Opzionale)_ Il nome del foglio di lavoro in cui verrà applicata la conversione del testo. Se omesso, l'operazione verrà applicata al primo foglio di lavoro.   |
| range            | String | Query                          | _(Opzionale)_ L'intervallo di celle in cui verrà applicata la conversione del testo (ad esempio: `"A1:C10"`). Se omesso, l'operazione verrà applicata a tutte le celle utilizzate nel foglio specificato. |
| outPath          | String | Query                          | _(Opzionale)_ Il percorso della cartella nell'archivio cloud dove verrà salvato il foglio di calcolo elaborato. Se omesso, il file verrà salvato nella cartella di origine. |
| outStorageName   | String | Query                          | Il nome dell'archivio cloud in cui verrà salvato il file di output.                                                                                             |
| region           | String | Query                          | _(Opzionale)_ Imposta il locale per le regole di conversione del testo, particolarmente rilevante per la gestione dei caratteri specifici della lingua (ad esempio: `"en-US"`, `"fr-FR"`). |
| password         | String | Query                          | _(Opzionale)_ Se il foglio di calcolo caricato è protetto da password, fornire la password per aprirlo ed elaborarlo.                                           |

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

- **400 Bad Request**: URI dell'API Aspose.Cells Cloud non valido.
- **401 Unauthorized**: Token di accesso non valido o ID client e segreto non validi.
- **404 Not Found**: Il file del foglio di calcolo non è accessibile.
- **500 Server Error**: Si è verificata un’anomalia durante il recupero dei dati di calcolo dal foglio di calcolo.

## Dove utilizzare l’API Convert Text?

- **Correzione del formato numerico**: Converti numeri memorizzati come testo (ad esempio: “123.45”) in un formato numerico adatto per i calcoli.
- **Pulizia dei caratteri speciali**: Rimuovi simboli non necessari, spazi extra o caratteri invisibili dai dati.
- **Gestione delle interruzioni di riga**: Sostituisci le interruzioni di riga nelle celle con spazi o altri delimitatori.
- **Normalizzazione dei caratteri accentati**: Converti le lettere accentate (ad esempio: “é”, “ñ”) in lettere standard (“e”, “n”).
- **Pre-elaborazione dei file CSV**: Standardizza il formato del testo prima di importare file CSV in Excel.

## Perché utilizzare l’API Convert Text?

- **Conversione automatica del formato**: Converti numeri formattati come testo in valori calcolabili in blocco con una singola richiesta.
- **Standardizzazione dei caratteri**: Gestisci in modo uniforme caratteri speciali, segni diacritici e problemi di codifica.
- **Coerenza dei dati**: Assicura che il formato del testo sia completamente uniforme in tutto l’intero insieme di dati.
- **Facile da usare per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e fornendo una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per l'elaborazione del testo, ciò riduce significativamente il carico di lavoro.
- **Conveniente**: Puoi convertire il testo senza caricare preventivamente il foglio di calcolo, risparmiando spazio di archiviazione e riducendo i costi.

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare direttamente interazioni REST da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo migliore per accelerare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendoti di implementare semplicemente la funzionalità Convert Text per le celle con un numero minimo di righe di codice.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
---