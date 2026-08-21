---
title: "Zellwert festlegen – Aspose.Cells Cloud API Referenz (v3.0)"  
type: docs  
url: /de/set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "Aspose Cells API Zellwert festlegen, Excel Zellupdate REST, Aspose.Cells Cloud cURL Beispiel"  
description: "Erfahren Sie, wie Sie den Wert einer bestimmten Zelle in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API festlegen. Enthält Anforderungssyntax, Parameter, HTTPS cURL Beispiel und SDK-Codebeispiele."  
---  

Diese REST API setzt den **Zellwert** in einer Excel-Datei.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Anforderungsparameter**

| Name          | Type   | Location | Beschreibung                                   |
|---------------|--------|----------|------------------------------------------------|
| name          | string | path     | Name der Excel-Datei (einschließlich Erweiterung). |
| sheetName     | string | path     | Name des Arbeitsblatts (Groß-/Kleinschreibung beachten). |
| cellName      | string | path     | A1-ähnliche Adresse der Zielzelle (z. B. `A1`). |
| value         | string | query    | Wert, der der Zelle zugewiesen werden soll. |
| type          | string | query    | Datentyp des Werts (`int`, `string`, `float`, etc.). |
| formula       | string | query    | Formel, die auf die Zelle angewendet werden soll (optional). |
| folder        | string | query    | Ordner, der das Dokument enthält (optional). |
| storageName   | string | query    | Name des Speichers, in dem sich die Datei befindet (optional). |

## **Antwort**

Gibt CellResponse zurück.

- **Übersicht der Antwortfelder**

| Feld            | Type    | Beschreibung                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Adresse der Zelle (z. B. `F341`).                   |
| `Row`           | integer | Nullbasierter Zeilenindex.                                 |
| `Column`        | integer | Nullbasierter Spaltenindex.                              |
| `Value`         | string  | Der angezeigte Wert der Zelle.                           |
| `Type`          | string  | Datentyp der Zelle (z. B. `IsString`).             |
| `Formula`       | string  | Formeltext, sofern die Zelle eine Formel enthält.          |
| `IsFormula`     | bool    | Gibt an, ob die Zelle eine Formel enthält.        |
| `IsMerged`      | bool    | Gibt an, ob die Zelle Teil eines zusammengeführten Bereichs ist. |
| `IsArrayHeader` | bool    | Gibt an, ob die Zelle ein Array-Header ist.        |
| `IsInArray`     | bool    | Gibt an, ob die Zelle Teil eines Arrays ist.       |
| `IsErrorValue`  | bool    | Gibt an, ob die Zelle einen Fehlerwert enthält.   |
| `IsInTable`     | bool    | Gibt an, ob die Zelle innerhalb einer Tabelle steht.         |
| `IsStyleSet`    | bool    | Gibt an, ob ein Stil auf die Zelle angewendet wurde.     |
| `HtmlString`    | string  | HTML-kodierte Darstellung des Zellwerts.      |
| `Style.link`    | object  | Hyperlink zur Stil-Ressource.                      |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                     | Beschreibung                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zur Operation. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbegrenzung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |
## Verwendung der PostWorksheetCellSetValue API mit SDKs

### Spezifikation der PostWorksheetCellSetValue API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) definiert eine öffentlich zugängliche Programmierschnittstelle, die Entwicklern ermöglicht, REST-Endpunkte direkt aus einem Browser oder einem beliebigen HTTP-Client aufzurufen.

Sie können das Kommandozeilenwerkzeug **cURL** verwenden, um Aspose.Cells-Webdienste aufzurufen. Das folgende Beispiel zeigt, wie Sie einen Zellwert mit cURL festlegen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
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
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK beschleunigt die Entwicklung, da sie sich um die Details der niedrigen Ebene kümmert, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie Aspose.Cells-Webdienste mit verschiedenen SDKs aufrufen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}