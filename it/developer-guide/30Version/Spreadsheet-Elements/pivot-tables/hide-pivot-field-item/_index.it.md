---
title: "Nascondi un elemento del campo pivot in una tabella pivot"
second_title: "Document"
linktitle: Nascondi
type: docs
url: /it/pivot-tables/hide-pivot-field-item/
aliases: [/it/hide-pivot-field-item/]
keywords: "Aspose.Cells, nascondi elemento del campo pivot, API PivotTable, API REST, SDK cloud"
description: "Scopri come nascondere un elemento del campo pivot in una tabella pivot utilizzando l'API REST di Aspose.Cells Cloud. Include i dettagli della richiesta, un esempio cURL e frammenti di codice SDK per diversi linguaggi."
weight: 110
ArticleTitle: "Nascondi elemento del campo pivot in una tabella pivot – Guida all'API di Aspose.Cells Cloud"
---

Prima di chiamare l'API, assicurati di avere:

* Un **token di accesso JWT** valido (ottenibile tramite il flusso di autenticazione di Aspose Cloud).  
* Il foglio di calcolo di destinazione caricato nel tuo archivio Aspose Cloud.  
* Il foglio di lavoro e la tabella pivot già creati.

Questi prerequisiti prevengono errori di autenticazione e risposte “risorsa non trovata”. I passaggi seguenti descrivono la configurazione necessaria prima di invocare l'API.

Questa API REST nasconde un elemento del campo pivot in una tabella pivot.

## API PostPivotTableFieldHideItem

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                                                                      |
| --------------- | ------- | --------- | ------------------------------------------------------------------------------------------------ |
| name            | string  | path      | Nome del file Excel.                                                                             |
| sheetName       | string  | path      | Foglio di lavoro contenente la tabella pivot.                                                    |
| pivotTableIndex | integer | path      | Indice della tabella pivot all'interno del foglio di lavoro.                                     |
| pivotFieldType  | string  | query     | Tipo del campo pivot (Row, Column, Page, Data, ecc.).                                           |
| fieldIndex      | integer | query     | Indice in base zero del campo pivot da modificare.                                              |
| itemIndex       | integer | query     | Indice dell'elemento specifico all'interno del campo da nascondere.                             |
| isHide          | boolean | query     | Impostare su **true** per nascondere l'elemento; **false** per mostrarlo.                       |
| needReCalculate | boolean | query     | Indica se la tabella pivot debba essere ricalcolata dopo la modifica. Il valore predefinito è **false**. |
| folder          | string  | query     | Percorso della cartella in cui è archiviato il foglio di calcolo.                               |
| storageName     | string  | query     | Nome del servizio di archiviazione.                                                              |

**Riferimento rapido ai parametri di query obbligatori**

- **pivotFieldType** – tipo del campo (es. `Row`).  
- **fieldIndex** – indice in base zero del campo da modificare.  
- **itemIndex** – indice in base zero dell'elemento da nascondere/mostrare.  
- **isHide** – `true` per nascondere, `false` per mostrare.  
- **needReCalculate** – opzionale, valore predefinito `false`.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
  -X POST \
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

**Dettagli della risposta**

| Codice di stato | Descrizione                                                          |
| --------------- | -------------------------------------------------------------------- |
| 200             | L'elemento è stato nascosto correttamente.                          |
| 400             | Richiesta non valida – parametri mancanti o non validi.             |
| 401             | Non autorizzato – token JWT non valido o mancante.                  |
| 500             | Errore del server – l'operazione non può essere completata.         |

**Nota:** Se `fieldIndex` o `itemIndex` forniti è fuori intervallo, l'API restituisce una risposta **400 Bad Request**.

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare contro l'API. Gli SDK gestiscono i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come nascondere un elemento del campo pivot utilizzando diversi SDK.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // Prepara il foglio di calcolo e il foglio di lavoro
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Carica il foglio di calcolo
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Crea il foglio di lavoro che conterrà la tabella pivot
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Crea un secondo foglio di lavoro con dati di esempio
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Importa dati di esempio in Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // Troncato per brevità
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Aggiungi una tabella pivot a PivotSheet
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Nascondi un elemento specifico del campo riga
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**Nota:** Gli esempi di SDK presuppongono che tu abbia già configurato l'autenticazione (token JWT) e che il foglio di calcolo si trovi nella cartella specificata dell'archivio. Regola i parametri `folder` e `storageName` in base al tuo ambiente.