---
title: "Aspose.Cells Cloud Add Text API – Aggiungi testo a più celle Excel contemporaneamente – Inserisci prefissi, suffissi e etichette"
second_title: "Documento"
ArticleTitle: "Inserimento massivo di testo per Excel – Aggiungi prefissi, suffissi e testo personalizzato alle celle – Guida passo dopo passo"
linktitle: "AddText"
type: docs
url: /it/add-text/
keywords: "Aspose Cells API, aggiungi testo Excel, inserimento massivo di testo, prefisso suffisso Excel, sostituisci testo foglio elettronico, automazione Excel, API foglio elettronico cloud"
description: "Inserisci prefissi, suffissi o etichette personalizzate in molte celle Excel con una sola chiamata tramite Aspose.Cells Cloud. Scegli di inserire all’inizio, alla fine, prima o dopo un determinato testo. Supporta intervalli, fogli di lavoro e gestione celle vuote."
weight: 100
---

Inserisci testo in più celle Excel in un’unica operazione. Aggiungi prefissi, suffissi, etichette o caratteri personalizzati all’inizio, alla fine o prima/dopo un testo specifico all’interno delle celle utilizzando l’API Aspose.Cells.

## Panoramica

Inserimento massivo con una sola chiamata di prefissi, suffissi o stringhe ancorate in ogni cella di un intervallo target—nessuna formula, nessuna colonna di supporto.

- Inserisci testo personalizzato in **qualsiasi posizione** all’interno di ogni cella

| Valore           | Descrizione                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------ |
| `None`           | Sostituisci il contenuto originale                                                               |
| `AtTheBeginning` | Inserisci all’inizio (prefisso)                                                                  |
| `AtTheEnd`       | Inserisci alla fine (suffisso)                                                                   |
| `BeforeText`     | Inserisci **prima** della prima occorrenza di `selectText`; salta se non trovata                 |
| `AfterText`      | Inserisci **dopo** la prima occorrenza di `selectText`; salta se non trovata                     |

- Quattro modalità di posizionamento: prefisso, suffisso, prima/dopo una sottostringa.
- Salta le celle vuote per evitare disordine.
- L’API modifica solo i valori di **tipo stringa**; numeri, booleani e formule vengono prima convertiti in testo.
- **Celle vuote**
  - `skipEmptyCells = true` → le celle vuote vengono saltate.
  - `skipEmptyCells = false` → alle celle vuote viene aggiunto il testo (la cella diventa di tipo testo).

- **Ancora non trovata**: Quando `position = BeforeText | AfterText` e `selectText` **non esiste**, il valore della cella rimane invariato.

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l’autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### I parametri della richiesta dell’API **AddText** sono

| Nome parametro | Tipo    | Percorso / Stringa query / Corpo HTTP | Descrizione                                                                                                                                              | Obbligatorio |
| :------------- | :------ | :------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------- |
| Spreadsheet    | File    | FormData                              | Il file del foglio elettronico da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                                   | Sì           |
| text           | String  | Query                                 | Il contenuto testuale da aggiungere alle celle specificate nel foglio elettronico.                                                                       | Sì           |
| position       | String  | Query                                 | Specifica dove inserire il testo rispetto al contenuto esistente della cella. Opzioni: `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`. | Sì           |
| selectText     | String  | Query                                 | _(Opzionale)_ Se fornito, il testo verrà aggiunto solo alle celle che contengono esattamente questa sottostringa. Usato in combinazione con `position`. | No           |
| skipEmptyCells | Boolean | Query                                 | Se `true`, le celle vuote vengono saltate; se `false`, il testo viene aggiunto alle celle vuote.                                                        | No           |
| worksheet      | String  | Query                                 | _(Opzionale)_ Il nome del foglio di lavoro in cui verrà aggiunto il testo. Se omesso, l’operazione si applica al primo foglio di lavoro per impostazione predefinita. | No           |
| range          | String  | Query                                 | _(Opzionale)_ L’intervallo di celle in cui verrà aggiunto il testo (es. `"A1:C10"`). Se omesso, l’operazione si applica a tutte le celle usate nel foglio specificato. | No           |
| outPath        | String  | Query                                 | _(Opzionale)_ Il percorso della cartella nell’archivio cloud dove verrà salvato il foglio di lavoro elaborato. Se omesso, il file viene salvato nella cartella di origine. | No           |
| outStorageName | String  | Query                                 | Il nome dell’archivio cloud in cui verrà salvato il file di output.                                                                                      | No           |
| region         | String  | Query                                 | _(Opzionale)_ Imposta il locale per la formattazione di numeri, date e valute nel file di output (es. `"en-US"`, `"zh-CN"`, `"de-DE"`).                   | No           |
| password       | String  | Query                                 | _(Opzionale)_ Se il foglio elettronico caricato è protetto da password, fornire la password per aprirlo e elaborarlo.                                   | No           |

