---
title: "Verifica se uno Storage Esiste – Aspose.Cells Cloud API (v4.0)"
second_title: "Documento"
ArticleTitle: "Gestione di File Excel Basata su Cloud – Verifica l’Esistenza di uno Storage"
linktitle: "Storage Esiste"
type: docs
url: /storage-exists/
keywords: "Aspose.Cells, storage esiste, API per storage cloud, REST, Excel"
description: "Verifica l'esistenza di un contenitore di storage in Aspose.Cells Cloud. Scopri l'endpoint GET /v4.0/cells/storage/{storageName}/exist, i parametri richiesti, il formato della risposta e consulta esempi di SDK in C#, Java, Python e altri linguaggi."
weight: 100
---

L'API `storageExists` verifica se uno storage specificato esiste nel servizio cloud di Aspose.Cells. Questa funzionalità è fondamentale per garantire che tutte le operazioni che dipendono dallo storage possano procedere senza errori.
**Sintesi** – L'endpoint `storageExists` consente di confermare se un contenitore di storage specifico è disponibile in Aspose.Cells Cloud. Utilizzatelo prima di eseguire operazioni relative ai file per evitare errori in fase di esecuzione.

## Verifica dell’Esistenza di uno Storage (storageExists)

### API Web

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro | Tipo   | Posizione | Descrizione                                           |
| -------------- | ------ | --------- | ----------------------------------------------------- |
| storageName    | String | Path      | Il nome dello storage di cui verificare l'esistenza. |

### **Risposta**

```json
{
  "Name": "StorageExist",
  "Description": ["Indica se lo storage specificato esiste."],
  "Type": "Classe",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indica se lo storage esiste.",
        "Questa proprietà restituisce true se lo storage è presente; in caso contrario, restituisce false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**Codici di Stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta Non Validata | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non Autorizzato       | Token JWT non valido o mancante.                                  |
| 413    | Payload Troppo Grande | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore Interno del Server | Errore imprevisto sul server.                                   |

## Come Usare l’API per Verificare l’Esistenza di uno Storage con gli SDK?

### Specifica OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione accessibile pubblicamente, consentendo agli sviluppatori di interagire direttamente con l'API REST da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta l’approccio più efficiente per accelerare lo sviluppo. Un SDK astrae i dettagli di implementazione di basso livello, consentendo agli sviluppatori di concentrarsi sulle attività del proprio progetto. Per un elenco completo degli SDK disponibili di Aspose.Cells Cloud, visitare il <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">repository GitHub</a>.

I seguenti esempi di codice mostrano come effettuare chiamate API ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}