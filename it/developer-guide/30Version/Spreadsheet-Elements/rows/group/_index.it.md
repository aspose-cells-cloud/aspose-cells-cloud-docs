---
title: "Raggruppa righe in un foglio di lavoro Excel"
second_title: "Document"
linktype: "Raggruppa"
type: docs
url: /rows/group/
aliases: [/group-rows-in-excel-worksheet/]
keywords: "raggruppa righe, Excel, Aspose.Cells Cloud, REST API, SDK, foglio di lavoro, Excel API"
description: "Raggruppa righe in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Supporta diversi SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) per un'integrazione semplice."
weight: 60
ArticleTitle: "Raggruppa righe in un foglio di lavoro Excel con l'API Aspose.Cells Cloud"
---

Questa API REST consente di raggruppare righe in un foglio di lavoro Excel.

**Prerequisiti:**  
- È necessario fornire un token di accesso OAuth 2.0 valido (Bearer JWT) nell'intestazione `Authorization`.  
- Il workbook deve già esistere nella cartella specificata `folder` dello `storageName` scelto (o nello storage predefinito) prima di effettuare la richiesta.

## API PostGroupWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome Parametro | Tipo    | Posizione | Descrizione                                                              |
| -------------- | ------- | -------- | ------------------------------------------------------------------------ |
| name           | string  | path     | Nome del file del workbook.                                              |
| sheetName      | string  | path     | Nome del foglio di lavoro.                                               |
| firstIndex     | integer | query    | Indice in base zero della prima riga da raggruppare.                    |
| lastIndex      | integer | query    | Indice in base zero dell'ultima riga da raggruppare.                    |
| hide           | boolean | query    | Indica se le righe raggruppate debbano essere nascoste (`true` o `false`). |
| folder         | string  | query    | Percorso della cartella contenente il workbook.                          |
| storageName    | string  | query    | Nome dello storage in cui si trova il workbook.                          |

Lo [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
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

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto sul server. |

Risposte di errore tipiche:

- **400 Richiesta non valida** – verificare che `firstIndex` e `lastIndex` siano interi validi e che `firstIndex` ≤ `lastIndex`.  
- **401 Non autorizzato** – verificare che l'intestazione `Authorization` contenga un token JWT valido e non scaduto.  
- **404 Non trovato** – assicurarsi che il workbook (`name`) e il foglio di lavoro (`sheetName`) esistano nella cartella (`folder`) e nello storage (`storageName`) specificati.

{{< /tab >}}

{{< /tabs >}}

**Vedi anche:** [Annulla il raggruppamento delle righe in un foglio di lavoro Excel](../rows/ungroup/ "Annulla il raggruppamento delle righe in un foglio di lavoro Excel"), [Nascondi righe in un foglio di lavoro Excel](../rows/hide/ "Nascondi righe in un foglio di lavoro Excel"), [Mostra righe in un foglio di lavoro Excel](../rows/unhide/ "Mostra righe in un foglio di lavoro Excel").

## Famiglia di SDK Cloud

Utilizzare un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells mediante vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}