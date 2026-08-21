---
title: "Convertire un file Excel in formati diversi"
second_title: "Documento"
linktitle: "Convertire foglio di calcolo"
type: docs
url: /it/convert-a-spread-file-to-different-formats/
keywords: "conversione Excel, conversione foglio di calcolo, Aspose.Cells Cloud, API REST, PDF, CSV, JSON, Markdown, conversione formato file"
description: "Usa l'API REST Aspose.Cells Cloud per convertire cartelle di lavoro Excel in formati diversi come PDF, CSV, JSON e Markdown. L'API supporta diversi SDK per linguaggi come C#, Java, Python e altri."
weight: 10
ArticleTitle: "Convertire un file Excel in formati diversi – Guida API Aspose.Cells Cloud"
---

Questa API REST consente di convertire un file Excel in un formato diverso. Supporta un'ampia gamma di formati di output e permette di impostare le opzioni di configurazione della pagina e di salvataggio prima della conversione.

## API PostConvertWorkBook

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

Prima di utilizzare questa API, assicurati di disporre di un token JWT valido e di aver installato l'SDK Aspose.Cells Cloud appropriato per il tuo linguaggio di programmazione.

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

## Come usare l'API PostConvertWorkBook con gli SDK

### Specifica dell'API PostConvertWorkBook

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come richiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Usare gli SDK Aspose.Cells Cloud

Utilizzare un SDK rappresenta il modo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, permettendoti di concentrarti sul tuo progetto. Consulta la [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}