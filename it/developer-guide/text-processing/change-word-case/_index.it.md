---
title: "Aspose.Cells Cloud – Modifica la capitalizzazione delle parole (Maiuscolo, Minuscolo, Iniziali Maiuscole, Frase)"
ArticleTitle: "Convertitore di maiuscole/minuscole Excel – Maiuscolo, Minuscolo, Iniziali Maiuscole e Frase"
linktitle: "Capitalizzazione delle parole"
type: docs
url: /change-word-case/
keywords: "API per la modifica della capitalizzazione delle parole, Aspose.Cells, conversione maiuscole/minuscole Excel, maiuscolo, minuscolo, iniziali maiuscole, frase, formattazione del testo"
description: "Converti facilmente la capitalizzazione del testo nei file Excel utilizzando l'API Aspose.Cells Cloud. Supporta Maiuscolo, Minuscolo, Iniziali Maiuscole e Frase. Ottieni esempi di codice in C#, Java, Python e altro."
weight: 100
---

## **Modifica la capitalizzazione delle parole**

Utilizza l'API Web Aspose.Cells Cloud per convertire istantaneamente la capitalizzazione del testo nel tuo foglio di calcolo—passa da maiuscolo a minuscolo, da iniziali maiuscole (prima lettera di ogni parola maiuscola) o da frase (prima lettera di ogni frase maiuscola) in un intervallo selezionato. Vengono interessati solo le celle contenenti stringhe; numeri, valori booleani, errori e celle vuote vengono ignorati. Formule, formattazione e convalida dati rimangono invariate.

- **UpperCase** – ogni carattere maiuscolo.
- **LowerCase** – ogni carattere minuscolo.
- **ProperCase** – prima lettera di ogni parola maiuscola, il resto minuscolo.
- **SentenceCase** – prima lettera di ogni frase maiuscola, il resto minuscolo.

