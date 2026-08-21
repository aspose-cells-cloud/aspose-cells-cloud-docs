---
---
title: "Rimuovere la protezione da scrittura (password) da un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Rimuovere la password dai file Excel"
type: docs
url: /it/clear-excel-files-password/
aliases:
  [
    "/it/clear-modify-password-of-excel-workbooks/",
    "/it/workbook/clear-modify-password/",
    "/it/workbook/password/clear/",
  ]
keywords: "Aspose.Cells, Excel, rimozione password, protezione da scrittura, API REST, esempi SDK"
description: "Scopri come rimuovere la protezione da scrittura (password) da un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempio cURL, passaggi per l'autenticazione e codice di esempio per gli SDK."
weight: 110
ArticleTitle: "Rimuovere la protezione da scrittura (password) da un foglio di lavoro Excel"
---

Questa API REST rimuove la **protezione da scrittura (password)** da un foglio di lavoro Excel, consentendo di **rimuovere la protezione tramite password** in modo programmatico.

**Prerequisiti:** Ottenere un token JWT valido, assicurarsi che il foglio di lavoro sia memorizzato in una posizione di archiviazione supportata e utilizzare la versione API v3.0.

Per aggiungere protezione, consulta la guida [Proteggi Excel](/it/cells/protect/).

## API DeleteDocumentUnprotectFromChanges

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **Sicurezza e autenticazione**

Le API REST di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                           |
| -------------- | ------ | --------- | ----------------------------------------------------- |
| `name`         | string | path      | Nome del foglio di lavoro Excel.                      |
| `folder`       | string | query     | Cartella contenente il foglio di lavoro (opzionale).  |
| `storageName`  | string | query     | Nome del servizio di archiviazione (opzionale).       |


### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                               |
|--------|-----------------------------|-----------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                          |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.         |
| 500    | Errore interno del server   | Errore imprevisto nel server.                             |

## Come utilizzare l'API DeleteDocumentUnprotectFromChanges con gli SDK

### Specifica dell'API DeleteDocumentUnprotectFromChanges

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) definiscono un'interfaccia di programmazione accessibile pubblicamente e permettono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi Aspose.Cells Cloud. L'esempio seguente mostra come effettuare una chiamata all'API REST tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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


### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}