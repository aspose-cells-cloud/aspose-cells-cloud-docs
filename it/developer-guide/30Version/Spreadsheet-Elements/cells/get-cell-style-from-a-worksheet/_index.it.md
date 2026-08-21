---
title: "Ottenere lo stile di una cella da un foglio di calcolo – Aspose.Cells Cloud API"
type: docs
url: /it/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, API REST, stile cella, foglio di calcolo, SDK cloud, documentazione API"
description: "Scopri come recuperare lo stile di una cella specifica in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud v3. Include esempio cURL, schema di risposta, codici di stato e frammenti SDK."
ArticleTitle: "Ottenere lo stile di una cella da un foglio di calcolo tramite Aspose.Cells Cloud API – Guida dettagliata"
---

Utilizza questa API REST per recuperare lo **stile** di una cella in un foglio di calcolo Excel.

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della richiesta


| Nome parametro | Tipo   | Posizione | Descrizione                         |
| -------------- | ------ | -------- | ----------------------------------- |
| name           | string | path     | Nome del documento Excel.           |
| sheetName      | string | path     | Nome del foglio di calcolo.         |
| cellName       | string | path     | Indirizzo della cella (es. A1).     |
| folder         | string | query    | Cartella contenente il file.        |
| storageName    | string | query    | Nome dello storage da utilizzare.   |


### **Risposta**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto sul server. |

**Risposte di errore**  
I payload di errore tipici per questo endpoint seguono il formato standard di errore di Aspose.Cells. Ad esempio, un errore 400 Bad Request restituisce:

```json
{
  "Code": 400,
  "Message": "Parametro 'cellName' non valido.",
  "Description": "Il nome della cella fornito non è in un formato A1 valido."
}
```

Analogamente, un errore 401 Unauthorized restituisce:

```json
{
  "Code": 401,
  "Message": "Autenticazione non riuscita.",
  "Description": "Il token JWT è mancante o non valido."
}
```

## Come utilizzare l'API GetWorksheetCellStyle con gli SDK

### Specifica dell'API GetWorksheetCellStyle


La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) definiscono un’interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare una chiamata all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Schema della risposta

| Campo                    | Tipo    | Descrizione                                                               |
| ------------------------ | ------- | ------------------------------------------------------------------------- |
| **Style**                | object  | Contenitore per tutte le proprietà relative allo stile della cella.       |
| Style.Font               | object  | Impostazioni del font (nome, dimensione, colore, flag di stile).           |
| Style.Font.Color         | object  | Valori colore RGBA per il font.                                           |
| Style.Font.IsBold        | boolean | `true` se il font è in grassetto.                                         |
| Style.Font.IsItalic      | boolean | `true` se il font è in corsivo.                                           |
| Style.Font.IsStrikeout   | boolean | `true` se il font è barrato.                                              |
| Style.Font.IsSubscript   | boolean | `true` se il font è in pedice.                                            |
| Style.Font.IsSuperscript | boolean | `true` se il font è in apice.                                             |
| Style.Font.Name          | string  | Nome del font (es. **Calibri**).                                          |
| Style.Font.Size          | number  | Dimensione del font in punti.                                             |
| Style.Font.Underline     | string  | Stile di sottolineatura (es. **Single**).                                 |
| Style.IsLocked           | boolean | Indica se la cella è protetta dalla modifica.                             |
| Style.IsTextWrapped      | boolean | `true` se l'incapsulamento del testo è abilitato.                         |
| Style.IsGradient         | boolean | `true` se è applicato un riempimento gradiente.                           |
| Style.Pattern            | string  | Nome del modello di riempimento (es. **None**).                           |
| Style.BorderCollection   | array   | Elenco di oggetti di bordo che definiscono lo stile di linea, il colore e il tipo di bordo. |
| Style.BackgroundColor    | object  | Valori RGBA per lo sfondo della cella.                                    |
| Style.ForegroundColor    | object  | Valori RGBA per il primo piano della cella.                               |
| …                        | …       | _(Altri campi seguono lo stesso schema definito nel riferimento API.)_ |

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta la [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Vedi anche**  
- [Imposta stile cella](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [Ottieni valore cella](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---