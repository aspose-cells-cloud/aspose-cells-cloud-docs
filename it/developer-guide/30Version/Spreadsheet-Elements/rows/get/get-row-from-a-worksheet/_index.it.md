---
title: "Ottenere la descrizione di una riga da un foglio di calcolo Excel"
second_title: "Document"
linktype: "Row"
type: docs
url: /it/rows/get/row/
aliases: [  /it/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, API riga Excel, Ottieni riga foglio di calcolo, REST API, .NET SDK, Java SDK, Python SDK"
description: "Recupera informazioni dettagliate (altezza, stile, stato di visibilità, ecc.) per una specifica riga in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempio cURL, frammenti SDK e gestione degli errori."
weight: 10
ArticleTitle: "Ottenere la descrizione di una riga da un foglio di calcolo Excel – API Aspose.Cells Cloud"
---

**Prerequisiti:**
- Ottieni un token di accesso JWT valido e includilo nell'intestazione `Authorization: Bearer <jwt token>`.
- Assicurati che il file di lavoro sia memorizzato nello storage di Aspose Cloud o specifica il percorso della cartella in cui si trova.
- Usa la versione dell'API **v3.0** come mostrato nell'URL dell'endpoint.

Questa API REST recupera i dati di una riga in base all'indice all'interno di un foglio di calcolo Excel.

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                         |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name           | string  | path     | Nome del file di lavoro.                            |
| sheetName      | string  | path     | Nome del foglio di calcolo all'interno del file di lavoro. |
| rowIndex       | integer | path     | Indice in base zero della riga da recuperare.       |
| folder         | string  | query    | Cartella contenente il file di lavoro.              |
| storageName    | string  | query    | Nome dello storage in cui risiede il file di lavoro. |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL. Includi l'intestazione `Authorization: Bearer <jwt token>` per autenticare la richiesta.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Schema della risposta**

| Proprietà         | Tipo    | Descrizione                                                          |
|-------------------|---------|----------------------------------------------------------------------|
| `GroupLevel`      | integer | Livello di raggruppamento della riga (usato per l'aggregazione).    |
| `Height`          | number  | Altezza della riga in punti.                                         |
| `Index`           | integer | Indice in base zero della riga restituita.                           |
| `IsBlank`         | boolean | Indica se la riga contiene dati.                                     |
| `IsHeightMatched`| boolean | `true` se l'altezza della riga corrisponde all'altezza predefinita.  |
| `IsHidden`        | boolean | `true` se la riga è nascosta.                                        |
| `Style`           | object  | Oggetto contenente le informazioni di stile della riga.             |
| `link`            | object  | Riferimento ipertestuale alla risorsa riga.                          |
| `Code`            | integer | Codice di stato HTTP della risposta.                                 |
| `Status`          | string  | Descrizione testuale dello stato (ad esempio, “OK”).                |

{{< /tab >}}

{{< /tabs >}}

**Note / Gestione errori:** L'API può restituire i seguenti codici di stato HTTP:

- **200** – Successo; i dati della riga vengono restituiti.
- **401** – Non autorizzato; il token JWT è mancante o non valido.
- **404** – Non trovato; il file di lavoro, il foglio di calcolo o la riga specificati non esistono.
- **500** – Errore interno del server; si è verificata una condizione imprevista.

| Codice | Descrizione                                   | Soluzione                                |
|--------|-----------------------------------------------|------------------------------------------|
| 200    | Successo – dati della riga restituiti.        | –                                        |
| 401    | Non autorizzato – token JWT mancante o non valido. | Fornire un token JWT valido.           |
| 404    | Non trovato – file di lavoro, foglio di calcolo o riga mancante. | Verificare i nomi e l'indice della riga. |
| 500    | Errore interno del server – condizione imprevista. | Contattare il supporto Aspose.          |

Per un elenco completo dei codici di errore, consulta la [documentazione sui codici di errore](https://docs.aspose.cloud/cells/) di Aspose.Cells Cloud.

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il metodo più rapido per lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}