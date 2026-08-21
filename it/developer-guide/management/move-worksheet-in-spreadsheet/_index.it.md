---
title: "Aspose.Cells Cloud Excel: Web API per spostare i fogli di lavoro – Modificare la posizione dei fogli in modo programmatico"
second_title: "Documento"
ArticleTitle: "Come spostare i fogli di lavoro in Excel – Riordinare l’ordine e la posizione dei fogli"
linktitle: "Sposta foglio di lavoro nel foglio elettronico"
type: docs
url: /it/move-worksheet-in-spreadsheet/
keywords: "API per spostare fogli di lavoro, API per riordinare fogli, API per cambiare l’ordine dei fogli, API per la gestione delle schede Excel, Aspose Cells REST API, automatizzare la posizionamento dei fogli, API per l’organizzazione dei file di lavoro, API per la struttura dei fogli elettronici, automazione Excel nel cloud, riordino batch dei fogli"
description: "Scopri come spostare i fogli di lavoro all’interno dei file di lavoro Excel per riorganizzare l’ordine dei fogli e ottimizzare la struttura del file. Modifica la posizione dei fogli di lavoro, riordina le schede per migliorare il flusso di lavoro e automatizza l’organizzazione dei fogli per una gestione professionale dei fogli elettronici."
weight: 100
---

Sposta in modo programmatico i fogli di lavoro all’interno dei file di lavoro Excel utilizzando l’API Aspose.Cells Cloud. Modifica le posizioni dei fogli, riordina le schede e ottimizza la struttura del file di lavoro tramite chiamate API RESTful. Ideale per automatizzare l’organizzazione dei fogli elettronici e creare layout standardizzati dei file di lavoro.

## **Sposta foglio di lavoro tramite l’API Foglio elettronico**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?sheetName={sheetName}&position={position}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome del parametro | Tipo    | Percorso/Query String/Corpo HTTP | Descrizione                                                                                                                                                           |
| :----------------- | :------ | :----------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet        | File    | FormData                       | **Obbligatorio**. Il file di lavoro Excel di origine (.xlsx, .xls, ecc.) contenente il foglio di lavoro da riordinare.                                                |
| worksheet          | String  | Query                          | **Obbligatorio**. Il nome esatto del foglio di lavoro da spostare (ad esempio, `Sommario`, `DatiGrezzi_2024`).                                                      |
| position           | Integer | Query                          | **Obbligatorio**. Il nuovo indice in posizione zero-based per il foglio di lavoro. Ad esempio, `0` lo sposta in prima posizione, `2` lo sposta in terza posizione.   |
| outPath            | String  | Query                          | **Facoltativo**. Il percorso della cartella di destinazione nello spazio di archiviazione cloud dove verrà salvato il file di lavoro riorganizzato. Se `null` o omesso, assume come predefinita la directory del file di origine. |
| outStorageName     | String  | Query                          | **Obbligatorio**. L’identificatore del nome del servizio di archiviazione cloud configurato (ad esempio, `TeamDrive`) dove verrà memorizzato il file di output.      |
| region             | String  | Query                          | **Facoltativo**. L’impostazione locale (ad esempio, `it-IT`) da applicare, che può influenzare alcune regole di formattazione durante l’operazione di salvataggio.     |
| password           | String  | Query                          | **Facoltativo**. La password di decrittazione necessaria per aprire e modificare un file di lavoro protetto da password. Omettere se il file non è crittografato.      |

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

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Dove dovremmo utilizzare l’API per spostare i fogli di lavoro nel foglio elettronico?

- **Generazione standardizzata dei report**: Dopo la generazione automatica dei report mensili o trimestrali, il foglio di lavoro `Sommario` o `Panoramica Esecutiva` viene spostato all’inizio del file di lavoro per garantire che le conclusioni principali siano visibili all’apertura del file.
- **Pipeline di elaborazione dei dati**: Dopo aver elaborato i fogli di lavoro grezzi provenienti da diverse fonti dati nel processo ETL, il foglio `Dati_Elaborati`, dopo la pulizia e la trasformazione, viene spostato in una posizione logica all’interno del file di lavoro (ad esempio, al centro), creando una struttura chiara del processo con i dati originali e i risultati dell’analisi.
- **Consegna di file personalizzati per l’utente**: Dopo che l’utente seleziona un layout preferito tramite un’interfaccia di configurazione (ad esempio, posizionando la pagina con i grafici in cima), il sistema riordina automaticamente l’ordine dei fogli di lavoro nel file di lavoro in base alla selezione e consegna il file personalizzato.

## Perché dovresti utilizzare l’API per spostare i fogli di lavoro nel foglio elettronico?

- **Facile da usare per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate, riduce significativamente il carico di lavoro di sviluppo.
- **Riduzione dei costi del personale**: Riduce la necessità di personale dedicato al consolidamento dei documenti.
- **Pagamento in base all’uso**: Nessun investimento iniziale; si paga solo per le chiamate API effettivamente utilizzate.
- **Costi di manutenzione nulli**: Nessuna necessità di mantenere server, aggiornare software o gestire problemi di compatibilità.

## Come utilizzare l’API per spostare i fogli di lavoro nel foglio elettronico con gli SDK

### Specifica dell’API per spostare i fogli di lavoro nel foglio elettronico

La [Specifica dell’API per spostare i fogli di lavoro nel foglio elettronico](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) fornisce un’interfaccia di programmazione pubblicamente accessibile per facilitare interazioni REST dirette da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheet/move?sheetName=Sheet1&destIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK è il modo più veloce per sviluppare, poiché astrae i dettagli a basso livello, consentendo di spostare i fogli di lavoro nel foglio elettronico con codice conciso. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.  
I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---