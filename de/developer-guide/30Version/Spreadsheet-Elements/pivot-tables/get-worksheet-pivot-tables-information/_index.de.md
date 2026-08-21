---
title: "Alle Pivot-Tabellen in einem Excel-Arbeitsblatt abrufen"
second_title: "Dokument"
linktitle: Alle abrufen
type: docs
url: /de/pivot-tables/get-all/
aliases: [  /de/get-worksheet-pivot-tables-information/ ]
keywords: "alle Pivot-Tabellen abrufen, Aspose.Cells Cloud API, Excel PivotTable, REST API"
description: "Rufen Sie alle Pivot-Tabellen aus einem Excel-Arbeitsblatt über die Aspose.Cells Cloud API ab. Enthält Endpunkt, Parameter, Authentifizierungsschritte, cURL- und SDK-Beispiele für die PivotTables API."
weight: 20
ArticleTitle: "Alle Pivot-Tabellen in einem Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API"
---

Ein **PivotTable** (Pivot-Tabelle) ist ein Datenzusammenfassungstool in Excel, mit dem Sie große Datensätze neu ordnen und analysieren können. Diese REST-API ruft Informationen zu **allen** Pivot-Tabellen in einem angegebenen Arbeitsblatt ab.

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Anforderungsparameter**

| Parametername | Typ   | Position | Beschreibung                                |
| ------------- | ----- | -------- | ------------------------------------------- |
| name          | string | Pfad     | Name der Excel-Datei.                       |
| sheetName     | string | Pfad     | Name des Arbeitsblatts.                     |
| folder        | string | Abfrage  | Ordner, in dem das Dokument gespeichert ist. |
| storageName   | string | Abfrage  | Name des Speicherdienstes.                  |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Anforderung

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### Antwort

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Fehlerantworten

| HTTP-Code | Beschreibung                                                     | Beispiel-JSON-Payload                                         |
| --------- | ---------------------------------------------------------------- | ------------------------------------------------------------- |
| 400       | Ungültige Anforderung – erforderlicher Parameter fehlt.        | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401       | Nicht autorisiert – ungültiges oder fehlendes Token.           | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404       | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Pivot-Tabelle existiert nicht. | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500       | Interner Serverfehler – unerwarteter Zustand auf dem Server.   | `{ "Code": "500", "Message": "Server error." }`               |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Methode zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}
---