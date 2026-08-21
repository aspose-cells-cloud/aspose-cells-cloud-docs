---
title: "Riparazione di file Excel"
second_title: "Documenti"
type: docs
linktitle: "Riparazione di file Excel"
url: /it/repair-excel-files/
keywords: "Aspose Cells, API per la riparazione di Excel, XLSX corrotto, recupero fogli di calcolo, API cloud"
description: "Utilizza l'API REST di Aspose.Cells Cloud per riparare file Excel danneggiati (XLS, XLSX, XLSM, XLSB, ODS). Carica uno o più file, scegli il formato di output e ricevi i file riparati in formato Base64. Nessuna installazione richiesta."
weight: 39
---

Questa API REST consente di **riparare** file Excel.

- Ripara i formati XLS, XLSX, XLSM, XLSB, ODS e altri formati di foglio di calcolo.  
- Supporta il caricamento di più file in una singola richiesta.

Aspose.Cells Cloud Excel Repair recupera i dati da file Excel danneggiati online, senza alcuna installazione. I file Excel danneggiati rappresentano un problema poiché non possono essere aperti. Puoi provare l'app Aspose.Cells Cloud Excel Repair per recuperare i dati da tali file.

## API REST

L'endpoint **Riparazione di file Excel** ripara file di fogli di calcolo danneggiati e restituisce il contenuto riparato.


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione                     | Descrizione |
|----------------|--------|------------------------------|-------------|
| file           | file   | formData (multipart)         | File da caricare |
| format         | string | query                        | Formato di output desiderato. Se omesso (null), il formato di output corrisponde a quello del file di input. |

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nome file unito]",
    "Filesize" : [dimensione file],
    "FileContent" : "[Base64String]"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto sul server. |
## Come utilizzare l'API PostRepair con gli SDK

### Specifica dell'API PostRepair

La [Specifica OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

In caso di successo, il servizio restituisce HTTP 200 con un payload JSON contenente un array `Files`. In caso di errore, l'API utilizza i codici di stato HTTP standard:

- **400 Bad Request** – Parametri non validi o file non riparabile.  
- **401 Unauthorized** – Token JWT mancante o non valido.  
- **413 Payload Too Large** – Il file caricato supera la dimensione consentita.  
- **500 Internal Server Error** – Errore imprevisto lato server.

## Famiglia di SDK Cloud

Utilizzare un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}