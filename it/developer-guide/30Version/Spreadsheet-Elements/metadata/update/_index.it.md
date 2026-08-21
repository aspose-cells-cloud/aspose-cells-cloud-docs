---
title: "Aggiornare i metadati"
second_title: "Documento"
linktype: "Aggiornare senza utilizzare l'archiviazione"
type: docs
url: /it/metadata/update/
keywords: "metadati, Excel, Aspose.Cells Cloud, REST API, aggiornamento, foglio di calcolo"
description: "L'API REST di Aspose.Cells Cloud consente di aggiornare i metadati nei file Excel. Supporta diversi SDK (C#, Java, Python, Ruby, Go, ecc.) per un'integrazione fluida tra vari linguaggi di programmazione."
weight: 35
ArticleTitle: "Aggiornare i metadati – Documentazione dell'API Aspose.Cells Cloud"
---

Questa API REST aggiorna i **metadati** in più file Excel.

**Prerequisiti:** Un account Aspose Cloud attivo, un token di accesso JWT valido e i file Excel da caricare.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro     | Tipo   | Posizione         | Descrizione                                     |
| ------------------ | ------ | ---------------- | ----------------------------------------------- |
| file               | file   | formData         | Il file Excel da caricare.                      |
| DocumentProperties | object | Corpo HTTP (JSON) | Proprietà del documento da impostare per il file Excel. |

**Note:** È possibile caricare fino a 10 file in una singola richiesta. I formati supportati includono `.xlsx`, `.xls` e `.csv`. La dimensione totale della richiesta non deve superare i 100 MB.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PostMetadata) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

La richiesta richiede un'intestazione **Authorization** con un token Bearer JWT. Assicurati che il token venga generato utilizzando le credenziali client del tuo account Aspose Cloud.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----StringaBase64--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----StringaBase64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Vedi anche:**  
- [Ottenere i metadati](/metadata/get/)  
- [Eliminare i metadati](/metadata/delete/)  
---