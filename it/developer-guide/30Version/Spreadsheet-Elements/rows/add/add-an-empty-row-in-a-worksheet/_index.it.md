---
title: "Aggiungi una riga vuota in un foglio di lavoro Excel"
ArticleTitle: "Aggiungi una riga vuota a un foglio di lavoro Excel utilizzando l'API Aspose.Cells Cloud"
second_title: "Documenti"
linktitle: "Riga"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, aggiungi riga vuota, foglio di lavoro, REST API, inserisci riga, foglio di calcolo cloud"
description: "Utilizza l'API REST Aspose.Cells Cloud per inserire una riga vuota in un foglio di lavoro Excel. Supporta numerosi SDK (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) per uno sviluppo rapido."
weight: 20
---

Questa API REST consente di aggiungere una nuova riga a un foglio di lavoro Excel. Essa inserisce una riga vuota all'indice zero-based specificato.

**Prerequisiti:**  
- È necessario includere un token di accesso Aspose Cloud valido (Bearer JWT) nell'header `Authorization`.  
- Il libro di lavoro target deve essere caricato nello storage Aspose Cloud, e i parametri `folder` e `storageName` devono puntare alla sua posizione.

**Note:**  
- L'indice `rowIndex` è zero-based; inserire alla posizione 0 aggiunge una riga all'inizio del foglio di lavoro.  
- I fogli di lavoro Excel hanno un massimo di 1.048.576 righe; tentare di inserire oltre questo limite comporterà un errore.

## API PutInsertWorksheetRow

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione tramite token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                                |
|----------------|---------|-----------|------------------------------------------------------------|
| name           | string  | path      | Nome del file del libro di lavoro.                         |
| sheetName      | string  | path      | Nome del foglio di lavoro.                                 |
| rowIndex       | integer | path      | Indice zero-based in cui verrà inserita la nuova riga.     |
| folder         | string  | query     | Percorso della cartella nello storage contenente il libro. |
| storageName    | string  | query     | Nome dello storage Aspose Cloud da utilizzare.             |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Nota:** Tutti gli endpoint Aspose.Cells Cloud richiedono HTTPS. Utilizzare lo schema sicuro `https://` per le chiamate in produzione.

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

**Codici di stato HTTP**

| Codice | Significato              | Descrizione                                               |
|--------|--------------------------|-----------------------------------------------------------|
| 200    | OK                       | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida     | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato          | Token JWT non valido o mancante.                          |
| 413    | Payload troppo grande    | File caricato supera il limite di dimensione.             |
| 500    | Errore interno del server | Errore imprevisto nel server.                            |

*Esempio di risposta di errore (es. quando l'indice della riga supera il limite del foglio di lavoro):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Indice riga fuori intervallo. Il numero massimo di righe consentito è 1048576."
}
```

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}