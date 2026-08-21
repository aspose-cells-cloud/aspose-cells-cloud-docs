---
title: "Esporta grafico Excel"
second_title: "Documento"
linktype: "grafico"
type: docs
url: /it/export-excel-chart-to-different-formats/
aliases: [  /it/export/excel-chart-to-different-formats/ ]
description: "Esporta oggetti grafico Excel in formati diffusi come PNG, JPEG, PDF, SVG, TIFF, EMF, WMF e altri utilizzando l'API REST Aspose.Cells Cloud o gli SDK. Include autenticazione, un esempio cURL e campioni di codice per diversi linguaggi."
keywords: "Aspose.Cells, esportazione grafico, esportazione grafico Excel, API REST, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, formati grafico, Aspose Cells Cloud"
weight: 20
ArticleTitle: "Esporta grafico Excel – Documento"
---

Esportare oggetti grafico da un foglio di calcolo Excel in vari formati immagine e documento è un requisito comune per la generazione di report e la pubblicazione. Aspose.Cells Cloud fornisce un semplice endpoint REST che converte direttamente i grafici in formati diffusi come PNG, JPEG, PDF, SVG, TIFF, EMF, WMF e altri.

Puoi esportare i grafici nei seguenti formati: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), e [PDF](https://docs.fileformat.com/pdf/).

**Prerequisiti:**  
- Un account Aspose.Cells Cloud valido con un abbonamento attivo.  
- Un token OAuth 2.0 Bearer (JWT) ottenuto tramite il flusso di autenticazione.  
- Il file del foglio di calcolo da caricare (dimensione massima < 50 MB).  

## **API REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Obbligatorio | Descrizione                                                                                                                     |
|----------------|--------|----------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| file           | file   | formData                         | Sì           | File da caricare                                                                                                                  |
| objectType     | string | query                            | Sì           | Il tipo di oggetto da esportare. Per l'esportazione di grafici usa `chart`. Altri valori possibili sono `worksheet`, `picture`, ecc.            |
| format         | string | query                            | Sì           | Format di output desiderato. Valori supportati: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.                        |

### **Risposta**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Codici di stato HTTP**

| Codice | Significato                     | Descrizione                                      |
|--------|----------------------------------|--------------------------------------------------|
| 200    | OK                               | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida             | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato                  | Token JWT non valido o mancante. |
| 413    | Payload troppo grande            | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server        | Errore imprevisto del server. |

## Come utilizzare l'API PostExport con gli SDK

### Specifica dell'API PostExport

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare direttamente interazioni REST da un browser web.

Tutte le richieste devono includere un token OAuth 2.0 Bearer valido nell'intestazione `Authorization`. L'esempio seguente mostra come chiamare l'API con **cURL** e caricare un foglio di calcolo usando multipart/form‑data.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti permette di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}