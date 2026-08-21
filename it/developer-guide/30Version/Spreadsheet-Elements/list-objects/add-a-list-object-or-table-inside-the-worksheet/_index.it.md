---
title: "Aggiungi un oggetto elenco (tabella) a un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Aggiungi"
type: docs
url: /it/list-objects/add/
aliases: [  /it/add-a-list-object-or-table-inside-the-worksheet/ , /it/tables/add/ ]
keywords: "Aspose.Cells Cloud, Excel API, oggetto elenco, tabella, REST API, foglio di lavoro"
description: "Scopri come aggiungere un oggetto elenco (tabella Excel) a un foglio di lavoro utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri, passaggi di autenticazione, esempio cURL e codice di esempio per SDK."
weight: 10
ArticleTitle: "Aggiungi un oggetto elenco (tabella) a un foglio di lavoro Excel – Documentazione di Aspose.Cells Cloud"
---

Questa REST API aggiunge un **oggetto elenco (tabella)** a un foglio di lavoro Excel.

Prima di utilizzare questo endpoint, assicurati di disporre di un token JWT valido, che il workbook sia memorizzato in un archivio cloud supportato e che il foglio di lavoro esista.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### Parametri della richiesta

| Nome parametro  | Tipo    | Posizione | Descrizione                                                                  |
| --------------- | ------- | --------- | ---------------------------------------------------------------------------- |
| **name**        | string  | path      | Nome del file del workbook.                                                  |
| **sheetName**   | string  | path      | Nome del foglio di lavoro.                                                   |
| **startRow**    | integer | query     | Indice in base zero della prima riga dell'intervallo della tabella.         |
| **startColumn** | integer | query     | Indice in base zero della prima colonna dell'intervallo della tabella.      |
| **endRow**      | integer | query     | Indice in base zero dell'ultima riga dell'intervallo della tabella.         |
| **endColumn**   | integer | query     | Indice in base zero dell'ultima colonna dell'intervallo della tabella.      |
| **hasHeaders**  | boolean | query     | `true` se la prima riga contiene intestazioni di colonna; altrimenti `false`. |
| **listObject**  | object  | body      | Definizione dell'oggetto elenco (vedere **Schema del corpo della richiesta**).|
| **folder**      | string  | query     | Cartella contenente il workbook.                                             |
| **storageName** | string  | query     | Nome dell'archivio.                                                          |

### Schema del corpo della richiesta

L'oggetto **listObject** descrive la tabella che verrà creata. Vengono mostrate solo le proprietà più comuni; per l'elenco completo consultare la specifica OpenAPI.

```json
{
  "displayName": "MiaTabella",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MiaTabella",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### Risposta di esempio

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Codici di errore

| Stato HTTP | Motivo             | Descrizione                                           |
| ---------- | ------------------ | ----------------------------------------------------- |
| **400**    | Richiesta non valida | Parametri di intervallo non validi o corpo JSON malformato. |
| **401**    | Non autorizzato    | Token JWT mancante o scaduto.                         |
| **404**    | Non trovato        | Il workbook o il foglio di lavoro specificato non esiste. |
| **500**    | Errore interno del server |Errore imprevisto lato server.                      |

**Esempio di risposta 400**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Parametri di intervallo non validi."
}
```

**Esempio di risposta 401**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Il token di autenticazione è mancante o scaduto."
}
```

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) forniscono il contratto completo per questa operazione.

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sui compiti del proprio progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}