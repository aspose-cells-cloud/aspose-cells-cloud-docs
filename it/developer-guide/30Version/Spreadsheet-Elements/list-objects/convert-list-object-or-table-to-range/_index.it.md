---
title: "Converti oggetto elenco in intervallo – Aspose.Cells Cloud API"
ArticleTitle: "Converti oggetto elenco in intervallo usando Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "Conversione"
type: docs
url: /it/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "API Aspose Cells, converti oggetto elenco in intervallo, API REST Excel"
description: "Scopri come convertire un oggetto elenco Excel (tabella) in un intervallo usando l'API REST Aspose.Cells Cloud. Include sintassi della richiesta, parametri, esempi cURL, schema di risposta, dettagli sull'autenticazione, codici di errore ed esempi di SDK."
weight: 30
---

Questa API REST converte un **oggetto elenco (tabella)** in un **intervallo** all'interno di un foglio di lavoro Excel.

**Prerequisiti:**  
Prima di chiamare l'endpoint, assicurati che il workbook sia caricato nello storage Aspose Cloud, che il foglio di lavoro contenga l'oggetto elenco target e che tu stia usando un formato di file supportato (ad esempio .xlsx, .xlsm).

## API REST

**Autenticazione**  
Per chiamare questa operazione devi includere un token JWT valido nell'intestazione `Authorization`. Ottieni il token inviando una richiesta POST all'endpoint di token OAuth 2.0 con il tuo client ID e client secret. Il token deve includere l'ambito `Cells.ReadWrite` ed è valido per il periodo restituito dal servizio token.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome                | Tipo    | Posizione | Obbligatorio | Predefinito | Descrizione                                              |
| ------------------- | ------- | --------- | ------------ | ----------- | -------------------------------------------------------- |
| **name**            | stringa | percorso  | Sì           | –           | Nome del file Excel.                                     |
| **sheetName**       | stringa | percorso  | Sì           | –           | Nome del foglio di lavoro contenente l'oggetto elenco.  |
| **listObjectIndex** | intero  | percorso  | Sì           | –           | Indice in base zero dell'oggetto elenco (tabella) da convertire. |
| **folder**          | stringa | query     | No           | –           | Percorso della cartella in cui è memorizzato il file.   |
| **storageName**     | stringa | query     | No           | –           | Nome del servizio di archiviazione.                      |

> **Nota:** Questa operazione funziona solo con formati moderni di Excel come **.xlsx** e **.xlsm**. L'oggetto elenco non deve essere protetto. Per ulteriori informazioni sugli oggetti elenco, consulta la [panoramica sugli oggetti elenco](/list-objects/). Per dettagli sull'uso degli intervalli, consulta la [documentazione sugli intervalli](/ranges/).

### Esempio cURL (richiesta)

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### Schema di risposta

L'API restituisce una risposta **200 OK** con i dettagli dell'intervallo appena creato.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| Campo           | Tipo    | Descrizione                                          |
| --------------- | ------- | ---------------------------------------------------- |
| **Code**        | intero  | Codice di stato simile a HTTP (200 indica successo). |
| **Status**      | stringa | Messaggio di stato testuale.                         |
| **RangeName**   | stringa | Nome assegnato all'intervallo creato.                |
| **Address**     | stringa | Indirizzo completo dell'intervallo, incluso il nome del foglio. |
| **FirstRow**    | intero  | Indice in base zero della prima riga nell'intervallo. |
| **FirstColumn** | intero  | Indice in base zero della prima colonna nell'intervallo. |
| **RowCount**    | intero  | Numero di righe nell'intervallo.                     |
| **ColumnCount** | intero  | Numero di colonne nell'intervallo.                   |

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                              |
|--------|-----------------------------|----------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                         |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.        |
| 500    | Errore interno del server   | Errore imprevisto del server.                            |

**Schema di risposta in caso di errore (esempio):**

```json
{
  "Code": 400,
  "Message": "listObjectIndex non valido. L'indice deve essere compreso tra 0 e 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'uso di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells mediante vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}