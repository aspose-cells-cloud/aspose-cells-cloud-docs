---
title: "Text in einem Excel-Arbeitsblatt ersetzen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Im Arbeitsblatt ersetzen"
type: docs
url: /de/worksheets/replace-text/
aliases: [  /de/replace-text-in-a-workbook/ ]
keywords: "Aspose.Cells, Text ersetzen, Excel, REST-API, Tabellenkalkulation, Arbeitsblatt"
description: "Erfahren Sie, wie Sie Text in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API (v3.0) ersetzen. Enthält Voraussetzungen, Authentifizierung, Anforderungssyntax, cURL-Beispiel, SDK-Codebeispiele, Antwortdetails und Fehlerbehandlung."
ArticleTitle: "Text in einem Excel-Arbeitsblatt ersetzen – Aspose.Cells Cloud API"
weight: 70
---

Diese REST-API ersetzt Text in einem Excel-Arbeitsblatt mithilfe der **Aspose.Cells Textersetzung-API**.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```

### Anforderungsparameter

| Parametername   | Typ    | Ort     | Beschreibung                            |
| ---------------- | ------ | ------- | --------------------------------------- |
| **name**         | string | path    | Der Name der Excel-Arbeitsmappe.        |
| **sheetName**    | string | path    | Der Name des Arbeitsblatts.             |
| **oldValue**     | string | query   | Der zu ersetzende Text.                 |
| **newValue**     | string | query   | Der Ersatztext.                         |
| **folder**       | string | query   | Der Ordner, der die Datei enthält.      |
| **storageName**  | string | query   | Der Name des Speicherdienstes.          |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200,
      "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als CSV herunterladen",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als HTML herunterladen",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als ODS herunterladen",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als PDF herunterladen",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als tabellengebundenes Textformat herunterladen",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als TIFF herunterladen",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als Microsoft Excel 2003 herunterladen",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als Microsoft Excel 2007 herunterladen",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Als XPS herunterladen",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                     |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.   |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                       |

## So verwenden Sie die PostWorksheetTextReplace-API mit SDKs

### PostWorksheetTextReplace-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace) definiert diese öffentlich zugängliche Schnittstelle.

Sie können das cURL-Befehlszeilentool verwenden, um den Dienst aufzurufen:

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/replaceText?oldValue=b&newValue=b11" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 0,
  "Worksheet": {
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1",
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


### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}