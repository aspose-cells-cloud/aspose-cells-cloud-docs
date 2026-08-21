---
title: "Aspose.Cells Cloud API – Ottieni l'uso del disco – Metriche di archiviazione in tempo reale"
second_title: "Documento"
ArticleTitle: "Soluzione di gestione dei file Excel basata sul cloud – Interfaccia per recuperare rapidamente l'uso del disco nel cloud."
linktype: "Ottieni l'uso del disco"
type: docs
url: /it/get-disk-usage/
keywords: "Aspose Cells, API cloud, uso del disco, metriche di archiviazione, Excel, REST"
description: "Recupera l’uso del disco in tempo reale per Aspose.Cells Cloud. Scopri l’endpoint GET /v4.0/cells/storage/disk, l’autenticazione richiesta e una risposta di esempio."
weight: 100
---

L'operazione **Ottieni l'uso del disco** restituisce metriche di archiviazione in tempo reale per il tuo account Aspose.Cells Cloud. Utilizza questo endpoint per monitorare lo spazio disco consumato e quello totale disponibile.

- Recupera l’uso corrente del disco per l’API Excel nell’ambiente Aspose Cloud.
- Consente agli sviluppatori di monitorare quanto spazio di archiviazione hanno consumato le proprie applicazioni.
- Consente una gestione proattiva dei limiti di archiviazione e un controllo dei costi.

## API Excel: GetDiskUsage

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                                           | Obbligatorio |
| -------------- | ------ | --------- | ----------------------------------------------------- | ------------ |
| storageName    | String | Query     | Il nome dell’archiviazione per la quale recuperare l’uso. | Opzionale    |

### **Risposta**

```json
{
  "Name": "DiskUsage",
  "Description": ["Classe per le informazioni sullo spazio su disco."],
  "Type": "Classe",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["Quantità di spazio su disco utilizzata dall'applicazione."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["Spazio su disco totale disponibile."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                        |
| ------ | ----------------------- | ------------------------------------------------------------------ |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                   |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer TU_TOKEN_ACCESS"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK rappresenta il modo più rapido per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}