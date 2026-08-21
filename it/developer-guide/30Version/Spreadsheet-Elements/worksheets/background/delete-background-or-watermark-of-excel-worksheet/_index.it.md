---
title: "Elimina lo sfondo di un foglio di calcolo Excel"
second_title: "Document"
linktype: "Elimina"
type: docs
url: /it/worksheets/background/delete/
aliases: [/it/delete-background-or-watermark-of-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Elimina sfondo del foglio di calcolo, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Utilizza l'API REST di Aspose.Cells Cloud per eliminare l'immagine di sfondo di un foglio di calcolo Excel. Gli SDK sono disponibili per C#, Java, PHP, Ruby, Node.js, Python, Perl e Go."
weight: 210
ArticleTitle: "Elimina lo sfondo di un foglio di calcolo Excel utilizzando l'API Aspose.Cells Cloud"
---

Questo REST API elimina l'immagine di sfondo di un foglio di calcolo.

**Prerequisiti:** Devi aver memorizzato il workbook nello storage di Aspose Cloud e possedere un token di accesso JWT valido per l'autenticazione.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Parametri della richiesta**

| Nome del parametro | Tipo   | Posizione | Descrizione                                               |
| ------------------ | ------ | --------- | --------------------------------------------------------- |
| name               | string | path      | Il nome del file Excel.                                   |
| sheetName          | string | path      | Il nome del foglio di calcolo da cui rimuovere lo sfondo. |
| folder             | string | query     | La cartella nello storage dove il file è posizionato.     |
| storageName        | string | query     | Il nome dello storage (se diverso da quello predefinito). |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) definiscono un'interfaccia di programmazione accessibile pubblicamente e ti consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. Tutte le richieste richiedono un token JWT valido. Ottieni il token tramite l'endpoint del token OAuth2 come descritto nella guida all'autenticazione.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
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

**Codici di stato HTTP**

| Codice | Significato              | Descrizione                                                    |
|--------|--------------------------|----------------------------------------------------------------|
| 200    | OK                       | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida     | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato          | Token JWT non valido o mancante. |
| 413    | Payload troppo grande    | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server | Errore imprevisto sul server. |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}