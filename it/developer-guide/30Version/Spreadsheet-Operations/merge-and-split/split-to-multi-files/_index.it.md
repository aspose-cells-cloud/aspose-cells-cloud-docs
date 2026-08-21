---
title: "Dividi un file Excel in più file"
second_title: "Document"
linktitle: "Dividi file Excel multipli"
type: docs
url: /split-an-excel-file-to-multi-files/
aliases: [/split-excel-workbooks/,/workbook/split/]
keywords: "Aspose.Cells, Cloud, Excel, Split, API, PDF, CSV, JSON"
description: "Utilizza l'API REST di Aspose.Cells Cloud per dividere i file Excel con più fogli in file separati. Supporta formati di output come PDF, CSV e JSON, ed è disponibile tramite SDK per Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift."
weight: 32
ArticleTitle: "Dividi un file Excel in più file - Documentazione di Aspose.Cells Cloud"
---

L'API REST di Aspose.Cells Cloud divide i file Excel con più fogli in file separati.

**Prerequisiti**  
Prima di chiamare l'API, è necessario ottenere un token JWT valido e includerlo nell'intestazione `Authorization` di ogni richiesta. Consulta la [guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) per i dettagli.

## API PostSplit

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.


### Parametri della richiesta

| Nome Parametro | Tipo   | Posizione  | Descrizione                                                        |
|----------------|--------|------------|--------------------------------------------------------------------|
| file           | file   | formData   | Il file Excel da caricare.                                         |
| format         | string | query      | Formato di output desiderato (ad esempio, `pdf`, `csv`, `json`).   |
| password       | string | query      | Password per un file Excel crittografato (opzionale).              |
| from           | integer| query      | Indice del primo foglio da includere (in base 1).                  |
| to             | integer| query      | Indice dell'ultimo foglio da includere (inclusivo).               |

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[nome file1]",
            "Filesize" : [dimensione file],
            "FileContent" : "[StringaBase64]"
        },
        {
            "Filename" : "[nome file2]",
            "Filesize" : [dimensione file],
            "FileContent" : "[StringaBase64]"
        },
        {
            "Filename" : "[nome file3]",
            "Filesize" : [dimensione file],
            "FileContent" : "[StringaBase64]"
        }
    ]
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                  |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                             |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.             |
| 500    | Errore interno del server   | Errore imprevisto sul lato server.                           |

## Come utilizzare l'API PostSplit con gli SDK

### Specifica dell'API PostSplit

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

**Codici di stato HTTP**

| Codice | Significato                   | Descrizione                                                       |
|--------|-------------------------------|-------------------------------------------------------------------|
| 200    | OK                            | Il file Excel è stato diviso correttamente e la risposta contiene l'elenco dei file. |
| 400    | Richiesta non valida          | Parametri mancanti o non validi (ad esempio, formato non supportato). |
| 401    | Non autorizzato               | Token JWT non valido o mancante.                                  |
| 500    | Errore interno del server     | Si è verificato un errore imprevisto lato server.                |

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# Sostituisci xxxxx1.xlsx e xxxxx2.xlsx con i percorsi dei tuoi file Excel
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----StringaBase64--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----StringaBase64--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---