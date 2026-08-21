---
title: "Zellen-Eigenschaften abrufen"
type: docs
url: /de/get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, Arbeitsblatt, Zelleneigenschaften, Zellen-Eigenschaften abrufen"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST API die Eigenschaften einer bestimmten Zelle oder vordefinierter Zellmethoden in einem Excel-Arbeitsblatt abrufen."
---

Diese REST API demonstriert, wie eine bestimmte Zelle in einer Excel-Datei abgerufen wird.

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Anforderungsparameter


| Parametername        | Typ    | Ort     | Beschreibung                                                                                                                                                                                                 |
| -------------------- | ------ | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**             | string | path    | Der Name der Excel-Datei.                                                                                                                                                                                    |
| **sheetName**        | string | path    | Der Name des Arbeitsblatts, das die Zelle enthält.                                                                                                                                                           |
| **cellOrMethodName** | string | path    | Der Zellenname oder ein vordefinierter Methodenname (z. B. `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`).              |
| **folder**           | string | query   | Der Ordner, in dem das Dokument gespeichert ist.                                                                                                                                                             |
| **storageName**      | string | query   | Der Name des Speicherdienstes.                                                                                                                                                                               |

## **Antwort**

Gibt die `CellResponse` zurück.

- **Übersicht der Antwortfelder**

| Feld            | Typ     | Beschreibung                                          |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Adresse der Zelle (z. B. `F341`).                    |
| `Row`           | integer | Nullbasierter Zeilenindex.                            |
| `Column`        | integer | Nullbasierter Spaltenindex.                           |
| `Value`         | string  | Der angezeigte Wert der Zelle.                        |
| `Type`          | string  | Datentyp der Zelle (z. B. `IsString`).                |
| `Formula`       | string  | Formeltext, falls die Zelle eine Formel enthält.     |
| `IsFormula`     | bool    | Gibt an, ob die Zelle eine Formel enthält.            |
| `IsMerged`      | bool    | Gibt an, ob die Zelle Teil eines zusammengeführten Bereichs ist. |
| `IsArrayHeader` | bool    | Gibt an, ob die Zelle ein Array-Header ist.           |
| `IsInArray`     | bool    | Gibt an, ob die Zelle Teil eines Arrays ist.          |
| `IsErrorValue`  | bool    | Gibt an, ob die Zelle einen Fehlerwert enthält.       |
| `IsInTable`     | bool    | Gibt an, ob sich die Zelle innerhalb einer Tabelle befindet. |
| `IsStyleSet`    | bool    | Gibt an, ob ein Stil auf die Zelle angewendet wurde.  |
| `HtmlString`    | string  | HTML-kodierte Darstellung des Zellenwerts.            |
| `Style.link`    | object  | Hyperlink zur Stilressource.                          |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.               |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Verwendung der GetWorksheetCell-API mit SDKs

### GetWorksheetCell-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der effizienteste Weg, die Entwicklung zu beschleunigen. Ein SDK abstractisiert Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs einzusehen.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### So rufen Sie eine bestimmte Zelle ab

- [Zelldaten aus einem Arbeitsblatt abrufen](/de/cells/get-cell-data-from-a-worksheet/)
- [Erste Zelle aus Excel-Arbeitsblatt abrufen](/de/cells/get-first-cell-from-excel-worksheet/)
- [Letzte Zelle des Excel-Arbeitsblatts abrufen](/de/cells/get-last-cell-of-excel-worksheet/)
- [MaxRow aus Excel-Arbeitsblatt abrufen](/de/cells/get-maxrow-from-excel-worksheet/)
- [MaxDataRow aus Excel-Arbeitsblatt abrufen](/de/cells/get-maxdatarow-from-excel-worksheet/)
- [MaxColumn aus Excel-Arbeitsblatt abrufen](/de/cells/get-maxcolumn-from-excel-worksheet/)
- [MaxDataColumn aus Excel-Arbeitsblatt abrufen](/de/cells/get-maxdatacolumn-from-excel-worksheet/)
- [MinRow aus Excel-Arbeitsblatt abrufen](/de/cells/get-minrow-from-excel-worksheet/)
- [MinDataRow aus Excel-Arbeitsblatt abrufen](/de/cells/get-mindatarow-from-excel-worksheet/)
- [MinColumn aus Excel-Arbeitsblatt abrufen](/de/cells/get-mincolumn-from-excel-worksheet/)
- [MinDataColumn aus Excel-Arbeitsblatt abrufen](/de/cells/get-mindatacolumn-from-excel-worksheet/)