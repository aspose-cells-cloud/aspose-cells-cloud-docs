---
title: "Ottenere una forma per indice in un foglio di lavoro Excel"
second_title: "Document"
linktype: "Get"
type: docs
url: /it/shapes/get/
aliases: [/it/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, API per le forme Excel, ottenere una forma per indice, forma nel foglio di lavoro, API REST, recupero della forma, Aspose.Cells SDK"
description: "Recuperare una forma per indice da un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta, i parametri, i dettagli della risposta e gli esempi di SDK."
weight: 20
ArticleTitle: "Ottenere una forma per indice in un foglio di lavoro Excel – Documentazione di Aspose.Cells Cloud"
---

Questa API REST recupera una forma (inclusi i dati dell'immagine o i metadati) da un foglio di lavoro Excel.

## API GetWorksheetShape

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**Prerequisiti**  
- Un token di accesso valido per Aspose Cloud (Bearer JWT).  
- Il foglio di lavoro deve essere memorizzato nello storage di Aspose Cloud o in una cartella specificata.  

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                         |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name           | string  | path     | Nome del documento Excel.                         |
| sheetName      | string  | path     | Nome del foglio di lavoro contenente la forma.         |
| shapeindex     | integer | path     | Indice in base zero della forma all'interno del foglio di lavoro. |
| folder         | string  | query    | Percorso della cartella in cui è memorizzato il documento.           |
| storageName    | string  | query    | Nome del servizio di archiviazione.                        |

**Nota:** `shapeindex` è in base zero; la prima forma ha indice 0. Assicurarsi che il foglio di lavoro sia memorizzato nella cartella e nello `storageName` specificati se non si utilizza lo storage predefinito.

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Endpoint e percorso corretti
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di stato HTTP possibili**

| Codice | Descrizione |
|------|-------------|
| **200 OK** | La forma è stata recuperata correttamente. |
| **400 Bad Request** | La richiesta è malformata o mancano parametri obbligatori. |
| **401 Unauthorized** | Autenticazione non riuscita o token mancante/non valido. |
| **404 Not Found** | Il foglio di lavoro, il foglio di lavoro o l'indice della forma specificati non esistono. |
| **500 Internal Server Error** | Si è verificato un errore imprevisto sul server. |

**Errori comuni:** Utilizzare un dominio di base errato (`api.aspose.com`) o il segmento obsoleto `/autoshapes/` produrrà un errore 404. Utilizzare sempre il segmento `/shapes/` con il dominio `api.aspose.cloud`.

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello e consente di concentrarsi sulle attività del progetto. Consultare il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

Gli esempi di codice seguenti mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

Per operazioni correlate, consultare la documentazione su **[Aggiungere una forma](/it/shapes/add/)** e **[Aggiornare una forma](/it/shapes/update/)**.