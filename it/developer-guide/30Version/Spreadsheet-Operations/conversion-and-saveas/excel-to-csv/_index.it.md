---
title: "Excel in CSV"
second_title: "Documenti"
linktype: "Excel in CSV"
type: docs
url: /it/itconvert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel in CSV, Aspose.Cells Cloud, API REST, conversione fogli di calcolo, file CSV, conversione file"
description: "Converti fogli di calcolo Excel in CSV utilizzando l'API REST di Aspose.Cells Cloud. Supporta numerosi SDK e linguaggi di programmazione per un'integrazione semplice."
weight: 90
---

Questa API REST converte un file di foglio di calcolo in un file in formato CSV.

## API REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.


### Parametri della query

| Nome parametro          | Tipo   | Descrizione                                                                           |
| ----------------------- | ------ | ------------------------------------------------------------------------------------- |
| `password`              | string | La password necessaria per aprire il file Excel.                                         |
| `storageName`           | string | Il nome dello storage in cui è situato il file.                                    |
| `checkExcelRestriction` | bool   | Indica se verificare le restrizioni del file Excel quando l'utente modifica oggetti correlati alle celle. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo      | Descrizione                                                             |
| -------------- | --------- | ----------------------------------------------------------------------- |
| `datafile`     | file dati | Il file dati incluso nella prima parte del corpo della richiesta multipart. |

### Risposta

L'API restituisce un oggetto **FileInfo** contenente il file CSV generato.

| Campo           | Tipo   | Descrizione                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Nome del file CSV (ad esempio, `esempio.csv`). |
| **FileSize**    | int    | Dimensione del file in byte.                    |
| **FileContent** | string | Contenuto del file CSV codificato in Base64.      |

[FileInfo](/cells/file-info/)


**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto del server. |

## Come utilizzare l'API PostConvertWorkbookToCSV con gli SDK

### Specifica dell'API PostConvertWorkbookToCSV

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "esempio.CSV",
  "FileSize": 12345,
  "FileContent": "Contenuto file: stringa_codificata_in_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta la [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

Gli esempi di codice seguenti mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}