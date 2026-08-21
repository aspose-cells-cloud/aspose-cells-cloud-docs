---
title: "Zellstil aus einem Arbeitsblatt abrufen – Aspose.Cells Cloud API"
type: docs
url: /de/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, REST API, Zellstil, Tabellenkalkulation, Cloud SDK, API-Dokumentation"
description: "Erfahren Sie, wie Sie den Stil einer bestimmten Zelle in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API v3 abrufen. Enthält cURL-Beispiel, Antwortschema, Statuscodes und SDK-Snippets."
ArticleTitle: "Zellstil aus einem Arbeitsblatt mit der Aspose.Cells Cloud API abrufen – Detaillierte Anleitung"
---

Verwenden Sie diese REST API, um den **Stil** einer Zelle in einem Excel-Arbeitsblatt abzurufen.

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter


| Parametername  | Typ    | Ort   | Beschreibung                        |
| -------------- | ------ | ----- | ----------------------------------- |
| name           | string | path  | Der Name der Excel-Datei.           |
| sheetName      | string | path  | Der Name des Arbeitsblatts.         |
| cellName       | string | path  | Die Adresse der Zelle (z. B. A1).  |
| folder         | string | query | Der Ordner, der die Datei enthält.  |
| storageName    | string | query | Der Name des zu verwendenden Speichers. |


### **Antwort**

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

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zur Operation.       |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

**Fehlerantworten**  
Typische Fehlerantworten für diesen Endpunkt folgen dem standardmäßigen Aspose.Cells-Fehlerformat. Beispielsweise gibt ein 400 Bad Request zurück:

```json
{
  "Code": 400,
  "Message": "Ungültiger Parameter 'cellName'.",
  "Description": "Der angegebene Zellname ist nicht im gültigen A1-Format."
}
```

Ebenso gibt ein 401 Unauthorized zurück:

```json
{
  "Code": 401,
  "Message": "Authentifizierung fehlgeschlagen.",
  "Description": "Das JWT-Token fehlt oder ist ungültig."
}
```

## Verwendung der GetWorksheetCellStyle API mit SDKs

### GetWorksheetCellStyle API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

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

## Antwortschema

| Feld                      | Typ    | Beschreibung                                                             |
| ------------------------- | ------ | ------------------------------------------------------------------------ |
| **Style**                 | object | Container für alle stilbezogenen Eigenschaften der Zelle.               |
| Style.Font                | object | Schriftarteinstellungen (Name, Größe, Farbe, Stilflags).                 |
| Style.Font.Color          | object | RGBA-Farbwerte für die Schriftart.                                        |
| Style.Font.IsBold         | boolean | `true`, wenn die Schriftart fett ist.                                   |
| Style.Font.IsItalic       | boolean | `true`, wenn die Schriftart kursiv ist.                                  |
| Style.Font.IsStrikeout    | boolean | `true`, wenn die Schriftart durchgestrichen ist.                         |
| Style.Font.IsSubscript    | boolean | `true`, wenn die Schriftart tiefgestellt ist.                            |
| Style.Font.IsSuperscript  | boolean | `true`, wenn die Schriftart hochgestellt ist.                            |
| Style.Font.Name           | string  | Schriftfamilienname (z. B. **Calibri**).                                |
| Style.Font.Size           | number  | Schriftgröße in Punkten.                                                 |
| Style.Font.Underline      | string  | Unterstreichungsstil (z. B. **Single**).                                |
| Style.IsLocked            | boolean | Gibt an, ob die Zelle vor Bearbeitung geschützt ist.                     |
| Style.IsTextWrapped       | boolean | `true`, wenn Textumbruch aktiviert ist.                                  |
| Style.IsGradient          | boolean | `true`, wenn ein Farbverlaufsfüllmuster angewendet ist.                  |
| Style.Pattern             | string  | Füllmustername (z. B. **None**).                                         |
| Style.BorderCollection    | array   | Liste von Randobjekten mit Linienstil, Farbe und Randtyp.                |
| Style.BackgroundColor     | object  | RGBA-Werte für den Zellhintergrund.                                      |
| Style.ForegroundColor     | object  | RGBA-Werte für den Zellvordergrund.                                      |
| …                         | …       | _(Weitere Felder folgen demselben Muster wie in der API-Referenz definiert.)_ |

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene, sodass Sie sich auf Ihre Projektziele konzentrieren können. Schauen Sie sich das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

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

**Siehe auch**  
- [Zellstil festlegen](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [Zellwert abrufen](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---