**Esempio cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Report&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
```

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

| Codice | Descrizione |
| ------ | ----------- |
| **400** Bad Request | URI non valido dell’API Aspose.Cells Cloud o parametri obbligatori mancanti. |
| **401** Unauthorized | Token di accesso non valido o ID client e secret non validi. |
| **404** Not Found | Il file del foglio elettronico non è accessibile. |
| **500** Server Error | Il foglio elettronico ha riscontrato un’anomalia durante il recupero dei dati per il calcolo. |

## Dove utilizzare l’API Aggiungi testo per fogli elettronici?

- **Etichettatura dinamica dei report**: Aggiungi titoli dinamici, tag di data o note a fogli di stato finanziario e report di vendita generati automaticamente.
- **Acquolina batch con watermark**: Aggiungi loghi aziendali, watermark di riservatezza o informazioni sulla versione a un lotto di file Excel.
- **Compilazione automatica di modelli**: Compila automaticamente nomi clienti, importi e altri testi in posizioni designate di modelli di contratti o fatture.
- **Etichettatura per classificazione dati**: Aggiungi automaticamente tag di classificazione o etichette di stato (es. “In revisione”, “Approvato”) alle righe di dati in base ai risultati dell’analisi.
- **Annotazione della qualità dei dati**: Aggiungi note per dati problematici durante la pulizia dei dati.
- **Formattazione testo in batch**: Aggiungi in modo uniforme prefissi o suffissi a nomi di prodotti o clienti.

## Perché utilizzare l’API Aggiungi testo per fogli elettronici?

- **Aggiunta di testo in batch**: Aggiungi testo a centinaia di celle o file contemporaneamente, risparmiando fino al 95% del tempo rispetto al lavoro manuale.
- **Controllo preciso della posizione**: Supporta l’inserimento accurato del testo in sei posizioni, tra cui l’inizio, la fine o prima/dopo un testo specifico all’interno di una cella.
- **Gestione intelligente condizionale**: Decidi se aggiungere il testo in base al fatto che una cella sia vuota o contenga testo specifico.
- **Supporto per strategie multi-posizione**:
  - `AtTheBeginning`: Aggiungi lo stesso testo prima del contenuto di tutte le celle selezionate.
  - `AtTheEnd`: Aggiungi testo dopo il contenuto di tutte le celle selezionate.
  - `BeforeText` / `AfterText`: Aggiungi testo solo prima o dopo celle che contengono testo specifico.
  - `None`: Sostituisci il contenuto originale.
- **Controllo preciso dell’intervallo**: Permette di specificare fogli di lavoro o intervalli di celle particolari per le operazioni.
- **Opzione di salto condizionale**: Supporta il salto delle celle vuote per evitare aggiunte di testo non necessarie.
- **Facile da usare per sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e dotate di documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering di grafici, questo riduce notevolmente il carico di sviluppo.
- **Conveniente economicamente**: Puoi aggiungere testo in una cella senza dover prima caricare il foglio di lavoro, risparmiando spazio di archiviazione e riducendo i costi.

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText) definiscono un’interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L’uso dell’SDK rappresenta il modo migliore per velocizzare lo sviluppo. L’SDK gestisce i dettagli sottostanti, consentendoti di implementare semplicemente l’aggiunta di testo alle celle con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}
---