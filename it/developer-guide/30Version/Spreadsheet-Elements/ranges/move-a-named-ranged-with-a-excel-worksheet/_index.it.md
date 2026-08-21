---
title: "Spostare un intervallo denominato in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Sposta"
type: docs
url: /it/ranges/move/
aliases: [  /it/move-a-named-range-with-an-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, sposta intervallo denominato, foglio di lavoro Excel, API REST, spostamento intervallo, esempi SDK"
description: "Scopri come spostare un intervallo denominato all'interno di un foglio di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud v3.0, con dettagli sull'endpoint, autenticazione, esempi e frammenti di codice SDK."
weight: 20
ArticleTitle: "Spostare un intervallo denominato in un foglio di lavoro Excel tramite l'API Aspose.Cells Cloud"
---

Spostare un intervallo denominato è un'attività comune quando è necessario riorganizzare i dati in modo programmatico. Questa sezione spiega come spostare un intervallo definito in una nuova posizione sullo stesso foglio di lavoro utilizzando l'API REST Aspose.Cells Cloud.

Questa API REST sposta un intervallo specificato in un intervallo di destinazione su un foglio di lavoro Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### Autenticazione
L'API richiede un **token JWT Bearer** ottenuto tramite il flusso OAuth di Aspose Cloud. Includi il token nell'intestazione `Authorization`:

```
Authorization: Bearer <jwt token>
```

Il token deve avere l'ambito **Cells**.

### Prerequisiti
- Il workbook deve essere archiviato nello storage di Aspose Cloud.  
- Fornire il nome dello storage (`storageName`) e il percorso della cartella (`folder`) se il file non si trova nella directory principale.  
- Utilizzare la versione più recente dell'SDK di Aspose.Cells Cloud che supporta la versione API **v3.0**.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome           | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| **name**       | string | path      | Nome del file del workbook |
| **sheetName**  | string | path      | Nome del foglio di lavoro |
| **destRow**    | integer| query     | Indice della riga iniziale dell'intervallo di destinazione (0‑based) |
| **destColumn**| integer| query     | Indice della colonna iniziale dell'intervallo di destinazione (0‑based) |
| **range**      | object | body      | Definizione dell'intervallo sorgente da spostare |
| **folder**     | string | query     | Percorso della cartella in cui è archiviato il workbook |
| **storageName**| string | query     | Nome dello storage di Aspose Cloud |

### Corpo della richiesta

| Campo          | Tipo   | Obbligatorio | Descrizione |
|----------------|--------|--------------|-------------|
| **ColumnCount**| integer| No | Numero di colonne nell'intervallo sorgente |
| **ColumnWidth**| integer| No | Larghezza di ciascuna colonna (in punti) |
| **FirstColumn**| integer| No | Indice iniziale (0‑based) della prima colonna dell'intervallo sorgente |
| **FirstRow**   | integer| No | Indice iniziale (0‑based) della prima riga dell'intervallo sorgente |
| **Name**       | string | No | Nome dell'intervallo (se si tratta di un intervallo denominato) |
| **RefersTo**   | string | No | Riferimento in stile A1 che definisce l'intervallo |
| **RowCount**   | integer| No | Numero di righe nell'intervallo sorgente |
| **RowHeight**  | integer| No | Altezza di ciascuna riga (in punti) |
| **Worksheet**  | string | No | Foglio di lavoro che contiene l'intervallo sorgente |

### Flusso di lavoro

1. **Carica** il workbook nello storage di Aspose Cloud (se non esiste già).  
2. **Genera** un token JWT utilizzando l'endpoint OAuth.  
3. **Costruisci** il payload JSON che descrive l'intervallo sorgente.  
4. **Chiama** l'endpoint `moveto` con i parametri di percorso, query e il corpo JSON richiesti.  
5. **Verifica** la risposta; una chiamata riuscita restituisce lo stato `200 OK`.

### Esempio di richiesta / risposta

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Quando si verifica un errore, la risposta include un campo opzionale `ErrorMessage` che fornisce dettagli aggiuntivi sull'errore.

**Codici di stato HTTP**

| Codice | Significato                  | Descrizione                                       |
|--------|------------------------------|---------------------------------------------------|
| 200    | OK                           | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida         | Parametri mancanti o non validi (ad es., tipo di file non supportato). |
| 401    | Non autorizzato              | Token JWT non valido o mancante. |
| 413    | Payload troppo grande        | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server    | Errore imprevisto del server. |

**Schema della risposta**

| Campo | Tipo   | Descrizione |
|-------|--------|-------------|
| **Code** | integer | Codice di stato simile HTTP restituito dall'API (ad es., 200) |
| **Status** | string | Descrizione testuale del risultato (ad es., "OK") |
| **ErrorMessage** | string (opzionale) | Dettagli dell'errore leggibili dall'uomo in caso di fallimento della chiamata |

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}