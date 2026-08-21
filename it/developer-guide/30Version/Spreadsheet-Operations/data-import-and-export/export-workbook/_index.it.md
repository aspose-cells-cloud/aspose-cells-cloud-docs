---
title: "Esporta cartella di lavoro"
second_title: "Documento"
linktitle: "Cartella di lavoro"
type: docs
url: /export-excel-to-different-formats/
aliases: [/export/excel-to-different-formats/]
keywords: "Aspose.Cells Cloud, esportazione Excel, conversione cartella di lavoro, PDF, CSV, JSON, formati immagine, API foglio di calcolo, XLSX, ODS, PNG"
description: "Una guida passo-passo per esportare cartelle di lavoro Excel in diversi formati—tra cui PDF, CSV, JSON e vari tipi di immagine—utilizzando l’API REST Aspose.Cells Cloud e i relativi SDK."
weight: 20
---

Puoi esportare cartelle di lavoro in uno dei seguenti formati: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## API REST


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.


### Parametri della richiesta

| Nome parametro | Tipo    | Percorso/Query string/Corpo HTTP | Obbligatorio | Descrizione |
|----------------|---------|----------------------------------|--------------|-------------|
| file           | file    | formData                         | Sì           | File da caricare |
| objectType     | string  | query                            | Sì           | Tipo di oggetto da esportare. Per l'esportazione di grafici usa `chart`. Altri valori possibili sono `worksheet`, `picture`, ecc. |
| format         | string  | query                            | Sì           | Format di output desiderato. Valori supportati: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |


### **Risposta**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**Codici di stato HTTP**

| Codice | Significato             | Descrizione |
|--------|-------------------------|-------------|
| 200    | OK                      | forme esportate correttamente; la risposta contiene l'elenco dei file. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi. |
| 401    | Non autorizzato         | Token di accesso non valido o mancante. |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server | Errore imprevisto sul server. |


## Come utilizzare l'API PostExport con gli SDK

### Specifica dell'API PostExport


La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiscono un'interfaccia di programmazione pubblicamente accessibile che consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud tramite cURL.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Utilizzo degli SDK Aspose.Cells Cloud

L'utilizzo di un SDK accelera lo sviluppo gestendo i dettagli di basso livello, permettendoti di concentrarti sulla logica di business. Un elenco completo degli SDK Aspose.Cells Cloud è disponibile nel [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come chiamare il servizio web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}

---