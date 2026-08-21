---
title: "Rimuovi sottostringhe duplicate in foglio di calcolo remoto"
ArticleTitle: "Rimuovi sottostringhe duplicate in foglio di calcolo remoto – Aspose.Cells Cloud API"
second_title: "Documenti"
linktype: "Rimuovi sottostringhe duplicate in foglio di calcolo remoto"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, Rimuovi sottostringhe duplicate, API"
description: "API per individuare e rimuovere sottostringhe ripetute all'interno delle celle di un intervallo specificato in un foglio di calcolo."
weight: 1
---

## Il servizio web Aspose.Cells Cloud per rimuovere sottostringhe duplicate in fogli di calcolo remoti

Individua e rimuove sottostringhe ripetute in ogni cella dell'intervallo selezionato, utilizzando delimitatori definiti dall'utente o predefiniti, preservando formule, formattazione e convalida dati.

**Come vengono rilevate le duplicazioni**  
1. Ogni valore di cella viene suddiviso in sottostringhe mediante i delimitatori scelti.  
2. Lo strumento confronta le sottostringhe **all’interno della stessa cella** e conserva soltanto la **prima occorrenza** di ciascuna sottostringa duplicata.  
3. Le sottostringhe pulite vengono nuovamente unite utilizzando gli stessi delimitatori e scritte nuovamente nella cella.  

**Opzioni per i delimitatori**  
- Elenco predefinito: virgola, punto e virgola, spazio, tabulazione, interruzione di riga  
- `Personalizzato` – inserire uno o più caratteri; più caratteri consecutivi vengono trattati come un unico delimitatore composto  
- `TreatConsecutiveDelimitersAsOne` – collassa i delimitatori adiacenti in un singolo separatore  

Vengono elaborate soltanto le celle di tipo stringa; numeri, valori booleani e formule vengono convertiti in stringa prima della suddivisione (le formule vengono perse). Restituisce il numero di celle pulite e il flusso del foglio di calcolo aggiornato.

### Endpoint API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l’autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Percorso/Query String/Corpo HTTP | Descrizione |
|----------------|---------|----------------------------------|-------------|
| name | stringa | Percorso | (Obbligatorio) Nome del file del foglio di calcolo da recuperare. |
| worksheet | stringa | Percorso | Specifica il foglio di calcolo. |
| range | stringa | Percorso | Specifica l'intervallo nel foglio di calcolo. |
| delimiters | stringa | Query | Delimitatori usati per suddividere i valori delle celle (es. virgola, punto e virgola, spazio, tabulazione, interruzione di riga). Obbligatorio. |
| treatConsecutiveDelimitersAsOne | booleano | Query | Collassa i delimitatori adiacenti in un singolo separatore. Valore predefinito: true. Opzionale. |
| caseSensitive | booleano | Query | Esegui confronto distinto tra maiuscole e minuscole durante il rilevamento delle duplicazioni. Opzionale. |
| folder | stringa | Query | (Opzionale) Percorso della cartella in cui è memorizzato il foglio di calcolo. Valore predefinito: null. |
| storageName | stringa | Query | (Opzionale) Nome dello storage qualora si utilizzi un cloud storage personalizzato. |
| region | stringa | Query | Impostazione di regione/lingua del foglio di calcolo (es. `en-US`, `fr-FR`). Opzionale. |
| password | stringa | Query | Password necessaria per aprire il file del foglio di calcolo. Opzionale. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| - | - | Nessun corpo della richiesta è richiesto per questa operazione. |

### **Risposta**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "flusso del foglio di calcolo in base64"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Operazione riuscita; restituisce il numero di celle pulite e il flusso del foglio di calcolo aggiornato. |
| 400 | Richiesta non valida | Uno o più parametri della richiesta sono mancanti o non validi. |
| 401 | Non autorizzato | Autenticazione non riuscita o token JWT mancante/invalido. |
| 413 | Payload troppo grande | La richiesta supera i limiti di dimensione consentiti. |
| 500 | Errore interno del server | Si è verificato un errore imprevisto sul server. |

## Come utilizzare la funzionalità di rimozione delle sottostringhe duplicate in fogli di calcolo remoti con gli SDK

### Specifica della funzionalità di rimozione delle sottostringhe duplicate in fogli di calcolo remoti

La [specifica dell’API per la rimozione delle sottostringhe duplicate in fogli di calcolo remoti](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}
{< tab tabNum="1" >}
```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "flusso del foglio di calcolo in base64"
}
```
{< /tab >}
{< /tabs >}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK rappresenta il metodo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells Cloud utilizzando vari SDK:
`[TBD]`