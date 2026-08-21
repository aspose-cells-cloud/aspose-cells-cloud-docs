---
title: "Come unire le celle in un foglio di lavoro Excel – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /it/merge-cells-in-excel-worksheet/
weight: 110
keywords: "unire celle, Aspose.Cells, API cloud, Excel"
description: "Guida all’unione delle celle in un foglio di lavoro Excel utilizzando l’API REST di Aspose.Cells Cloud con esempi in cURL e SDK."
ArticleTitle: "Come unire le celle in un foglio di lavoro Excel – Aspose.Cells Cloud API (v3.0)"
---

L'API REST di Aspose.Cells Cloud consente di unire un blocco rettangolare di celle in un’unica cella che si estende sulle righe e sulle colonne specificate.

**Prerequisiti**  
- Un token JWT valido per l’autenticazione.  
- Il workbook deve già esistere nella cartella di archiviazione specificata.  
- La configurazione dell’archiviazione (nome cartella e nome archivio) deve essere impostata nel tuo account Aspose.Cloud.

## API PostWorksheetMerge

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome             | Tipo    | Posizione | Descrizione                                             |
|------------------|---------|-----------|---------------------------------------------------------|
| name             | string  | path      | Nome del workbook.                                      |
| sheetName        | string  | path      | Nome del foglio di lavoro.                              |
| startRow         | integer | query     | Indice in base zero della prima riga (0 = prima riga).  |
| startColumn      | integer | query     | Indice in base zero della prima colonna (0 = prima colonna). |
| totalRows        | integer | query     | Numero di righe da unire.                               |
| totalColumns     | integer | query     | Numero di colonne da unire.                             |
| folder           | string  | query     | Cartella contenente il workbook.                        |
| storageName      | string  | query     | Nome dell’archivio.                                     |

*Per questa operazione non è richiesto alcun corpo della richiesta.*

## **Risposta**

Restituisce un oggetto CellsCloudResponse.

```json
{
  "Status": "OK",
  "Code": 200
}
```

**Codici di stato HTTP**

| Codice | Significato                  | Descrizione                                                |
|--------|------------------------------|------------------------------------------------------------|
| 200    | OK                           | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida         | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato              | Token JWT non valido o mancante.                           |
| 413    | Payload troppo grande        | Il file caricato supera il limite di dimensione.         |
| 500    | Errore interno del server    | Errore imprevisto nel server.                              |

## Come utilizzare l’API PostWorksheetMerge con gli SDK

### Specifica dell’API PostWorksheetMerge

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) definiscono un’interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK rappresenta il modo più efficiente per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}