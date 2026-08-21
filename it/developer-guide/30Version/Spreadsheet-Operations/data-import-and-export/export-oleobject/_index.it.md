---
title: "Esporta oggetto OLE – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Oggetto OLE"
type: docs
url: /it/export-excel-ole-object/
aliases: [  /it/export/excel-ole-object/ ]
keywords: "Aspose.Cells, oggetto OLE, esportazione, Excel, API cloud, PDF, PNG, DOCX, PPTX"
description: "Esporta oggetti OLE da un foglio di calcolo Excel utilizzando l'API cloud Aspose.Cells. Scopri il formato della richiesta, i parametri, un esempio cURL e la gestione degli errori."
weight: 20
ArticleTitle: "Esporta oggetto OLE – Aspose.Cells Cloud API"
---

## **API REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicurezza e autenticazione**

Le API cloud di Aspose.Cells sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.


### Parametri della richiesta

| Parametro       | Posizione   | Tipo   | Obbligatorio | Descrizione                                                                          |
| --------------- | --------- | ------ | ------------ | ------------------------------------------------------------------------------------ |
| `file`          | Form‑data | file   | Sì           | Il foglio di calcolo Excel (`.xlsx`, `.xls`, ecc.) contenente gli oggetti OLE.      |
| `outputFormat`  | Query     | string | Sì           | Formato di destinazione per gli oggetti esportati (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`    | Query     | string | Sì           | Valore fisso `oleobject`.                                                            |


### Risposta

Una richiesta riuscita restituisce un oggetto JSON contenente l'elenco dei file esportati:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato).         |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                           |
| 500    | Errore interno del server   | Errore imprevisto nel server.                                               |

## Come utilizzare l'API PostExport con gli SDK

### Specifica dell'API PostExport

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API cloud con cURL.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### Cos'è un oggetto OLE?

Un **oggetto OLE (Object Linking and Embedding)** incorpora contenuti esterni—come documenti Word, diapositive PowerPoint, immagini o altri file—in un foglio di calcolo Excel. Quando viene esportato, il contenuto incorporato viene estratto e salvato nel formato di output richiesto.

### Panoramica dell'endpoint

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – Deve essere impostato su `oleobject`.
- `format` – Formato di output desiderato (es. `pdf`, `png`, `jpeg`, `docx`, `pptx`).

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---