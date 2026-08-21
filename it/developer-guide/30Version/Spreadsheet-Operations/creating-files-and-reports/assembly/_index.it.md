---
title: "Assemblaggio dei dati per la creazione di un report Excel"
second_title: "Documento"
linktitle: "Assemblaggio dati"
type: docs
url: /it/assembly-data-for-the-creation-of-an-excel-report/
aliases: [  /it/assembly/ ]
keywords: "Aspose.Cells, report Excel, assemblaggio dati, API cloud, REST, SDK, cURL, PDF, ODS"
description: "Scopri come utilizzare l'API di assemblaggio di Aspose.Cells Cloud per unire dati in report Excel (XLSX, PDF, ODS). Include endpoint, parametri, esempio cURL, codice SDK, guida all'autenticazione e gestione degli errori."
weight: 40
---

Questa API REST assembla i dati **all'interno** di un file Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione tramite token JWT</a>.

### Parametri della richiesta


| Nome parametro | Tipo   | Posizione                  | Descrizione                                                           |
| ---------------- | ------ | ------------------------- | ---------------------------------------------------------------------- |
| file             | file   | formData (corpo multipart) | Il file del foglio elettronico da caricare.                           |
| DataSource       | string | query string              | Identificatore della fonte dati che fornisce i dati per l'assemblaggio. |
| format           | string | query string              | Formato di output desiderato (ad esempio, `xlsx`, `pdf`).              |

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nome file2]",
    "Filesize" : [dimensione file],
    "FileContent" : "[Base64String]"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                |
|--------|-----------------------------|------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                           |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.          |
| 500    | Errore interno del server   | Errore imprevisto nel server.                              |

## Come utilizzare l'API PostAssemble con gli SDK

### Specifica dell'API PostAssemble

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare interfacce verso l'API. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica aziendale. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}