---
title: "Adattamento automatico delle colonne in un file Excel"
second_title: "Documento"
linktitle: "Colonne"
type: docs
url: /it/autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "Adattamento automatico colonne, Excel, Aspose.Cells Cloud, REST API, SDK, cURL, API"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per adattare automaticamente le colonne in un file Excel. Include i dettagli della richiesta, un esempio cURL e campioni di codice SDK per diversi linguaggi."
weight: 90
---

Questa REST API supporta l'adattamento automatico delle colonne in un file Excel.

## API PostAutofitWorkbookColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

I parametri della richiesta sono:

| Nome Parametro        | Tipo    | Posizione | Descrizione                                          |
| --------------------- | ------- | --------- | ---------------------------------------------------- |
| **name**              | string  | path      | Nome del file del workbook.                          |
| **autoFitterOptions** | object  | body      | Opzioni che controllano il comportamento di adattamento automatico. |
| **startColumn**       | integer | query     | Indice in base zero della prima colonna da adattare. |
| **endColumn**         | integer | query     | Indice in base zero dell'ultima colonna da adattare. |
| **folder**            | string  | query     | Cartella contenente il workbook.                     |
| **storageName**       | string  | query     | Nome del servizio di archiviazione.                  |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **Nota:** Utilizza sempre l'endpoint HTTPS in produzione e mantieni il token JWT riservato.

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

### Prerequisiti
Prima di chiamare questa operazione, assicurati di disporre di una chiave API valida di Aspose Cloud, di un token JWT generato e che il workbook di destinazione esista già nella posizione di archiviazione specificata.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                  |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                             |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.            |
| 500    | Errore interno del server   | Errore imprevisto nel server.                                |

L'API può restituire i seguenti codici di stato HTTP:

| Codice | Descrizione                                      |
|--------|--------------------------------------------------|
| 200    | Successo – colonne adattate automaticamente      |
| 400    | Richiesta non valida – parametri mancanti o non validi |
| 401    | Non autorizzato – JWT non valido o scaduto       |
| 500    | Errore server – errore durante l'elaborazione interna |

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il metodo più efficiente per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulla logica del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}