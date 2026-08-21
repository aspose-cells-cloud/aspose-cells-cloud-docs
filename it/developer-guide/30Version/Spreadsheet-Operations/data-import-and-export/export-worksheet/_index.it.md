---
title: "Esporta Foglio di Lavoro – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Foglio di Lavoro"
type: docs
url: /it/export-excel-worksheet-to-different-formats/
aliases: [  /it/export/excel-worksheet-to-different-formats/ ]
keywords: "Aspose.Cells, esporta foglio di lavoro, API Excel, PDF, CSV, TIFF, ODS, formati immagine"
description: "Scopri come esportare un foglio di lavoro Excel in PDF, CSV, TIFF e altri formati utilizzando l'API REST di Aspose.Cells Cloud. Include un esempio cURL, autenticazione richiesta, dettagli dei parametri e gestione della risposta."
weight: 20
ArticleTitle: "Esporta Foglio di Lavoro Excel in Vari Format – Aspose.Cells Cloud"
---

Puoi esportare un foglio di lavoro nei seguenti formati:

- **XLS** – [Dettagli sul formato XLS](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [Dettagli sul formato XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [Dettagli sul formato XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [Dettagli sul formato CSV](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [Dettagli sul formato TSV](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [Dettagli sul formato XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [Dettagli sul formato ODS](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [Dettagli sul formato TXT](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [Dettagli sul formato PDF](https://docs.fileformat.com/pdf/)
- **OTS** – [Dettagli sul formato OTS](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [Dettagli sul formato XPS](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [Dettagli sul formato DIF](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [Dettagli sul formato PNG](https://docs.fileformat.com/Image/png/)
- **JPEG** – [Dettagli sul formato JPEG](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [Dettagli sul formato BMP](https://docs.fileformat.com/image/bmp/)
- **SVG** – [Dettagli sul formato SVG](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [Dettagli sul formato TIFF](https://docs.fileformat.com/image/tiff/)
- **EMF** – [Dettagli sul formato EMF](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Dettagli sul formato Numbers](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [Dettagli sul formato FODS](https://docs.fileformat.com/spreadsheet/fods/)

[Esplora operazioni di esportazione correlate, come l'esportazione dell'intero workbook o di un grafico.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## API PostExport

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro | Tipo    | Percorso/Query String/Corpo HTTP | Obbligatorio | Descrizione                                                                 |
|----------------|---------|----------------------------------|--------------|-----------------------------------------------------------------------------|
| file           | file    | formData                         | Sì           | File da caricare                                                            |
| objectType     | string  | query                            | Sì           | Tipo di oggetto da esportare. Per l'esportazione di grafici usare `chart`. Altri valori possibili sono `worksheet`, `picture`, ecc. |
| format         | string  | query                            | Sì           | Format di output desiderato. Valori supportati: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### Risposta

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **Gestione degli Errori**

Se la richiesta fallisce, l'API restituisce un oggetto JSON di errore contenente campi come `Code` e `Message`. I codici di stato HTTP tipici includono **401 Unauthorized** (token mancante o non valido) e **400 Bad Request** (parametri non validi).

**Codici di Stato HTTP**

| Codice | Significato                 | Descrizione                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200    | OK                          | Filtro applicato con successo; la risposta contiene i dettagli dell'operazione. |
| 400    | Bad Request                 | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Unauthorized                | Token JWT non valido o mancante.                              |
| 413    | Payload Too Large           | Il file caricato supera il limite di dimensione.             |
| 500    | Internal Server Error       | Errore imprevisto del server.                                 |

**Note**

- La dimensione massima del file per il caricamento è di 50 MB.  
- L'API supporta l'esportazione di più fogli di lavoro in una singola richiesta; ogni foglio viene restituito come file separato nell'array `Files`.  
- È disponibile l'elaborazione asincrona per workbook di grandi dimensioni; utilizzare la risposta `202 Accepted` per controllare lo stato dell'operazione.

## Come Usare l'API PostExport con gli SDK

### Prerequisiti

Prima di chiamare l'API, ottieni un token di accesso JWT valido utilizzando il flusso di autenticazione di Aspose.Cells Cloud. Assicurati che il token sia incluso nell'header `Authorization` di ogni richiesta. Gli SDK gestiscono automaticamente l'acquisizione del token quando vengono configurati con le tue credenziali client.

### Specifica dell'API PostExport

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiscono un'interfaccia di programmazione accessibile pubblicamente e ti consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

```bash
# Esporta un foglio di lavoro nel formato TIFF
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare un SDK è il modo più veloce per sviluppare con Aspose.Cells Cloud. Un SDK nasconde i dettagli a basso livello, consentendoti di concentrarti sulla logica di business. Per l'elenco completo degli SDK supportati, visita il [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}