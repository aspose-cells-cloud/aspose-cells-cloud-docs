---
title: "Aspose.Cells Cloud Upload File API – Un'interfaccia per il caricamento rapido di file nel cloud"
second_title: "Documento"
ArticleTitle: "Aspose.Cells Cloud Upload File API – Un'interfaccia per il caricamento rapido di file nel cloud"
linktitle: "Carica file"
type: docs
url: /upload-file/
keywords: "Aspose.Cells, caricamento file, API Excel, archiviazione cloud, API REST"
description: "Guida al caricamento di file tramite l'API Aspose.Cells Cloud, con copertura di parametri di richiesta, codici di stato HTTP, gestione degli errori ed esempi di codice."
weight: 100
---

L'API **uploadFile** consente agli sviluppatori di caricare direttamente i file nell'archiviazione cloud per l'elaborazione con Aspose Cells.

## **Aspose Cells API: Carica file**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### I parametri della richiesta dell'API **uploadFile** sono

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                   |
| :------------- | :----- | :------------------------------ | :-------------------------------------------------------------------------------------------- |
| UploadFiles    | File   | FormData                        | Carica file nell'archiviazione cloud.                                                        |
| path           | String | Percorso                        | Il percorso di destinazione nell'archiviazione cloud. Specificare il percorso in cui caricare il file. |
| storageName    | String | Query                           | Il nome dell'archiviazione in cui verrà caricato il file.                                   |

### **Risposta**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["Risultato del caricamento del file"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["Elenco dei nomi dei file caricati"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["Elenco degli errori."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

L'API restituisce i seguenti codici di stato HTTP:

| Codice di stato               | Descrizione                                         |
| ----------------------------- | --------------------------------------------------- |
| **200 OK**                    | File caricato correttamente.                        |
| **400 Bad Request**           | Parametri non validi o richiesta malformata.        |
| **401 Unauthorized**          | Token di autenticazione mancante o non valido.      |
| **403 Forbidden**             | Permessi insufficienti per l'archiviazione specificata. |
| **500 Internal Server Error** | Errore imprevisto del server.                       |

## Come utilizzare l'API per il caricamento file con gli SDK?

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) forniscono una descrizione dettagliata dell'API, consentendo agli sviluppatori di interagire direttamente con essa tramite un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK migliora l'efficienza dello sviluppo gestendo i dettagli a basso livello, consentendo agli sviluppatori di concentrarsi sulle attività del progetto. Visita il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**Vedi anche**

- [API Download File](/download-file/) – Recupera un file dall’archiviazione cloud.
- [API Copy File](/copy-file/) – Duplica un file all’interno dell’archiviazione cloud.
- [API Delete File](/delete-file/) – Rimuovi un file dall’archiviazione cloud.