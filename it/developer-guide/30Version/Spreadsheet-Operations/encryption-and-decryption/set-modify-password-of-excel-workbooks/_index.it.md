---
---
title: "Modifica la protezione tramite password di un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Modifica la password di un file Excel"
type: docs
url: /workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "password Excel, Aspose.Cells Cloud, protezione in scrittura, API REST, modifica password foglio di lavoro"
description: "Cambia la password di protezione in scrittura di un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include esempi in cURL e SDK."
weight: 100
ArticleTitle: "Modifica la protezione tramite password di un foglio di lavoro Excel – Aspose.Cells Cloud"
---

Questa API REST **modifica la password di protezione in scrittura** di un foglio di lavoro Excel esistente.

Aggiornare programmaticamente la password di protezione in scrittura consente di ruotare o sostituire le password senza scaricare il file. Questo approccio risulta particolarmente utile quando si gestiscono fogli di lavoro protetti memorizzati nello storage di Aspose.Cells Cloud.


## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### Sicurezza e autenticazione

Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Parametri della richiesta

| Nome del parametro | Tipo   | Posizione    | Descrizione                                      |
| ------------------ | ------ | ------------ | ------------------------------------------------ |
| **name**           | string | path         | Nome del foglio di lavoro Excel (obbligatorio).  |
| **password**       | string | body (JSON)  | Nuova password di protezione in scrittura da impostare (obbligatoria). |
| **folder**         | string | query        | Cartella opzionale in cui è memorizzato il foglio di lavoro. |
| **storageName**    | string | query        | Nome opzionale del servizio di storage.          |

### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | File caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

## Come utilizzare l'API PutDocumentProtectFromChanges con gli SDK

### Specifica dell'API PutDocumentProtectFromChanges

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) definiscono l'interfaccia di programmazione accessibile pubblicamente che consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. Il comando cURL riportato di seguito mostra come richiamare l'API Cloud.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
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

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}