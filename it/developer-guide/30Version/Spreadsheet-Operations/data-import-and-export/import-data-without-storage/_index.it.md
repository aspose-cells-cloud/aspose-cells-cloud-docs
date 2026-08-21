---
title: "Importare dati senza utilizzare l'archiviazione – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Importazione dati senza archiviazione"
type: docs
url: /it/import/without-using-storage/
aliases: [  /it/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells, Cloud API, importazione dati senza archiviazione, API per importazione Excel, REST import"
description: "Scopri come importare dati senza archiviazione in un file Excel utilizzando l'API Aspose.Cells Cloud. Include il formato della richiesta, i parametri, un esempio cURL, il codice SDK e la gestione degli errori."
weight: 10
ArticleTitle: "Importare dati senza utilizzare l'archiviazione – Aspose.Cells Cloud API"
---

L'importazione di dati Excel può essere complessa poiché molti fattori influenzano il risultato finale. Tutti questi fattori devono essere presi in considerazione durante il processo di **importazione**. Aspose.Cells Cloud semplifica l'importazione di vari formati e tipi di dati in un file Excel, garantendo una qualità professionale.

Questa API REST importa **dati** all'interno di un file Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo          | Posizione  | Descrizione                                                                                                                                     |
| -------------- | ------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| file           | file          | formData   | Il file Excel da caricare.                                                                                                                       |
| ImportOption   | ImportOption  | JSON body  | Oggetto JSON che definisce i dati da importare, il relativo tipo (ad esempio `IntArray`, `DoubleArray`, `StringArray`) e la posizione all'interno del foglio di calcolo. |

I parametri **ImportOption** sono descritti nel riferimento **Opzione ImportData** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter).

**Prerequisiti:**  
Un token JWT valido deve essere generato in anticipo e la dimensione del file non deve superare il limite del servizio (tipicamente 100 MB). I formati di file supportati includono XLS, XLSX, CSV e ODS. Assicurati che l'SDK appropriato sia installato se preferisci l'accesso programmatico.

### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

**Note:**  
Durante l'invio della richiesta, l'intestazione `Content-Type: multipart/form-data` viene impostata automaticamente tramite il flag `-F`. Per payload di grandi dimensioni, considera la compressione dei dati prima dell'importazione e implementa una logica di retry per errori transitori.

## Come utilizzare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*Il flag `-F` imposta automaticamente `Content-Type: multipart/form-data`.*  

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello e consente di concentrarsi sulle attività del proprio progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}