---
title: "Aspose.Cells Cloud API – Ottieni elenco file (contenuto cartella)"
description: "Recupera un elenco di file e sottocartelle da una specifica cartella nell'archivio cloud di Aspose.Cells."
keywords:
  - Aspose.Cells
  - API
  - Ottieni elenco file
  - Archiviazione cloud
  - Excel
  - REST
type: docs
weight: 100
---

L'operazione **Ottieni elenco file** restituisce la raccolta di file e sottocartelle memorizzate in una cartella specifica dell'archivio cloud di Aspose.Cells.  
Rappresenta il punto di ingresso principale per esplorare cartelle di fogli di calcolo Excel, archivi e altri tipi di file supportati nel cloud.

## Aspose.Cells Cloud API – Ottieni elenco file (contenuto cartella)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome            | Posizione | Tipo    | Obbligatorio | Descrizione                                                                   |
| --------------- | --------- | ------- | ------------ | ----------------------------------------------------------------------------- |
| **path**        | Path      | stringa | Sì           | Percorso della cartella nell'archivio cloud.                                  |
| **storageName** | Query     | stringa | No           | Nome dell'archivio da utilizzare. Se omesso, viene usato l'archivio predefinito. |
| **pageSize**    | Query     | intero  | No           | Numero massimo di elementi da restituire per pagina (valore predefinito: 100). |
| **pageNumber**  | Query     | intero  | No           | Numero di pagina da recuperare (inizia da 1, valore predefinito: 1).          |

- **Valore** – Array di oggetti `StorageFile`. Ciascun oggetto contiene:
  - `Name` – Nome del file o della cartella.
  - `IsFolder` – `true` se l'elemento è una cartella.
  - `Size` – Dimensione in byte (le cartelle riportano `0`).
  - `ModifiedDate` – Data e ora dell'ultima modifica (formato ISO 8601).

### **Risposta**

**Codici di stato HTTP**

| Codice HTTP | Stato HTTP            | Descrizione                                                              |
| ----------- | --------------------- | ------------------------------------------------------------------------ |
| 200         | OK                    | L'API Web è stata richiamata correttamente; la risposta contiene i dettagli dell'operazione. |
| 400         | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401         | Non autorizzato       | Token JWT non valido o mancante.                                         |
| 413         | Payload troppo grande | Il file caricato supera il limite di dimensione.                        |
| 500         | Errore interno del server | Errore imprevisto nel server.                                          |
|             |                       |                                                                          |

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK: