---
title: "Aspose.Cells Cloud Get File Versions API – Recupero rapido della cronologia delle versioni dei file"
second_title: "Documento"
ArticleTitle: "Gestione Excel basata su cloud – Recupera rapidamente la cronologia delle versioni dei file in Aspose.Cells Cloud"
linktitle: "Ottieni versioni file"
type: docs
url: /it/get-file-versions/
keywords: "Aspose Cells API, versioni file, versionamento fogli di calcolo, API di archiviazione cloud, REST, cronologia file Excel"
description: "Ottieni un elenco completo della cronologia delle versioni per qualsiasi file Excel archiviato in Aspose.Cells Cloud. Supporta la selezione dell'archiviazione, l'autenticazione e codici di errore dettagliati."
weight: 100
---

Recupera un elenco completo di record di versione per un foglio di calcolo specifico archiviato in Aspose.Cells Cloud. Questo endpoint consente agli sviluppatori di tenere traccia delle modifiche, di verificare le modifiche effettuate e di implementare flussi di lavoro di controllo delle versioni direttamente dall'archiviazione cloud.

L'API **GetFileVersions** restituisce tutti i record di versione per un foglio di calcolo specifico archiviato in Aspose.Cells Cloud. Ti aiuta a mantenere una cronologia completa delle modifiche per ogni file.

## **Excel API: Ottieni versioni file**

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### I parametri della richiesta dell'API **GetFileVersions** sono

| Nome parametro | Tipo   | Posizione | Descrizione                                                                                 |
| -------------- | ------ | -------- | ------------------------------------------------------------------------------------------- |
| `path`         | Stringa | Path     | **Obbligatorio.** Percorso completo del file di cui si desidera recuperare le versioni.     |
| `storageName`  | Stringa | Query    | Opzionale. Nome dell'archiviazione contenente il file. Se omesso, viene utilizzata l'archiviazione predefinita. |

### **Risposta**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contiene un elenco delle versioni dei file per il documento specificato."
  ],
  "Type": "Classe",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["Una raccolta di dettagli sulla versione del file."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Classe",
          "Reference": "FileVersion",
          "Name": "classe:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

In caso di esito positivo, l'API restituisce **HTTP 200 OK** con un payload JSON contenente l'array `Value` di oggetti versione file, come illustrato sopra.

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) fornisce un'interfaccia di programmazione completa per eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK semplifica lo sviluppo astrayendo le complessità di basso livello, consentendo agli sviluppatori di concentrarsi sulle funzionalità principali. Esplora il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come interagire con i servizi web di Aspose.Cells in vari linguaggi di programmazione:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}

---