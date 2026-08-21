---
title: "Convertire Excel in PPTX tramite Aspose.Cells Cloud API v3.0"
second_title: "Documento"
linktitle: "Excel in PPTX"
type: docs
url: /it/convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, conversione, REST API, cloud"
description: "Scopri come convertire file di cartelle di lavoro Excel in presentazioni PPTX tramite l'API REST Aspose.Cells Cloud v3.0. Include richieste cURL, esempi di codice SDK, autenticazione e gestione degli errori."
weight: 90
ArticleTitle: "Convertire Excel in PPTX tramite Aspose.Cells Cloud API v3.0"
---

Questa API REST converte un file foglio elettronico nel formato PPTX.

## API PostConvertWorkbookToPptx

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della query

| Nome parametro          | Tipo   | Descrizione                                                                                  |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------- |
| `password`              | string | Password necessaria per aprire la cartella di lavoro Excel.                                  |
| `storageName`           | string | Nome dello storage in cui si trova il file sorgente.                                         |
| `checkExcelRestriction` | bool   | Indica se applicare le restrizioni dei file Excel quando si modificano oggetti legati alle celle. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo      | Descrizione                                                              |
| -------------- | --------- | ------------------------------------------------------------------------ |
| `datafile`     | file dati | Il file Excel incluso nella prima parte del corpo della richiesta multipart. |

**Esempio di corpo richiesta multipart (semplificato):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<contenuto binario di input.xlsx>
--boundary
Content-Disposition: form-data; name="password"

LaMiaPwd
--boundary--
```

### Risposta

L'API restituisce un oggetto **FileInfo** contenente il file pptx generato.

| Campo           | Tipo   | Descrizione                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Nome del file pptx (ad esempio, `esempio.pptx`). |
| **FileSize**    | int    | Dimensione del file in byte.                  |
| **FileContent** | string | Contenuto del file pptx codificato in Base64. |

[FileInfo](/cells/file-info/)

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto sul server. |

*Note:* L'endpoint supporta i formati Excel comuni (`.xlsx`, `.xls`, `.xlsm`). La dimensione massima del file è limitata a 50 MB. La conversione potrebbe essere limitata per cartelle di lavoro contenenti macro o fogli protetti, a meno che i parametri appropriati non vengano forniti.

## Come utilizzare l'API PostConvertWorkbookToPptx con gli SDK

### Specifica dell'API PostConvertWorkbookToPptx

La <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/percorso/di/input.xlsx" \
     -F "password=LaMiaPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "esempio.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: stringa_codificata_in_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud" rel="noopener noreferrer") per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Altre API che implementano questa funzionalità

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Converte un file Excel in PDF.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Converte un file Excel in immagini PNG.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Converte un file Excel in formato SVG.