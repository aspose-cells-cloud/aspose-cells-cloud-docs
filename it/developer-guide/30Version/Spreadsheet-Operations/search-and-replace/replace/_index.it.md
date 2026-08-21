---
title: "Sostituisci il testo nei file Excel"
second_title: "Documento"
linktitle: "Sostituisci senza utilizzare l'archiviazione"
type: docs
url: /it/replace/
keywords: "sostituisci testo in Excel, Aspose.Cells Cloud, API REST, sostituisci foglio di calcolo, API, sostituzione testo in file Excel"
description: "Utilizza l'API REST di Aspose.Cells Cloud per sostituire il testo esistente con nuovi valori nei file Excel. Supporta SDK per C#, Java, Python, Node.js, PHP, Ruby, Go e Perl."
weight: 80
---


## API REST

Questa API REST sostituisce i dati nei file Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### Sicurezza e autenticazione

Le API REST di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Parametri della richiesta

| Nome parametro | Tipo   | Posizione             | Descrizione                                           |
| -------------- | ------ | -------------------- | ----------------------------------------------------- |
| **file**       | file   | formData (multipart) | File Excel da elaborare.                              |
| **text**       | string | query                | Stringa di testo da sostituire.                       |
| **newtext**    | string | query                | Testo di sostituzione.                                |
| **password**   | string | query                | Password per un workbook protetto (opzionale).       |
| **sheetname**  | string | query                | Nome del foglio di calcolo da interessare (opzionale). |

### **Risposta**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[nome file1]",
      "Filesize" : [dimensione file],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[nome file2]",
      "Filesize" : [dimensione file],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[nome file3]",
      "Filesize" : [dimensione file],
      "FileContent" : "[Base64String]"
    }
  ]
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                |
|--------|-----------------------------|------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                           |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.          |
| 500    | Errore interno del server   | Errore imprevisto del server.                              |

## Come utilizzare l'API PostReplace con gli SDK

### Specifica dell'API PostReplace

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) definiscono un'interfaccia di programmazione accessibile pubblicamente e permettono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK per il Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}