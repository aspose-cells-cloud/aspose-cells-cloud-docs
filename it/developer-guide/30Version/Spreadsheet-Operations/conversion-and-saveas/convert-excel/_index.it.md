---
title: "Convertire un file Excel in diversi formati"
ArticleTitle: "Convertire un file Excel in diversi formati"
second_title: "Documento"
linktype: "Converti Excel"
type: docs
url: /it/convertire-un-file-excel-in-diversi-formati/
aliases:
  [
    /convertire-un-libro-di-lavoro-excel-in-diversi-formati-file/,
    /converti/excel-in-diversi-formati/,
  ]
keywords: "Aspose.Cells Cloud, conversione Excel, conversione formati file, API REST, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Converti libri di lavoro Excel in formati come CSV, PDF, HTML, JSON, Markdown e altri utilizzando l'API REST Aspose.Cells Cloud."
weight: 10
---

Prima di chiamare questa endpoint, assicurati di aver ottenuto un token JWT valido e che il libro di lavoro sorgente sia memorizzato in una posizione di archiviazione supportata (ad esempio, Aspose Cloud Storage). Includi il token nell'header `Authorization` e, se necessario, specifica il parametro di query `storageName`.

Questa API REST converte un file Excel in vari formati di output.

## API PutConvertWorkBook

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

La richiesta è un HTTP **PUT** con contenuto multipart (vedi [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La prima parte del corpo multipart contiene il **file dati**, mentre la seconda parte contiene le **opzioni di salvataggio**.

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri di query

| Nome parametro          | Tipo   | Descrizione                                                                                                                |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | Format di file di destinazione (ad esempio, CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, ecc.).      |
| `password`              | string | Password necessaria per aprire il file Excel sorgente.                                                                           |
| `outPath`               | string | Percorso completo (incluso nome file ed estensione) per un singolo file di output, oppure un percorso di cartella quando vengono generati più file. |
| `storageName`           | string | Nome dell'archiviazione in cui risiede il file sorgente.                                                                         |
| `checkExcelRestriction` | bool   | Se **true**, convalida le restrizioni di Excel prima di modificare celle o oggetti correlati.                                     |
| `streamFormat`          | string | Formato del flusso di file in ingresso.                                                                                           |
| `region`                | string | Impostazioni regionali applicate al libro di lavoro.                                                                                 |
| `pageWideFitOnPerSheet` | bool   | Regola la larghezza della pagina per adattarla a ogni foglio di calcolo durante la conversione in PDF.                                                           |
| `pageTallFitOnPerSheet` | bool   | Regola l'altezza della pagina per adattarla a ogni foglio di calcolo durante la conversione in PDF.                                                          |
| `sheetName`             | string | Nome del foglio di calcolo da convertire.                                                                                          |
| `pageIndex`             | string | Indice della pagina da convertire (richiede `sheetName`).                                                                       |
| `onePagePerSheet`       | bool   | Se **true**, genera una pagina PDF per ogni foglio di calcolo.                                                                       |
| `AutoRowsFit`           | bool   | Adatta automaticamente tutte le righe nel libro di lavoro.                                                                                        |
| `AutoColumnsFit`        | bool   | Adatta automaticamente la larghezza delle colonne nel libro di lavoro.                                                                                   |

### Parametri del corpo della richiesta

| Nome parametro | Tipo      | Descrizione                                                    |
| -------------- | --------- | -------------------------------------------------------------- |
| `datafile`     | data file | Il file Excel inserito nella prima parte del corpo multipart. |
| `SaveOptions`  | object    | Opzioni di salvataggio inserite nella seconda parte del corpo multipart.  |

### **Risposta**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Codici di stato HTTP**

| Codice | Significato                     | Descrizione                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida                 | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato                | Token JWT non valido o mancante. |
| 413  | Payload troppo grande           | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server       | Errore imprevisto del server. |
## Come utilizzare l'API PutConvertWorkBook con gli SDK

### Specifica dell'API PutConvertWorkBook

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) definiscono un'interfaccia accessibile pubblicamente che consente interazioni REST dirette da un browser web.

### Esempio cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK accelera lo sviluppo gestendo i dettagli a basso livello, consentendoti di concentrarti sulla logica aziendale. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells con vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---