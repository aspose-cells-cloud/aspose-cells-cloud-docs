---
title: "Rivela righe in un foglio di lavoro Excel"
second_title: "Documento"
linktype: "Rivela"
type: docs
url: /it/rows/unhide/
aliases: [  /it/unhide-rows-in-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, rivela righe, REST API, foglio di calcolo, .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl, Swift, Aspose.Cells Cloud REST API"
description: "Utilizza l'API REST di Aspose.Cells Cloud per rivelare le righe in un foglio di lavoro Excel. L'API è disponibile tramite diversi SDK, tra cui .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl e Swift."
weight: 50
ArticleTitle: "Rivela righe in un foglio di lavoro Excel utilizzando l'API Aspose.Cells Cloud"
---

Questa REST API rivela le righe in un foglio di lavoro Excel.

**Prerequisiti:** Ottenere un token di accesso JWT valido dal servizio di autenticazione di Aspose Cloud e assicurarsi che il workbook di destinazione sia caricato su uno storage supportato prima di richiamare questo endpoint.

## API PostUnhideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/unhide
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                           |
| -------------- | ------- | --------- | ----------------------------------------------------- |
| name           | string  | path      | Nome del workbook.                                    |
| sheetName      | string  | path      | Nome del foglio di lavoro.                            |
| startrow       | integer | query     | Indice in base zero della prima riga da rivelare.     |
| totalRows      | integer | query     | Numero di righe da rivelare.                          |
| height         | number  | query     | Altezza della riga (valore predefinito: 15,0).        |
| folder         | string  | query     | Cartella del documento.                               |
| storageName    | string  | query     | Nome dello storage.                                   |

La <a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetRows" rel="noopener noreferrer">specifiche OpenAPI</a> definiscono un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

**Autenticazione**  
Tutte le richieste devono essere autenticate utilizzando un token di accesso JWT ottenuto dal servizio di autenticazione di Aspose Cloud. Includere il token nell'intestazione `Authorization: Bearer <jwt token>`.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/unhide?startrow=1&totalRows=1&height=15" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
# Nota: il corpo della richiesta POST è vuoto per questo endpoint
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

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                             |
|--------|-----------------------------|---------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                        |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.       |
| 500    | Errore interno del server   | Errore imprevisto sul server.                           |

Per la risoluzione dettagliata dei problemi, consulta la [guida alla gestione degli errori](/it/error-handling/).

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---