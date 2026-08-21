---
title: "Converti un file Excel in un altro formato o salvalo in modo diverso."
second_title: "Document"
linktype: "Conversione e Salva con nome"
type: docs
url: /it/conversion-and-save-as/
aliases: [/it/convert-excel/, /it/convert/]
keywords: "Aspose.Cells, API di conversione Excel, converti Excel in PDF, Excel in CSV, Excel in JSON, conversione cloud di fogli elettronici"
description: "Scopri come convertire cartelle di lavoro Excel in PDF, CSV, JSON, HTML e oltre 15 altri formati utilizzando l'API REST Aspose.Cells Cloud. Include dettagli sugli endpoint, comandi cURL di esempio e frammenti di codice per SDK in Java, .NET, Python e altro ancora."
weight: 30
ArticleTitle: "Converti file Excel in PDF, CSV, JSON e altro con Aspose.Cells Cloud"
---

Se hai creato originariamente un file Excel in un determinato formato—ad esempio [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), o [CSV](https://docs.fileformat.com/spreadsheet/csv/)—potresti trovarlo utile per convertire il file Excel in un altro formato per sfruttare funzionalità speciali. Ad esempio, convertire un file Excel in [PDF](https://docs.fileformat.com/pdf/) protegge i suoi contenuti da modifiche non autorizzate e ne facilita la lettura e la condivisione.

**Prerequisiti**  
Prima di chiamare le API di conversione, ottieni un token di accesso OAuth 2.0 da Aspose Cloud e assicurati che la cartella di lavoro sia memorizzata nel tuo archivio Aspose Cloud (o inclusa nel corpo della richiesta per l'endpoint di conversione PUT).

La conversione di documenti è un processo complesso. Molti fattori contribuiscono alla complessità del processo di conversione e devono essere considerati durante la trasformazione. Fornire una conversione precisa e di qualità professionale tra formati Excel è una funzionalità chiave di Aspose.Cells Cloud.

Il servizio funziona in modo fluido per qualsiasi conversione di formati di documento. Puoi sia importare che esportare documenti in questi formati:

**Formati supportati**  
- Importazione/Esportazione: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- Esportazione solo: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### API di conversione

| API                         | Descrizione                                                                             |
| :-------------------------- | :-------------------------------------------------------------------------------------- |
| `GET /cells/{name}`         | Recupera una cartella di lavoro Excel dall'archivio cloud e la converte nel formato richiesto. |
| `PUT /cells/convert`        | Converte una cartella di lavoro Excel fornita nel corpo della richiesta nel formato di output specificato. |
| `POST /cells/{name}/saveAs` | Salva una cartella di lavoro Excel esistente in un altro formato direttamente nell'archivio cloud.           |

**Dettagli API**

- **GET /cells/{name}**  
  - **Parametri di percorso:** `name` – nome del file della cartella di lavoro (obbligatorio).  
  - **Parametri di query:** `format` – formato di destinazione (ad es., pdf, csv, json); `storage` – nome dell'archivio cloud (opzionale); `folder` – percorso della cartella all'interno dell'archivio (opzionale).  
  - **Risposta:** Flusso di file della cartella di lavoro convertita; `Content‑Type` corrisponde al formato di destinazione.  
  - **Codici di stato:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **Corpo della richiesta:** multipart/form‑data contenente il file della cartella di lavoro di origine (`file`) e un campo obbligatorio `format` che indica l'output desiderato.  
  - **Risposta:** Flusso binario del file convertito.  
  - **Codici di stato:** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **Parametri di percorso:** `name` – nome della cartella di lavoro esistente.  
  - **Parametri di query:** `format` – formato di destinazione; `outPath` – percorso di destinazione nell'archivio cloud (opzionale); `storage` – nome dell'archivio (opzionale).  
  - **Risposta:** Oggetto JSON con il risultato dell'operazione e il percorso del file salvato. Esempio di risposta:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "File salvato correttamente.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **Codici di stato:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

**Esempio di cURL per la conversione in PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Frammento di codice per Java SDK (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**Frammento di codice per .NET SDK (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Frammento di codice per Python SDK (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

I seguenti articoli spiegano in dettaglio ciascuna API e includono esempi aggiuntivi di cURL e SDK:

- [Converti un file Excel in un formato diverso](/it/cells/convert-an-excel-file-to-different-formats)
- [Salva un file Excel in un formato diverso](/it/cells/save-an-excel-file-as-other-formats-files)
- [Converti un file Excel in un file CSV](/it/cells/convert-excel-file-to-csv-file)
- [Converti un file Excel in un file DOCX](/it/cells/convert-excel-file-to-docx-file)
- [Converti un file Excel in un file HTML](/it/cells/convert-excel-file-to-html-file)
- [Converti un file Excel in un file JSON](/it/cells/convert-excel-file-to-json-file)
- [Converti un file Excel in un file Markdown](/it/cells/convert-excel-file-to-markdown-file)
- [Converti un file Excel in un file PDF](/it/cells/convert-excel-file-to-pdf-file)
- [Converti un file Excel in un file PNG](/it/cells/convert-excel-file-to-png-file)
- [Converti un file Excel in un file PPTX](/it/cells/convert-excel-file-to-pptx-file)
- [Converti un file Excel in un file SQL](/it/cells/convert-excel-file-to-sql-file)
- [Converti un file Excel in un file TIFF](/it/cells/convert-excel-file-to-tiff-file)
---