---
title: "Aspose.Cells Cloud Remove Duplicate Substrings Web API - Rimuovi i sottotesti duplicati in Excel"
second_title: "Documento"
ArticleTitle: "Rimuovi sottotesti duplicati in Excel – Pulisci il testo ripetuto nelle celle"
linktitle: "Rimuovi i sottotesti duplicati"
type: docs
url: /remove-duplicate-substrings/
keywords: "Aspose.Cells, sottotesti duplicati, API Excel, pulizia del testo, cloud"
description: "Rimuovi i sottotesti duplicati dalle celle Excel tramite l'API Aspose.Cells Cloud, preservando la formattazione e la convalida."
weight: 100
---

Rimuovi i sottotesti duplicati dalle celle Excel con un rilevamento intelligente. Mantieni intatta la formattazione originale ed elimina il testo ridondante utilizzando l'API di deduplicazione di Aspose.Cells.

## **Introduzione**: Rimuovi i caratteri indesiderati con precisione

L'API Repeat Substring Cleaner rimuove i sottotesti duplicati all'interno delle singole celle di un intervallo Excel, preservando la formattazione delle celle, la convalida dei dati e le altre strutture del foglio di calcolo. Elabora ogni cella in modo indipendente, mantenendo soltanto la prima occorrenza di ciascun sottotesto duplicato.

### **Opzioni per l'origine dati**

| Campo        | Tipo   | Obbligatorio | Descrizione                                      |
| ------------ | ------ | ------------ | ------------------------------------------------ |
| `workbook`   | file   | Sì           | File di foglio di calcolo Excel (.xlsx, .xlsm)  |
| `range`      | string | Sì           | Intervallo di destinazione da elaborare (es. "A1:D100", "Foglio1!A:D") |

### **Opzioni per i delimiter**

| Campo                              | Tipo    | Valore predefinito | Descrizione                                                                                                                                               |
| ---------------------------------- | ------- | ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                       | string  | `"preset"`         | Opzioni: `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break` oppure una stringa personalizzata di delimiter (caratteri multipli vengono considerati un insieme) |
| `treatConsecutiveDelimitersAsOne` | boolean | `false`            | Unisci i delimiter adiacenti in un unico separatore                                                                                                      |
| `caseSensitive`                    | boolean | `false`            | Determina se il confronto è sensibile alle maiuscole/minuscole. Quando impostato su `false`, la distinzione tra maiuscole e minuscole viene ignorata durante il rilevamento dei duplicati. |

## **API RemoveDuplicateSubstrings**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### I parametri della richiesta dell'API **RemoveDuplicateSubstrings** sono:

| Nome del parametro              | Tipo    | Percorso/QueryString/Corpo HTTP | Descrizione                                                                                                                                                                       |
| :------------------------------ | :------ | :---------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                     | File    | FormData                      | Il file di foglio di calcolo da elaborare. I formati supportati includono XLSX, XLS, ODS, CSV, ecc.                                                                              |
| delimiters                      | String  | Query                         | Specifica uno o più caratteri di delimiter utilizzati per dividere il contenuto delle celle in sottotesti, al fine di rilevare e rimuovere i duplicati. Possono essere specificati più delimiter (es. `",;"`). |
| treatConsecutiveDelimitersAsOne | Boolean | Query                         | Quando impostato su `true`, i caratteri delimiter consecutivi vengono considerati come un singolo separatore. Quando impostato su `false`, ogni delimiter viene elaborato individualmente. |
| caseSensitive                   | Boolean | Query                         | Quando impostato su `true`, il rilevamento dei duplici considera la distinzione tra maiuscole e minuscole (es. "Testo" ≠ "testo"). Quando impostato su `false`, tale distinzione viene ignorata durante il confronto dei duplicati. |
| worksheet                       | String  | Query                         | _(Facoltativo)_ Il nome del foglio di lavoro in cui verrà applicata la rimozione dei sottotesti duplicati. Se omesso, l'operazione viene applicata al primo foglio di lavoro.       |
| range                           | String  | Query                         | _(Facoltativo)_ L'intervallo di celle in cui verrà applicata la rimozione dei sottotesti duplicati (es. `"A1:C10"`). Se omesso, l'operazione viene applicata a tutte le celle utilizzate nel foglio di lavoro specificato. |
| outPath                         | String  | Query                         | _(Facoltativo)_ Il percorso della cartella nell'archivio cloud in cui verrà salvato il foglio di calcolo elaborato. Se omesso, il file viene salvato nella cartella di origine.        |
| outStorageName                  | String  | Query                         | Il nome dell'archivio cloud in cui verrà salvato il file di output.                                                                                                               |
| region                          | String  | Query                         | _(Facoltativo)_ Imposta il locale per l'elaborazione del testo, il quale può influenzare l'interpretazione dei delimiter e le regole relative alla distinzione tra maiuscole e minuscole per alcune lingue (es. `"en-US"`, `"tr-TR"`). |
| password                        | String  | Query                         | _(Facoltativo)_ Se il foglio di calcolo caricato è protetto da password, fornire la password per aprirlo ed elaborarlo.                                                            |

**Esempio di richiesta (cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
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

### **Codici di stato**

| Codice | Significato                         | Descrizione                                                                                       |
|--------|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 200    | OK                                  | La richiesta è andata a buon fine e il foglio di calcolo elaborato viene restituito.             |
| 202    | Accettata                           | La richiesta è stata accettata per l'elaborazione asincrona.                                     |
| 400    | Richiesta non valida                | La richiesta è malformata o contiene parametri non validi.                                        |
| 401    | Non autorizzata                     | L'autenticazione non è riuscita o il token è mancante/non valido.                                 |
| 404    | Non trovata                         | Il foglio di calcolo o la risorsa specificata non è stato trovato.                                |
| 500    | Errore interno del server           | Si è verificato un errore imprevisto lato server.                                                |

## Dove utilizzare l'API Remove Duplicate Substrings?

- **Scenari di pulizia e standardizzazione dei dati**: Pulire etichette come `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.
- **Dati tecnici e operativi**: Pulire le voci di log con codici di errore ripetuti, rimuovere identificatori di bin/rack duplicati, ecc.
- **Gestione di contenuti e media**: Deduplicare tag sulle competenze, rimuovere voci di certificazione ridondanti.

## Perché utilizzare l'API Remove Duplicate Substrings?

- **Automatizza le attività manuali**: Elimina la noia della modifica manuale e riduce gli errori umani.  
- **Preserva l’integrità dei dati**: Colori delle celle, caratteri, bordi e formattazione condizionale rimangono invariati; i menu a discesa e le regole di convalida vengono conservate.  
- **Elaborazione flessibile**: Indipendente dai delimiter, con controllo opzionale sulla sensibilità alle maiuscole/minuscole e protezione delle intestazioni.  
- **Facile per gli sviluppatori**: Aspose.Cells Cloud fornisce librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido grazie a una documentazione completa.  
- **Conveniente economicamente**: L'operazione viene eseguita nel cloud, evitando la necessità di memorizzare localmente file intermedi.  

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

### Utilizza gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo migliore per accelerare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendoti di implementare semplicemente la rimozione dei sottotesti duplicati nelle celle con un codice minimo.Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

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
---