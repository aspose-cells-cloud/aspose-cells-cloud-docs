---
title: "Ottenere i metadati dai file Excel"
second_title: "Documento"
linktitle: "Ottenere senza utilizzare l'archiviazione"
type: docs
url: /it/metadata/get/
keywords: "Aspose.Cells, Excel, metadati, REST API, cloud SDK"
description: "Recupera i metadati integrati o personalizzati dai file Excel utilizzando l'API REST Aspose.Cells Cloud. Include il formato della richiesta, i parametri, il codice di esempio per gli SDK e la gestione degli errori."
weight: 23
ArticleTitle: "Ottenere i metadati dai file Excel - Aspose.Cells Cloud API"
---

Questa API REST recupera i **metadati** da uno o più file Excel.  
La richiesta deve includere l'intestazione `Authorization: Bearer <access_token>`, ottenuta tramite il flusso OAuth 2.0 client-credentials.

**Prerequisiti**: Per chiamare questo endpoint è necessario disporre di un token di accesso valido ottenuto dall'endpoint dei token OAuth 2.0 di Aspose Cloud. Esempio di richiesta curl per ottenere un token:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### Parametro di query

| Nome parametro | Tipo   | Descrizione                                                                 |
| -------------- | ------ | --------------------------------------------------------------------------- |
| type           | string | `ALL` / `BuiltIn` / `Custom` – specifica quali gruppi di metadati restituire. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo      | Descrizione                                                       |
| -------------- | --------- | ----------------------------------------------------------------- |
| excel file     | data file | Il file Excel fornito come prima parte della richiesta multipart. |

### Risposta

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| Codice | Significato             | Quando                            |
|------|-------------------------|-----------------------------------|
| 200  | Successo                | Metadati restituiti.              |
| 400  | Richiesta non valida    | File mancante o query non valida. |
| 401  | Non autorizzato         | Token non valido o mancante.      |
| 404  | Non trovato             | File specificato non trovato.     |
| 500  | Errore interno del server | Fallimento imprevisto del server. |

L'API restituisce questi codici di stato HTTP standard insieme a un oggetto JSON di risposta di errore, quando applicabile.

### Famiglia di SDK cloud

L'utilizzo di un SDK accelera lo sviluppo gestendo i dettagli a basso livello. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}