---
title: "Aggiungi una filigrana ai file Excel"
second_title: "Documento"
linktitle: "Aggiungi una filigrana ai file Excel"
type: docs
url: /it/add-watermark-into-excel-files/
aliases: [  /it/watermark/ ]
keywords: "aggiungi filigrana a Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Scopri come aggiungere una filigrana di testo ai fogli di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include un esempio cURL, i parametri obbligatori e i dettagli della risposta."
weight: 39
ArticleTitle: "Aggiungi una filigrana ai file Excel – Documentazione di Aspose.Cells Cloud"
---

Questa API REST aggiunge una **filigrana** ai file Excel.

**Prerequisiti:** Devi ottenere un token di accesso JWT valido e assicurarti che il file Excel sia in un formato supportato (ad esempio, `.xlsx`, `.xls`).  
**Panoramica:** Una filigrana è un sovraimpressione di testo semitrasparente applicata a ogni foglio di lavoro per indicare la proprietà o la riservatezza.

## API PostWatermark

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione                  | Descrizione                                                 |
| -------------- | ------ | ------------------------- | ----------------------------------------------------------- |
| `file`         | file   | formData (corpo multipart) | Il file Excel a cui verrà applicata la filigrana.           |
| `text`         | string | query                     | Il testo della filigrana da visualizzare.                   |
| `color`        | string | query                     | Il colore della filigrana in formato esadecimale ARGB (ad esempio, `004433ff`). |

### **Risposta**

La risposta JSON contiene un array **Files**. Per ogni oggetto file:

- **Filename** – nome del foglio di calcolo elaborato.  
- **FileSize** – dimensione del file in byte.  
- **FileContent** – contenuto codificato in Base64 del file Excel con filigrana; decodificalo per ottenere il file effettivo.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[nome file1]",
            "Filesize" : [dimensione file],
            "FileContent" : "[StringaBase64]"
        },        {
            "Filename" : "[nome file2]",
            "Filesize" : [dimensione file],
            "FileContent" : "[StringaBase64]"
        },        {
            "Filename" : "[nome file3]",
            "Filesize" : [dimensione file],
            "FileContent" : "[StringaBase64]"
        }
    ]
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filigrana applicata con successo; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

## Come utilizzare l'API PostWatermark con gli SDK

### Specifica dell'API PostWatermark

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per chiamare i servizi web di Aspose.Cells. L'esempio seguente mostra una richiesta completa, inclusa l'intestazione di autenticazione obbligatoria. Sostituisci `<your-jwt-token>` con un token di accesso JWT valido ottenuto dall'endpoint di autenticazione di Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----StringaBase64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulla logica aziendale. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}