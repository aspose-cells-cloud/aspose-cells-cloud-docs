---
title: "Aspose.Cells Cloud Text Trimming Web API - Rimuovi spazi extra e interruzioni di riga"
second_title: "Documento"
ArticleTitle: "Pulitore di dati Excel - Ritaglia automaticamente caratteri, spazi e interruzioni di riga – Online, con short-code"
linktitle: "Ritaglia caratteri"
type: docs
url: /it/trim-character/
keywords: "Excel, ritaglio testo, rimozione spazi, interruzioni di riga, Aspose.Cells, pulizia dati, foglio elettronico, normalizzazione formattazione celle"
description: "Ritaglia spazi extra, interruzioni di riga e caratteri indesiderati dalle celle Excel con l'API di Aspose.Cells Cloud. Assicura dati nei fogli elettronici puliti e coerenti."
weight: 100
---

Ritaglia automaticamente caratteri non necessari, spazi extra e interruzioni di riga dalle celle Excel utilizzando l'API di Aspose.Cells per il ritaglio dei caratteri. Pulisci le voci dei dati e mantieni una formattazione coerente in tutti i tuoi fogli elettronici.

## **Panoramica**

- **Ritaglia gli spazi iniziali e finali**
  - Rimuovi gli spazi extra all'inizio e alla fine del testo
  - Migliora l'ordine visivo e la leggibilità dei dati
- **Elaborazione di spazi extra tra le parole**
  - Elimina spazi extra tra le parole
  - Risolvi i problemi di formattazione causati da dati provenienti da più fonti

- **Spazi speciali rimossi**
  - Rimuovi esplicitamente gli spazi di non interruzione
  - Garantisci l'accuratezza e la coerenza dei dati

- **Gestione delle interruzioni di riga**
  - Rimuovi interruzioni di riga extra o tutte quelle presenti
  - Mantieni il contenuto delle celle organizzato e dallo stile professionale

## **API TrimCharacter**

Prima di chiamare l'API, assicurati di avere un account Aspose Cloud valido, un `client_id`/`client_secret` e un token di accesso con l’ambito **Cells**.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della richiesta dell’API **trimCharacter**

| Nome parametro          | Tipo    | Percorso/Query string/HTTPBody | Descrizione                                                                                                                                                         |
| :---------------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet             | File    | FormData                   | Il file del foglio elettronico da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                                               |
| trimContent             | String  | Query                      | Specifica i caratteri o le stringhe particolari da ritagliare dal contenuto delle celle. Può essere un singolo carattere, più caratteri o un pattern personalizzato. |
| trimLeading             | Boolean | Query                      | Se `true`, rimuove i caratteri specificati dall'inizio del contenuto di ogni cella.                                                                                |
| trimTrailing            | Boolean | Query                      | Se `true`, rimuove i caratteri specificati dalla fine del contenuto di ogni cella.                                                                                 |
| trimSpaceBetweenWordTo1 | Boolean | Query                      | Se `true`, riduce gli spazi multipli consecutivi tra le parole a un singolo spazio all'interno di ogni cella.                                                       |
| trimNonBreakingSpaces   | Boolean | Query                      | Se `true`, rimuove i caratteri di spazio di non interruzione (Unicode U+00A0) dal contenuto della cella.                                                           |
| removeExtraLineBreaks   | Boolean | Query                      | Se `true`, riduce le interruzioni di riga multiple consecutive a una singola interruzione di riga all'interno di ogni cella.                                      |
| removeAllLineBreaks     | Boolean | Query                      | Se `true`, rimuove tutti i caratteri di interruzione di riga dal contenuto della cella.                                                                            |
| worksheet               | String  | Query                      | _(Opzionale)_ Il nome del foglio di calcolo su cui verrà applicato il ritaglio del testo. Se omesso, l'operazione viene applicata al primo foglio.                 |
| range                   | String  | Query                      | _(Opzionale)_ L'intervallo di celle su cui verrà applicato il ritaglio del testo (ad es. `"A1:C10"`). Se omesso, l'operazione viene applicata a tutte le celle usate nel foglio specificato. |
| outPath                 | String  | Query                      | _(Opzionale)_ Il percorso della cartella nell'archivio cloud dove verrà salvato il foglio elettronico elaborato. Se omesso, il file viene salvato nella cartella di origine. |
| outStorageName          | String  | Query                      | Il nome dell'archivio cloud dove verrà memorizzato il file di output.                                                                                               |
| region                  | String  | Query                      | _(Opzionale)_ Imposta il locale per l'elaborazione del testo, che può influenzare la gestione di spazi e interruzioni di riga per lingue specifiche (ad es. `"en-US"`, `"ar-SA"`). |
| password                | String  | Query                      | _(Opzionale)_ Se il foglio elettronico caricato è protetto da password, fornisci la password per aprirlo e elaborarlo.                                             |

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

**Esempio di esito positivo (HTTP 200):** L'API restituisce un flusso di file contenente il foglio elettronico ritagliato.

### Codici di errore

- **400 Bad Request**: URI dell'API Aspose.Cells Cloud non valido.
- **401 Unauthorized**: Token di accesso non valido. Oppure client ID o client secret non validi.
- **404 Not Found**: File del foglio elettronico non accessibile.
- **500 Server Error**: Si è verificata un'anomalia nel recupero dei dati di calcolo del foglio elettronico.

## Dove utilizzare l’API di ritaglio dei caratteri?

- **Normalizzazione dell'input utente**: Pulisci i dati delle tabelle inserite manualmente, rimuovendo spazi e interruzioni di riga in eccesso.
- **Manutenzione del database clienti**: Pulisci spazi ridondanti e problemi di formattazione nei nomi, indirizzi e dati di contatto dei clienti.
- **Pulizia automatica dei report**: Pulisci il formato della fonte dati prima di generare report automatici.
- **Preparazione alla migrazione dei dati**: Risolvi i problemi di formattazione prima della migrazione dei dati verso un nuovo sistema.

## Perché utilizzare l’API di ritaglio dei caratteri?

- **Riduzione dei costi di manodopera**: Elimina gli sforzi manuali dispendiosi in termini di tempo per la pulizia dei dati.
- **Riduzione dei costi legati agli errori**: Evita errori di analisi causati da problemi di formattazione.
- **Pagamento in base all'uso**: Nessuna tariffa fissa, viene addebitato solo il throughput effettivo.
- **Nessun investimento in infrastrutture**: Nessuna necessità di mantenere server o software.
- **Supporto multi-formato**: Supporta l’elaborazione di più formati come XLSX, XLS, CSV, ODS, ecc.
- **Facile da usare per sviluppatori**: Aspose.Cells Cloud offre SDK in diversi linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering di grafici, ciò riduce significativamente il carico di sviluppo.
- **Conveniente**: Puoi rimuovere i caratteri doppi senza caricare preventivamente il foglio elettronico, risparmiando spazio di archiviazione e riducendo i costi.

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter) definiscono un'interfaccia di programmazione accessibile pubblicamente e ti consentono di effettuare direttamente interazioni REST da un browser web.

### Utilizza gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK è il modo migliore per velocizzare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendoti di implementare facilmente il ritaglio dei caratteri nelle celle con un numero minimo di righe di codice.
Consulta l’<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">archivio GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}