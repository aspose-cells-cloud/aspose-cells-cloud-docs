---
title: "Zellendaten basierend auf benanntem Bereich abrufen"
second_title: "Dokument"
linktitle: "Werte"
type: docs
url: /ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: "Aspose.Cells, Cloud, REST-API, Excel, benannter Bereich, Zellwerte, Arbeitsblatt"
description: "Rufen Sie Zellwerte aus einem benannten Bereich in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API ab. Der Dienst ist über mehrere SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) verfügbar und läuft auf einer breiten Palette von Entwicklungsplattformen."
weight: 20
ArticleTitle: "Zellendaten basierend auf benanntem Bereich abrufen – Aspose.Cells Cloud API"
---

**Voraussetzungen**

- Ein gültiges JWT-Zugriffstoken mit der entsprechenden Berechtigung.  
- Die Arbeitsmappe muss in den Aspose Cloud-Speicher (oder einen angegebenen Ordner) hochgeladen sein.  
- Stellen Sie sicher, dass der Name des Ziel-Speichers angegeben wird, wenn ein von Standard abweichender Speicher verwendet wird.

Diese REST-API gibt eine Liste von Zellen innerhalb eines Bereichs zurück, der entweder durch einen benannten Bereich oder durch Zeilen-/Spaltenindizes identifiziert wird.

Mit diesem Vorgang können Entwickler programmgesteuert die Werte von Zellen abrufen, die zu einem bestimmten benannten Bereich in einem Excel-Arbeitsblatt gehören. Indem entweder der Bezeichner `namedRange` oder explizite Zeilen- und Spaltenindizes übergeben werden, gibt die API eine detaillierte Liste der Zellen zurück, einschließlich ihrer Adresse, Zeile, Spalte, des Werts, des Datentyps und der Formatierungsinformationen. Die Antwort kann verwendet werden, um datengetriebene Anwendungen zu steuern, Berichte zu generieren oder weitere Berechnungen serverseitig durchzuführen. Der Aspose.Cells Cloud-Dienst unterstützt mehrere Programmiersprachen über seine SDKs und gewährleistet eine nahtlose Integration unabhängig von der Entwicklungsplattform. Die Verwendung von HTTPS garantiert die sichere Übertragung der Daten, und die API richtet sich nach RESTful-Prinzipien, wobei standardmäßige HTTP-Statuscodes für Erfolgs- und Fehlerbedingungen zurückgegeben werden.

## REST-API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **Anforderungsparameter**

| Parametername | Typ    | Ort      | Beschreibung                                                                                      |
| ------------- | ------ | -------- | ------------------------------------------------------------------------------------------------- |
| name          | string | path     | Der Name der Arbeitsmappendatei.                                                                  |
| sheetName     | string | path     | Der Name des Arbeitsblatts innerhalb der Arbeitsmappe.                                           |
| namedRange    | string | query    | Der abzurufende benannte Bereich, z. B. `A1:B2` oder `range_name1`.                             |
| firstRow      | integer | query   | Nullbasierter Index der ersten Zeile des Bereichs (wird verwendet, wenn `namedRange` nicht angegeben ist). |
| firstColumn   | integer | query   | Nullbasierter Index der ersten Spalte des Bereichs (wird verwendet, wenn `namedRange` nicht angegeben ist). |
| rowCount      | integer | query   | Anzahl der im Bereich einzuschließenden Zeilen.                                                   |
| columnCount   | integer | query   | Anzahl der im Bereich einzuschließenden Spalten.                                                  |
| folder        | string | query    | Der Ordner, der die Arbeitsmappe enthält.                                                        |
| storageName   | string | query    | Der Name des Cloud-Speichers, in dem sich die Arbeitsmappe befindet.                             |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices problemlos aufzurufen. Das folgende Beispiel zeigt, wie Zellwerte aus einem benannten Bereich angefordert werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Sicherheitshinweis:** Verwenden Sie bei Aufruf der API stets HTTPS. Der Dienst unterstützt keinen unverschlüsselten HTTP-Verkehr; HTTPS stellt sicher, dass die Anfrage verschlüsselt ist und bewährten Sicherheitspraktiken entspricht.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.        |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

**Beispiel einer Fehlerantwort (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Der Parameter 'namedRange' fehlt oder ist ungültig."
}
```

> **Tipp:** Die API verwendet nullbasierte Indizes für `firstRow` und `firstColumn`. Die erste Zeile des Arbeitsblatts ist beispielsweise `0`.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der effizienteste Weg, die Entwicklung zu beschleunigen. Ein SDK abstrahiert low-level-Details, sodass Sie sich auf die Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}