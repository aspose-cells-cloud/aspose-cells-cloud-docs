---
title: "Eliminare più righe da un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Righe"
type: docs
url: /rows/delete/rows/
keywords: "Aspose.Cells Cloud, eliminare righe, eliminare più righe, foglio di lavoro Excel, API REST, SDK"
description: "Scopri come eliminare una o più righe da un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include dettagli sull'endpoint, parametri, un esempio cURL e campioni di codice SDK per vari linguaggi."
weight: 80
ArticleTitle: "Eliminare più righe da un foglio di lavoro Excel con l'API Aspose.Cells Cloud"
---

Questa API REST elimina più righe **da** un foglio di lavoro Excel.

**Prerequisiti:** Per chiamare questo endpoint, è necessario disporre di un token di accesso JWT valido ottenuto tramite l'autenticazione di Aspose Cloud e di autorizzazioni appropriate per lo storage del file di lavoro.

## API DeleteWorksheetRows

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Percorso / Stringa di query / Corpo HTTP | Descrizione                                                            |
| --------------- | ------- | ---------------------------------------- | ---------------------------------------------------------------------- |
| name            | string  | percorso                                 | Nome del file di lavoro.                                               |
| sheetName       | string  | percorso                                 | Nome del foglio di lavoro.                                             |
| startrow        | integer | query                                    | Indice in base zero della prima riga da eliminare (es. `0` = prima riga). |
| totalRows       | integer | query                                    | Numero di righe da eliminare.                                          |
| updateReference | boolean | query                                    | Indica se aggiornare i riferimenti dopo l'eliminazione (`true`/`false`). |
| folder          | string  | query                                    | Cartella del documento.                                                |
| storageName     | string  | query                                    | Nome dello storage.                                                    |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL. **Tutti gli endpoint richiedono HTTPS; HTTP è deprecato.**

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
-X DELETE \
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

**Codici di risposta possibili**

| Stato HTTP | Descrizione |
|------------|-------------|
| 200 | Righe eliminate con successo. |
| 400 | Richiesta non valida – parametri non validi. |
| 401 | Non autorizzato – token JWT mancante o non valido. |
| 404 | Non trovato – il file di lavoro o il foglio di lavoro non esiste. |
| 500 | Errore interno del server – condizione imprevista. |

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}