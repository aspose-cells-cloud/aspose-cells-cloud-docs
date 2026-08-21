---
title: "Aspose.Cells Cloud Remove Characters Web API – Elimina caratteri personalizzati e sottostringhe da Excel (Short‑Code online)"
second_title: "Documenti"
ArticleTitle: "Pulitore di testo Excel – Elimina caratteri e sottostringhe da un intervallo selezionato"
linktitle: "Rimuovi caratteri"
type: docs
url: /it/remove-characters/
keywords: "Aspose.Cells, rimuovi caratteri, Excel API, pulizia testo, foglio di calcolo"
description: "Rimuovi caratteri personalizzati, set di caratteri e sottostringhe dalle celle Excel in un intervallo selezionato. Elimina il testo in posizioni specifiche usando l'API Aspose.Cells per una pulizia dati precisa."
weight: 100
---

Pulisci i dati Excel eliminando caratteri personalizzati, set di caratteri o sottostringhe da un intervallo selezionato di celle. Rimuovi il testo in posizioni specifiche con l’API Aspose.Cells per una formattazione dati accurata.

## Introduzione

Pulisci e standardizza facilmente i tuoi dati Excel rimuovendo caratteri specifici non desiderati. Il nostro componente aggiuntivo offre diversi metodi mirati per pulire le celle:

- **Rimuovi caratteri personalizzati**  
  Elimina simboli specifici definiti dall’utente. Basta inserire ogni carattere nel campo indicato: il componente aggiuntivo eliminerà immediatamente tutte le relative occorrenze nelle celle selezionate. Ideale per rimuovere delimitatori unici, errori di battitura o simboli speciali.

- **Rimuovi set di caratteri (pulizia in blocco)**
  - **Caratteri non stampabili** – Pulisci i dati da caratteri invisibili che interferiscono con l’analisi e la formattazione (interruzioni di riga, ritorni a capo, tabulazioni e altri caratteri di controllo come ASCII 0‑31, 127, 129, 141, 143, 144, 157).
  - **Caratteri di testo (tutte le lettere)** – Isola numeri e simboli rimuovendo tutte le lettere (A‑Z, a‑z) dall’intervallo selezionato.
  - **Caratteri numerici (tutte le cifre)** – Estrai testo puro eliminando tutte le cifre (0‑9), ideale per pulire nomi di prodotti o descrizioni testuali.
  - **Simboli** – Rimuovi un’ampia gamma di simboli inutili, tra cui quelli matematici (es. ±, √), geometrici (es. ∆, °), tecnici, valutari (es. £, ¢) e simili a lettere (es. ™, ®, ©).
  - **Segni di punteggiatura** – Ottieni testo pulito e privo di punteggiatura eliminando tutti i segni di punteggiatura, come punti, virgole, virgolette e trattini.

- **Rimuovi una sottostringa specifica**  
  Vai oltre la semplice rimozione di singoli caratteri ed elimina intere parole o sequenze di caratteri specifiche. Rimuovi facilmente prefissi, suffissi comuni o qualsiasi frase ridondante nei tuoi dataset.

**Versione 4.0 – Aggiornata il 2024-11-15**

## API RemoveCharacters

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della richiesta

| Nome parametro    | Tipo   | Posizione           | Descrizione                                                                                                                                                                                                                      |
| ----------------- | ------ | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | File   | FormData           | Il file del foglio di calcolo da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                                                                                                              |
| removeTextMethod  | String | Query              | Specifica il metodo di rimozione del testo. Opzioni: `None`, `RemoveCustomCharacter`, `RemoveCharacterSets`, `RemoveSubString`. Il valore predefinito è `None`.                                                               |
| characterSets     | String | Query              | Set di caratteri predefiniti da rimuovere quando è selezionato `RemoveCharacterSets`. Opzioni: `NonPrintingCharacters`, `TextCharacters`, `NumericCharacters`, `Symbols`, `PunctuationMarks`. Più set possono essere combinati separandoli con virgole. |
| removeCustomValue | String | Query              | Carattere/i o sottostringa/e personalizzata/e da rimuovere quando si usa `RemoveCustomCharacter` o `RemoveSubString`.                                                                                                           |
| worksheet         | String | Query _(opzionale)_ | Il nome del foglio di calcolo in cui verrà applicata la rimozione del testo. **Se omesso, l’API elabora il primo foglio del libro.**                                                                                           |
| range             | String | Query _(opzionale)_ | L’intervallo di celle in cui verrà applicata la rimozione del testo (es. `"A1:C10"`). **Se omesso, l’operazione viene applicata a tutte le celle utilizzate nel foglio specificato.**                                         |
| outPath           | String | Query _(opzionale)_ | Percorso della cartella nell’archivio cloud dove verrà salvato il libro elaborato. Se omesso, il file viene salvato nella cartella di origine.                                                                                 |
| outStorageName    | String | Query _(opzionale)_ | Nome dell’archivio cloud in cui verrà salvato il file di output.                                                                                                                                                                |
| region            | String | Query _(opzionale)_ | Imposta la localizzazione per le definizioni dei set di caratteri (es. `"en-US"`, `"ja-JP"`).                                                                                                                                   |
| password          | String | Query _(opzionale)_ | Password per un libro protetto, se richiesta.                                                                                                                                                                                   |

### Risposta

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

- **400 Bad Request** – URI dell’API Aspose.Cells Cloud non valido.
- **401 Unauthorized** – Token di accesso non valido, oppure ID client e segreto errati.
- **404 Not Found** – Il file del foglio di calcolo non è accessibile.
- **500 Server Error** – Si è verificata un’anomalia nel foglio di calcolo durante il recupero dei dati per il calcolo.

## Dove utilizzare l’API Remove Characters?

- **Importazione/esportazione dati** – Pulisci CSV o dati importati rimuovendo caratteri invisibili ed errori di formattazione.
- **Gestione database** – Standardizza codici prodotto, ID e nomi rimuovendo simboli o punteggiatura indesiderati.
- **Analisi finanziaria** – Estrai numeri puri rimuovendo simboli valutari e caratteri testuali.
- **Elaborazione testo** – Rimuovi interruzioni di riga e tabulazioni per un’analisi e reportistica pulita del testo.
- **Gestione inventario** – Pulisci i nomi dei prodotti eliminando prefissi o suffissi ridondanti.

## Perché utilizzare l’API Remove Characters?

- **Risparmia tempo** – Rimuovi in blocco più tipi di caratteri istantaneamente rispetto alla pulizia manuale.
- **Garantisci precisione** – Elimina caratteri nascosti che causano errori di analisi e problemi di formattazione.
- **Standardizza i dati** – Ottieni una formattazione coerente tra dataset e sistemi diversi.
- **Migliora l’analisi** – Ottieni dati puliti e pronti per l’analisi, isolando numeri o testo secondo le esigenze.
- **Risolve errori di importazione** – Rimuovi caratteri problematici che bloccano database e formule.
- **Facile per gli sviluppatori** – Aspose.Cells Cloud fornisce librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido con una documentazione completa. Rispetto alla creazione di soluzioni personalizzate, ciò riduce notevolmente il carico di lavoro.
- **Conveniente** – Rimuovi caratteri senza caricare preventivamente il libro, risparmiando spazio di archiviazione e riducendo i costi.

## Specifica OpenAPI

La [specifica OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters) definisce un’interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK Aspose.Cells Cloud

L’utilizzo degli SDK è il modo migliore per accelerare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, permettendoti di implementare la funzionalità **Remove Characters** per le celle con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}