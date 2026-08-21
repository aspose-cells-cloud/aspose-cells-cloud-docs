---
title: "Aggiorna un oggetto OLE in un foglio di calcolo Excel"
second_title: "Document"
linktype: "Aggiorna"
type: docs
url: /it/oleobjects/update/
aliases: [/it/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "aggiornare oggetto OLE, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Scopri come aggiornare un oggetto OLE (immagine, grafico, ecc.) in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi in cURL, SDK, passaggi per l'autenticazione e gestione degli errori."
weight: 30
author: "Team documentazione Aspose Cloud"
lastmod: "2024-03-01"
ArticleTitle: "Aggiorna un oggetto OLE in un foglio di calcolo Excel – Guida all'API di Aspose.Cells Cloud"
---

Questa API REST aggiorna un **oggetto OLE** in un foglio di calcolo Excel.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

## API PostUpdateWorksheetOleObject

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

I parametri della richiesta sono:

| Nome parametro | Tipo    | Posizione parametro | Descrizione                                           |
| -------------- | ------- | ------------------ | ---------------------------------------------------- |
| name           | string  | path               | Nome del workbook.                                   |
| sheetName      | string  | path               | Nome del foglio di calcolo.                          |
| oleObjectIndex | integer | path               | Indice dell'oggetto OLE all'interno del foglio.      |
| ole            | object  | body               | Rappresentazione JSON dell'oggetto OLE da aggiornare. |
| folder         | string  | query              | Cartella contenente il workbook.                     |
| storageName    | string  | query              | Nome del servizio di archiviazione.                  |

### Campi del corpo della richiesta

| Campo               | Tipo    | Obbligatorio | Descrizione                                               |
| ------------------- | ------- | ------------ | --------------------------------------------------------- |
| ImageSourceFullName | string  | opzionale    | Percorso del file immagine utilizzato per l'oggetto OLE. |
| IsAutoSize          | boolean | opzionale    | Indica se l'oggetto OLE deve essere ridimensionato automaticamente. |
| SourceFullName      | string  | obbligatorio | File sorgente (ad esempio, un'immagine o un grafico) per l'oggetto OLE. |
| UpperLeftRow        | integer | obbligatorio | Indice di riga (in base zero) dell'angolo superiore sinistro. |
| UpperLeftColumn     | integer | obbligatorio | Indice di colonna (in base zero) dell'angolo superiore sinistro. |
| Left                | integer | opzionale    | Spostamento orizzontale, in punti, dall'angolo superiore sinistro. |
| Top                 | integer | opzionale    | Spostamento verticale, in punti, dall'angolo superiore sinistro. |
| Width               | integer | obbligatorio | Larghezza dell'oggetto OLE, in punti.                    |
| Height              | integer | obbligatorio | Altezza dell'oggetto OLE, in punti.                      |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
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
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Risposte di errore

| Stato HTTP | Codice | Messaggio                                                         |
| ---------- | ------ | ----------------------------------------------------------------- |
| 400        | 4000   | Richiesta non valida – parametri mancanti o non validi.           |
| 401        | 4010   | Non autorizzato – token JWT non valido o mancante.                |
| 404        | 4040   | Non trovato – workbook, foglio di calcolo o oggetto OLE inesistente. |
| 500        | 5000   | Errore interno del server – errore imprevisto lato server.        |

L'API restituisce inoltre un campo personalizzato **Code** nel corpo della risposta che corrisponde allo stato HTTP (ad esempio, 200 → 2000, 400 → 4000, ecc.).

## Quando utilizzare questa API?

Utilizzare questo endpoint quando è necessario modificare un oggetto OLE esistente—ad esempio un'immagine, un grafico o un documento incorporato—senza dover caricare nuovamente l'intero foglio di calcolo. Gli scenari tipici includono l'aggiornamento della fonte immagine, il ridimensionamento dell'oggetto o la modifica della sua posizione dopo la generazione del workbook. Per operazioni correlate, vedere [Aggiungi un oggetto OLE](/it/oleobjects/add/) e [Elimina un oggetto OLE](/it/oleobjects/delete/).

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

Di seguito è riportato un breve esempio in C# che aggiorna un oggetto OLE utilizzando l'SDK di Aspose.Cells Cloud:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}