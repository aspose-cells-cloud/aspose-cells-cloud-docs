---
title: "Aggiorna le proprietà del foglio di lavoro – Riferimento API Cloud di Aspose.Cells (v3.0)"
second_title: "Documento"
linktitle: "Aggiorna"
type: docs
url: /it/worksheets/update-properties/
aliases: [  /it/update-excel-worksheet-properties/ ]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "foglio di lavoro",
    "aggiorna proprietà",
    "API REST",
    "cloud",
    "v3.0",
  ]
description: "Scopri come aggiornare le proprietà di base (ad esempio, visualizzazione degli zeri, visibilità del righello) di un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud v3.0. Include richieste cURL, esempi SDK, parametri e gestione degli errori."
ArticleTitle: "Aggiorna le proprietà del foglio di lavoro – Riferimento API Cloud di Aspose.Cells (v3.0)"
---

Questa API REST aggiorna le proprietà di base del foglio di lavoro.

## API REST

**Prerequisiti:** È necessario disporre di un account Aspose Cloud valido, ottenere un token di accesso JWT e assicurarsi che il foglio di calcolo di destinazione sia archiviato in una posizione di archiviazione supportata. Tutte le richieste devono essere effettuate tramite **HTTPS**.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                      |
| -------------- | ------ | -------------------------------- | ------------------------------------------------------------------------------------------------ |
| name           | string | percorso                         | Nome del file del foglio di calcolo (inclusa l'estensione).                                     |
| sheetName      | string | percorso                         | Nome del foglio di lavoro da aggiornare.                                                        |
| sheet          | object | corpo                            | Oggetto JSON contenente le coppie chiave/valore delle proprietà del foglio di lavoro (es. `DisplayZeros`, `IsRulerVisible`). |
| folder         | string | query                            | Percorso della cartella nella quale si trova il foglio di calcolo.                             |
| storageName    | string | query                            | Nome dell'archiviazione da utilizzare.                                                          |

L'oggetto **sheet** viene inviato nel corpo della richiesta come JSON. Le proprietà modificabili includono `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible` e altre definite nella specifica dell'API.

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
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

Codici di risposta tipici:

- **200** – Esito positivo. Le proprietà del foglio di lavoro sono state aggiornate.
- **400** – Richiesta non valida (ad esempio, JSON non corretto o parametro obbligatorio mancante).
- **401** – Non autorizzato – token JWT mancante o non valido.
- **404** – Foglio di calcolo o foglio di lavoro non trovato.
- **500** – Errore interno del server.

| Codice | Significato |
|--------|-------------|
| 200 | Esito positivo – le proprietà del foglio di lavoro sono state aggiornate. |
| 400 | Richiesta non valida – JSON non corretto o parametro obbligatorio mancante. |
| 401 | Non autorizzato – token JWT mancante o non valido. |
| 404 | Non trovato – il foglio di calcolo o il foglio di lavoro non esiste. |
| 500 | Errore interno del server. |

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}