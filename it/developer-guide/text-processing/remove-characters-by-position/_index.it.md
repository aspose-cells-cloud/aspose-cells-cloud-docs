---
title: "Aspose.Cells Cloud Remove Characters by Position Web API – Elimina testo da posizioni specifiche in Excel"
second_title: "Documento"
ArticleTitle: "Rimuovi caratteri in base alla posizione in Excel – Elimina testo da posizioni specifiche – Shortcode online"
linktitle: "Rimuovi caratteri in base alla posizione"
type: docs
url: /it/remove-characters-by-position/
keywords: "Aspose.Cells Cloud, rimuovi caratteri in base alla posizione, pulizia testo Excel, elimina primi N caratteri, elimina ultimi N caratteri, rimuovi testo prima di un marcatore, rimuovi testo dopo un marcatore, rimozione tra valori"
description: "Utilizza l'API Web di Aspose.Cells Cloud per eliminare caratteri da celle Excel in base alla posizione—rimuovi i primi/ultimi N caratteri o il testo prima/dopo marcatori specifici con alta precisione."
weight: 100
---

Elimina caratteri dalle celle Excel in base alla posizione: rimuovi i primi/ultimi N caratteri oppure elimina il testo prima/dopo marcatori specificati. Pulizia precisa del testo grazie all'API Web di Aspose.Cells Cloud.


## **Introduzione**: Rimuovi caratteri indesiderati in base alla posizione

**Modalità di posizione**

- `theFirstNCharacters` – rimuovi N caratteri dall'inizio
- `theLastNCharacters` – rimuovi N caratteri dalla fine
- `allCharactersBeforeText` – elimina tutto ciò che precede la prima occorrenza della sottostringa fornita
- `allCharactersAfterText` – elimina tutto ciò che segue la prima occorrenza
- `BetweenValues` – rimuovi la sottostringa (e, opzionalmente, i delimitatori stessi) compresa tra due valori definiti dall'utente

**Opzioni**

- `caseSensitive` – determina se le ricerche per `BeforeText`, `AfterText` e `BetweenValues` sono distinte per maiuscole/minuscole

## **API RemoveCharactersByPosition**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della richiesta dell'API **RemoveCharactersByPosition**

| Nome parametro            | Tipo    | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                                                                                                             |
| ------------------------- | ------- | ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet               | File    | FormData                              | Il file del foglio di calcolo da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                                                   |
| Authorization             | String  | Intestazione                          | Token Bearer per l'autenticazione (obbligatorio).                                                                                                                      |
| theFirstNCharacters       | Integer | Query                                 | Numero di caratteri da rimuovere dall'inizio del testo in ciascuna cella selezionata (ad esempio, `3` rimuove i primi 3 caratteri).                                   |
| theLastNCharacters        | Integer | Query                                 | Numero di caratteri da rimuovere dalla fine del testo in ciascuna cella selezionata (ad esempio, `2` rimuove gli ultimi 2 caratteri).                                  |
| allCharactersBeforeText   | String  | Query                                 | Rimuove tutti i caratteri che precedono la stringa di testo specificata in ciascuna cella. Se la stringa appare più volte, la rimozione si basa sulla prima occorrenza. |
| allCharactersAfterText    | String  | Query                                 | Rimuove tutti i caratteri che seguono la stringa di testo specificata in ciascuna cella. Se la stringa appare più volte, la rimozione si basa sulla prima occorrenza.  |
| worksheet                 | String  | Query                                 | _(Opzionale)_ Il nome del foglio di lavoro in cui verrà applicata la rimozione dei caratteri. Se omesso, l'operazione viene applicata al primo foglio di lavoro.        |
| range                     | String  | Query                                 | _(Opzionale)_ L'intervallo di celle in cui verrà applicata la rimozione dei caratteri (ad esempio, `"A1:C10"`). Se omesso, l'operazione viene applicata a tutte le celle utilizzate nel foglio di lavoro specificato. |
| outPath                   | String  | Query                                 | _(Opzionale)_ Il percorso della cartella nello storage cloud in cui verrà salvato il foglio di calcolo elaborato. Se omesso, il file viene salvato nella cartella di origine. |
| outStorageName            | String  | Query                                 | Il nome dello storage cloud in cui verrà salvato il file di output.                                                                                                    |
| region                    | String  | Query                                 | _(Opzionale)_ Imposta la localizzazione per la gestione del testo, particolarmente rilevante per le posizioni dei caratteri e la codifica specifiche della lingua (ad esempio, `"en-US"`, `"zh-CN"`). |
| password                  | String  | Query                                 | _(Opzionale)_ Se il foglio di calcolo caricato è protetto da password, fornire la password per aprirlo ed elaborarlo.                                                  |

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

- **200 OK** – La richiesta ha avuto successo e il file elaborato viene restituito.
- **400 Bad Request**: URI dell'API Aspose.Cells Cloud non valido.
- **401 Unauthorized**: Token di accesso non valido oppure ID client e segreto non validi.
- **404 Not Found**: Il file del foglio di calcolo non è accessibile.
- **500 Server Error**: Si è verificato un'anomalia durante il recupero dei dati di calcolo per il foglio di calcolo.

## Dove utilizzare l'API Remove Characters by Position?

- **Standardizzazione dei dati**: Pulisci i codici prodotto (rimuovi zeri iniziali o suffissi), i numeri di telefono (rimuovi i prefissi internazionali)
- **Estrazione di testo**: Estrai informazioni chiave dai file di log (rimuovi timestamp o prefissi)
- **Elaborazione di file**: Organizza i nomi dei file (rimuovi prefissi uniformi o suffissi di data)
- **Parsing dei dati**: Elabora testo strutturato (estrai contenuto tra parentesi o marcatori specifici)
- **Gestione database**: Pulisci i dati importati (rimuovi caratteri di intestazione/piede in formato fisso)

## Perché utilizzare l'API Remove Characters by Position?

- **Precisa ed efficiente**: La cancellazione diretta in base alla posizione elimina la necessità di complesse espressioni regolari.
- **Configurazione flessibile**: Cinque modalità di posizionamento più un'opzione per la distinzione maiuscole/minuscole coprono scenari diversificati.
- **Elaborazione in batch**: Pulisci intere colonne con una singola chiamata, aumentando l'efficienza fino a 10 volte.
- **Parsing intelligente**: Gestisci facilmente l'estrazione di contenuti tra due delimitatori.
- **Adatto agli sviluppatori**: Aspose.Cells Cloud fornisce SDK per diversi linguaggi, accelerando lo sviluppo e offrendo una documentazione completa. Rispetto alla creazione di logiche personalizzate per l'elaborazione del testo, ciò riduce notevolmente il carico di lavoro.
- **Conveniente**: I caratteri possono essere rimossi senza caricare preventivamente il foglio di calcolo, risparmiando spazio di archiviazione e riducendo i costi.

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK rappresenta il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendoti di implementare semplicemente la rimozione dei caratteri in base alla posizione nelle celle con un codice minimo.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web di Aspose.Cells Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---