<img src="images/result.png" alt="Screenshot prima/dopo la conversione della capitalizzazione" width="800" height="450" />

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```
### Parametri della richiesta per l'API **UpdateWordCase**

| Nome Parametro | Tipo   | Posizione | Descrizione                                                                                                                                                           |
| :------------- | :----- | :-------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet    | File   | FormData  | Il file del foglio di calcolo da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                                                 |
| wordCaseType   | String | Query     | Specifica il tipo di conversione della capitalizzazione del testo: `UpperCase`, `LowerCase`, `ProperCase` o `SentenceCase`.                                         |
| worksheet      | String | Query     | _(Opzionale)_ Il nome del foglio di calcolo in cui verrà applicata la conversione della capitalizzazione. Se omesso, l'operazione viene applicata al primo foglio del workbook. |
| range          | String | Query     | _(Opzionale)_ L'intervallo di celle in cui verrà applicata la conversione della capitalizzazione (ad esempio, `"A1:C10"`). Se omesso, l'operazione viene applicata a tutte le celle utilizzate nel foglio specificato. |
| outPath        | String | Query     | _(Opzionale)_ Il percorso della cartella nello spazio di archiviazione cloud dove verrà salvato il workbook elaborato. Se omesso, il file viene salvato nella cartella di origine. |
| outStorageName | String | Query     | Il nome dello spazio di archiviazione cloud in cui verrà salvato il file di output.                                                                                 |
| region         | String | Query     | _(Opzionale)_ Imposta la localizzazione per le regole di conversione della capitalizzazione del testo, particolarmente rilevante per la capitalizzazione specifica della lingua (ad esempio, `"en-US"`, `"tr-TR"`). |
| password       | String | Query     | _(Opzionale)_ Se il foglio di calcolo caricato è protetto da password, fornire la password per aprirlo e elaborarlo.                                                |

### Risposta

In caso di esito positivo, il servizio restituisce **200 OK** (o **202 Accepted**) con un payload JSON contenente il flusso binario del workbook elaborato.

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

- **400 Bad Request** – URI dell'API Aspose.Cells Cloud non valido.
- **401 Unauthorized** – Token di accesso non valido o credenziali client errate.
- **404 Not Found** – Il file del foglio di calcolo non è accessibile.
- **500 Server Error** – Si è verificato un errore interno durante l'elaborazione del foglio di calcolo.

## Dove utilizzare l'API per la modifica della capitalizzazione delle parole?

### Pulizia e standardizzazione dei dati

- **Gestione dei dati dei clienti** – Standardizzare la capitalizzazione dei nomi dei clienti e delle informazioni sugli indirizzi (ad esempio, `john doe` → `John Doe`).
- **Elaborazione del catalogo prodotti** – Standardizzare i titoli dei prodotti e i testi descrittivi (ad esempio, `IPHONE 15 PRO` → `iPhone 15 Pro`).
- **Generazione di report finanziari** – Normalizzare i nomi delle voci e i campi descrittivi nei bilanci finanziari.

### Integrazione di dati da fonti multiple

- **ETL nel data warehouse** – Standardizzare il formato del testo durante il caricamento di dati da vari sistemi.
- **Ricezione dati tramite API** – Gestire i dati restituiti da API esterne con capitalizzazione non coerente.
- **Fusione di dati tra reparti** – Standardizzare il formato del testo nei report Excel provenienti da reparti diversi.

### Sistema di gestione dei contenuti

- **Rilasci di notizie automatizzati** – Formattare automaticamente titoli e contenuti delle notizie (regole di capitalizzazione per i titoli).
- **Generazione della documentazione dei prodotti** – Garantire coerenza nella formattazione dei termini della documentazione tecnica.
- **Manutenzione della knowledge base** – Standardizzare il formato del testo delle FAQ e dei documenti di aiuto.

### Integrazione di applicazioni aziendali

- **Integrazione con sistemi CRM** – Formattare automaticamente nomi e informazioni aziendali durante l’importazione/esportazione dei dati dei clienti.
- **Elaborazione dati ERP** – Standardizzare i campi chiave come le descrizioni dei materiali e i nomi dei fornitori.
- **Sistema di gestione delle risorse umane** – Standardizzare le informazioni sui dipendenti e i titoli di ruolo.

### Elaborazione batch di documenti

- **Preparazione di documenti legali** – Elaborazione in batch dei formati delle clausole in contratti e accordi.
- **Generazione di materiali di marketing** – Standardizzare i formati dei testi pubblicitari e dei modelli di email.
- **Formattazione di articoli accademici** – Standardizzare i requisiti di formattazione per le referenze e i titoli.

### Elaborazione in tempo reale dei dati

- **Convalida dei dati inseriti dall’utente** – Formattazione in tempo reale dei dati dei moduli inviati dagli utenti.
- **Risposte dei chatbot** – Standardizzazione del formato del testo per le risposte generate automaticamente.
- **Generazione istantanea di report** – Creazione dinamica di report aziendali uniformemente formattati.

### Internazionalizzazione e localizzazione

- **Elaborazione di dati multilingua** – Gestione delle differenze nelle regole di capitalizzazione per i testi in varie lingue.
- **Preparazione del contenuto localizzato** – Preparare contenuti localizzati formattati per diverse regioni.
- **Gestione dei progetti di traduzione** – Garantire coerenza nel formato del testo prima e dopo la traduzione.

## Perché utilizzare l'API per la modifica della capitalizzazione delle parole?

- **Facile da utilizzare per gli sviluppatori** – Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e una documentazione completa. Rispetto alla creazione di soluzioni personalizzate, ciò riduce significativamente il carico di lavoro di sviluppo.
- **Conveniente** – Puoi modificare la capitalizzazione delle parole senza caricare preventivamente il workbook, risparmiando spazio di archiviazione e riducendo i costi.

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase) definiscono un'interfaccia di programmazione accessibile pubblicamente e ti consentono di effettuare direttamente interazioni REST da un browser web.

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo degli SDK è il modo migliore per velocizzare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendoti di implementare semplicemente **UpdateWordCase** per le celle con pochissimo codice. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---