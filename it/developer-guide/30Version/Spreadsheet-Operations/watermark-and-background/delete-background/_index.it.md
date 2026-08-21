---
title: "Elimina lo sfondo di un workbook Excel"
second_title: "Documento"
linktitle: "Elimina"
type: docs
url: /it/delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells elimina sfondo, Excel API elimina sfondo, Aspose.Cells Cloud, DELETE /cells background"
description: "Rimuovi un'immagine di sfondo da un workbook Excel utilizzando l'API Aspose.Cells Cloud. Scopri l'endpoint DELETE, i parametri richiesti, l'esempio cURL e il codice SDK in C#, Java, Python e altro."
weight: 170
ArticleTitle: "Elimina l'immagine di sfondo da un workbook Excel utilizzando l'API Aspose.Cells Cloud"
---

Questa API REST elimina l'immagine di sfondo di un workbook Excel.

## API DeleteWorkbookBackground

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della query**

| Nome parametro | Tipo   | Descrizione                                              | Obbligatorio |
| -------------- | ------ | -------------------------------------------------------- | ------------ |
| folder         | string | Cartella che contiene il workbook originale.             | No           |
| storageName    | string | Nome del servizio di archiviazione da utilizzare.        | No           |

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                           |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                          |
| 500    | Errore interno del server   | Errore imprevisto sul server.                                              |

## Come utilizzare l'API DeleteWorkbookBackground con gli SDK

### Specifica dell'API DeleteWorkbookBackground

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione accessibile pubblicamente che consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra una richiesta DELETE completa con l'intestazione di autenticazione richiesta; non è necessario alcun corpo di richiesta.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}