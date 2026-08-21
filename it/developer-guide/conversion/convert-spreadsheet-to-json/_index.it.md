---
---
title: "Aspose.Cells Cloud Web API – Convertire foglio di calcolo in JSON"
second_title: "Documento"
ArticleTitle: "Come convertire un foglio di calcolo locale in JSON utilizzando Aspose.Cells Cloud API"
linktitle: "Convertire foglio di calcolo in JSON"
type: docs
url: /convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, convertire foglio di calcolo in JSON, Excel in JSON API, Aspose.Cells Cloud API, REST API, conversione foglio di calcolo"
description: "Scopri come convertire file Excel locali in JSON con Aspose.Cells Cloud API. Include endpoint, parametri, codice di esempio e gestione degli errori per un'integrazione senza problemi."
weight: 100
---

L'endpoint **ConvertSpreadsheetToJson** converte un foglio di calcolo archiviato su un disco locale in un file JSON interamente sul server di Aspose.Cells Cloud. Inviando il foglio di calcolo come `multipart/form-data`, il servizio restituisce un flusso JSON pronto per il download o l'elaborazione successiva. Questa conversione nativa nel cloud elimina la necessità di caricare prima il file nello storage, riduce i costi di archiviazione e semplifica il flusso di lavoro per le applicazioni che richiedono dati di fogli di calcolo in formato JSON per analisi, report o scambio di dati.

**Prerequisiti**: È necessario disporre di un account Aspose Cloud, di un token di accesso JWT valido e di un SDK o chiave API di Aspose.Cells Cloud configurato.

**Contesto**: Convertire fogli di calcolo in JSON è un passaggio comune quando si integrano dati Excel con servizi web, database NoSQL o applicazioni JavaScript lato client. L'API Converti foglio di calcolo in JSON fornisce una conversione rapida lato server senza la necessità di archiviare il file originale.

## API Converti foglio di calcolo in JSON

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome del parametro | Tipo                       | Posizione | Obbligatorio/Opzionale | Descrizione                                                                                                                                                                     |
| :----------------- | :------------------------- | :-------- | :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet        | File (multipart/form-data) | FormData  | Obbligatorio          | File del foglio di calcolo sorgente (ad esempio, `.xls`, `.xlsx`, `.xlsm`). Esempio: `curl -F "Spreadsheet=@myfile.xlsx"`                                                       |
| outPath            | Stringa                    | Query     | Opzionale             | Percorso della cartella di destinazione sullo storage cloud dove verrà salvato il file JSON convertito. Se omesso, il JSON viene restituito direttamente nel flusso di risposta. Esempio: `outPath=/output/`. |
| outStorageName     | Stringa                    | Query     | Opzionale             | Nome dello storage cloud (ad esempio, Amazon S3, Azure Blob) in cui scrivere il file di output. Richiesto solo quando `outPath` utilizza uno storage non predefinito.            |
| fontsLocation      | Stringa                    | Query     | Opzionale             | Percorso di una cartella personalizzata dei font sul server. Utilizzare quando il foglio di calcolo fa riferimento a font non disponibili nella libreria predefinita.          |
| region             | Stringa                    | Query     | Opzionale             | Impostazione area/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione di numeri, date e valute durante la conversione.                      |
| password           | Stringa                    | Query     | Opzionale             | Password per aprire un foglio di calcolo protetto da password. Omettere per file non protetti.                                                                                  |

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

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto sul server.                                     |

## Dove utilizzare l'API Converti foglio di calcolo in JSON?

- **Pipeline di migrazione dei dati** – Convertire report Excel legacy in JSON per l'ingestione in database NoSQL moderni o data lake.
- **Applicazioni mobili o web** – Trasformare rapidamente fogli di calcolo caricati dall'utente in JSON per il rendering lato client senza archiviare il file originale nel cloud.
- **Report automatizzati** – Generare payload JSON per servizi di analisi a valle (ad esempio, Power BI, Tableau) direttamente da input di fogli di calcolo.
- **Funzioni serverless** – Utilizzare l'API all'interno di AWS Lambda o Azure Functions per effettuare conversioni in tempo reale senza gestire storage temporanei.

## Perché utilizzare l'API Converti foglio di calcolo in JSON?

- La conversione nativa nel cloud elimina la necessità di caricare file di grandi dimensioni nello storage prima dell'elaborazione, riducendo latenza e costi di archiviazione.
- Flusso di lavoro in una singola richiesta: caricare il foglio di calcolo e ricevere JSON nella stessa chiamata HTTP, semplificando la logica di integrazione.
- Supporta fogli di calcolo protetti da password e regionali, garantendo una rappresentazione accurata dei dati tra diverse localizzazioni.
- Scalabile sull'infrastruttura Aspose: gestisce cartelle di lavoro grandi e formule complesse senza impattare le risorse del proprio server.

## Come utilizzare l'API Converti foglio di calcolo in JSON con gli SDK

### Specifica dell'API Converti foglio di calcolo in JSON

La [Specifica dell'API Converti foglio di calcolo in JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) fornisce un'interfaccia di programmazione pubblicamente accessibile per eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli di basso livello e consente di convertire un foglio di calcolo in JSON con poche righe di codice.  
Consultare il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.  
I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}