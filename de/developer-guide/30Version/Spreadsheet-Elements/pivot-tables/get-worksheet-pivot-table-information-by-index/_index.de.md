---
title: "Abrufen einer Pivot-Tabelle in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: Abrufen
type: docs
url: /pivot-tables/get/
aliases: [/get-worksheet-pivot-table-information-by-index/]
keywords: "Aspose.Cells, Pivot-Tabelle, Excel, REST-API, Arbeitsblatt-Pivot-Tabelle abrufen"
description: "Abrufen einer Pivot-Tabelle aus einem Excel-Arbeitsblatt über die Aspose.Cells Cloud REST-API. Enthält Anforderungssyntax, Parameter, Authentifizierung, Antwortschema, Fehlerbehandlung und SDK-Beispiele."
weight: 10
ArticleTitle: "Abrufen einer Pivot-Tabelle in einem Excel-Arbeitsblatt"
---

Diese REST-API ruft Informationen zur **Pivot-Tabelle** in einem Arbeitsblatt anhand ihres Index ab.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## REST-API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### Anforderungsparameter

| Parametername       | Typ     | Ort      | Beschreibung                                                 |
| ------------------- | ------- | -------- | ------------------------------------------------------------ |
| **name**            | string  | path     | Der Name der Excel-Datei.                                    |
| **sheetName**       | string  | path     | Der Name des Arbeitsblatts, das die Pivot-Tabelle enthält.  |
| **pivottableIndex** | integer | path     | Nullbasierter Index der Pivot-Tabelle im Arbeitsblatt.      |
| **folder**          | string  | query    | Der Ordner, in dem das Dokument gespeichert ist.            |
| **storageName**     | string  | query    | Der Name des Aspose Cloud-Speichers.                         |

Sie können das Befehlszeilentool **cURL** verwenden, um problemlos auf die Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
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
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**Antwort-Schema**

| Feld            | Typ     | Beschreibung                                           |
|-----------------|---------|--------------------------------------------------------|
| Status          | string  | Statusnachricht des Vorgangs (z. B. „OK“).            |
| PivotFilters    | array   | Sammlung von Pivot-Filterdefinitionen.                |
| └─ AutoFilter   | object  | Details zur automatischen Filterung der Pivot-Tabelle.|
|    └─ link      | object  | Hyperlink-Informationen für den Filter.               |
|    └─ FilterColumns | array | Einzeldaten zu Spaltenfiltereinstellungen.        |
|    └─ Range     | string  | Zellbereich, auf den der Filter angewendet wird.      |
|    └─ Sorter    | object  | Sortierkonfiguration für die gefilterten Daten.       |
| (zusätzliche verschachtelte Felder folgen derselben Struktur wie im Beispiel-JSON) |

{{< /tab >}}

{{< /tabs >}}

### Fehlerbehandlung

Die API verwendet standardmäßige HTTP-Statuscodes. Typische Antworten sind:

| Statuscode | Bedeutung                                                              | Beispiel-JSON (Fehler)                            |
| ---------- | ---------------------------------------------------------------------- | ------------------------------------------------- |
| 200        | Erfolg – die Pivot-Tabelle wurde zurückgegeben                         | —                                                 |
| 401        | Nicht autorisiert – ungültiges oder fehlendes Token                   | `{"code":401,"message":"Invalid access token."}`  |
| 404        | Nicht gefunden – Datei, Arbeitsblatt oder Pivot-Table-Index existiert nicht | `{"code":404,"message":"Pivot table not found."}` |
| 500        | Serverfehler – unerwarteter Zustand                                    | `{"code":500,"message":"Internal server error."}` |

**Hinweise:** Die API unterstützt Excel-Dateien bis zu 150 MB und arbeitet mit Excel-Formaten von 2007 bis 2021. Der Name des Arbeitsblatts unterscheidet zwischen Groß- und Kleinschreibung.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}