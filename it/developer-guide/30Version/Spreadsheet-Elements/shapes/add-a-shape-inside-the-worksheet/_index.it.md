---
title: "Aggiungi una forma a un foglio di calcolo Excel"
second_title: "Document"
linktype: "Add"
type: docs
url: /it/shapes/add/
aliases: [  /it/add-a-shape-inside-the-worksheet/ ]
keywords: "Aspose.Cells, aggiungi forma, Excel, REST API, cloud SDK, shapeDTO, tipo di disegno"
description: "Scopri come aggiungere forme (arco, linea, rettangolo, ecc.) a un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud v3.0. Include la sintassi della richiesta, i parametri obbligatori, i passaggi di autenticazione e il codice di esempio per l'SDK."
weight: 30
ArticleTitle: "Aggiungi una forma a un foglio di calcolo Excel utilizzando l'API Aspose.Cells Cloud"
---

Questa REST API aggiunge una forma a un foglio di calcolo Excel.  
L'endpoint appartiene alla **versione API v3.0**; assicurati di utilizzare un token di accesso JWT ottenuto tramite il flusso OAuth2 di Aspose Cloud (client‑id/client‑secret) e di includerlo nell'intestazione `Authorization: Bearer <token>`.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

## API PutWorksheetShape

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                                                                           |
| --------------- | ------- | -------- | ----------------------------------------------------------------------------------------------------- |
| name            | string  | path     | Nome del documento.                                                                                  |
| sheetName       | string  | path     | Nome del foglio di calcolo.                                                                          |
| shapeDTO        | object  | body     | Oggetto JSON che descrive la forma da aggiungere (vedere la specifica OpenAPI per lo schema completo). |
| drawingType     | string  | query    | Tipo di oggetto forma (ad esempio, `arc`, `line`, `rectangle`).                                      |
| upperLeftRow    | integer | query    | Indice della riga in alto a sinistra della forma.                                                     |
| upperLeftColumn | integer | query    | Indice della colonna in alto a sinistra della forma.                                                  |
| top             | integer | query    | Offset verticale della forma dal suo bordo superiore, in pixel.                                       |
| left            | integer | query    | Offset orizzontale della forma dal suo bordo sinistro, in pixel.                                      |
| width           | integer | query    | Larghezza della forma, in pixel.                                                                      |
| height          | integer | query    | Altezza della forma, in pixel.                                                                        |
| folder          | string  | query    | Cartella che contiene il documento.                                                                   |
| storageName     | string  | query    | Nome dello storage.                                                                                   |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ShapeId": 5
}
```

_La risposta in caso di esito positivo restituisce il codice di stato HTTP, una descrizione testuale e l'identificatore della nuova forma creata (`ShapeId`)._

{{< /tab >}}

{{< /tabs >}}

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

Le risposte di errore tipiche includono:

- **400 Richiesta non valida** – parametri mancanti o non validi.  
- **401 Non autorizzato** – token JWT non valido o mancante.  
- **404 Non trovato** – il foglio di calcolo o il documento specificato non esiste.

Ogni errore viene restituito come oggetto JSON contenente i campi `Code` e `Message`.

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}