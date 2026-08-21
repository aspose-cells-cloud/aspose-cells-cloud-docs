---
title: "Esporta forme"
second_title: "Documento"
linktitle: "Forma"
type: docs
url: /it/export-excel-shape-to-different-formats/
aliases: [  /it/export/excel-shape-to-different-formats/ ]
keywords: "Esporta forme, Aspose.Cells Cloud, Esportazione forma Excel, Formati immagine, REST API, SDK"
description: "Scopri come esportare forme Excel in vari formati immagine (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) utilizzando l'API REST di Aspose.Cells Cloud e gli SDK."
weight: 20
ArticleTitle: "Esporta forme – Aspose.Cells Cloud"
---

Esportare forme da Excel consente di riutilizzare contenuti diagrammatici su diverse piattaforme e applicazioni. **Prerequisiti:** un token di accesso JWT valido e il file Excel di origine da caricare.

È possibile esportare forme nei seguenti formati: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## API PostExport

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.


### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Obbligatorio | Descrizione |
|----------------|--------|----------------------------------|--------------|-------------|
| file           | file   | formData                         | Sì           | File da caricare |
| objectType     | string | query                            | Sì           | Tipo di oggetto da esportare. Per l'esportazione di grafici utilizzare `chart`. I valori validi includono `shape`, `worksheet`, `picture`, ecc. |
| format         | string | query                            | Sì           | Format di output desiderato. Valori supportati: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **Esempio di richiesta**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Risposta

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... altri oggetti file ...
  ]
}
```

*I payload di file tipici codificati in Base64 variano da poche centinaia di byte a diversi megabyte, a seconda delle dimensioni dell’immagine e del formato.*

**Codici di stato HTTP**

| Codice | Significato           | Descrizione |
|--------|-----------------------|-------------|
| 200    | OK                    | Forme esportate correttamente; la risposta contiene l'elenco dei file. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi. |
| 401    | Non autorizzato       | Token di accesso non valido o mancante. |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno server | Errore imprevisto sul server. |


## Come utilizzare l'API PostExport con gli SDK

### Specifica dell'API PostExport

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud tramite cURL.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare con Aspose.Cells Cloud. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulla logica di business. Consulta la [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}