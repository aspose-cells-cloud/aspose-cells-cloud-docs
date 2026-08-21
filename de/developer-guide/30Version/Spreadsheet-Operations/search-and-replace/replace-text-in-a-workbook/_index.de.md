---
title: "Text in einer Excel-Arbeitsmapme ersetzen"
second_title: "Dokument"
linktitle: "In Arbeitsmappe ersetzen"
type: docs
url: /de/workbook/replace-text/
aliases: [  /de/replace-text-in-a-workbook/ ]
weight: 60
keywords: "Aspose.Cells Cloud, Text ersetzen, Excel-Arbeitsmappe, XLSX, ODS, REST API, Tabellenkalkulation, SDK"
description: "Ersetzen Sie Text in Excel-Dateien (XLS, XLSX, XLSM, XLSB) und OpenDocument-Tabellenkalkulationen (ODS) mithilfe der Aspose.Cells Cloud REST API. Verfügbar über cURL und eine breite Palette an SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go usw.)."
---

Diese REST API ersetzt Text in einer Excel-Arbeitsmappe.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```
### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ   | Ort   | Beschreibung                                           |
| ------------- | ----- | ----- | ------------------------------------------------------ |
| name          | string | path  | Name der Arbeitsmappen-Datei.                         |
| sheetName     | string | path  | Name des Arbeitsblatts, in dem die Ersetzung stattfindet. |
| oldValue      | string | query | Text, der ersetzt werden soll.                         |
| newValue      | string | query | Text, der den alten Wert ersetzen soll.               |
| folder        | string | query | Ordnerpfad, der die Arbeitsmappe enthält.             |
| storageName   | string | query | Name des Speicherdienstes, in dem sich die Arbeitsmappe befindet. |

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
        "Title": "Als tabellengestütztes Textformat herunterladen",
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

| Code | Bedeutung                   | Beschreibung                                              |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details des Vorgangs. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                     |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.    |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                |

## Verwendung der PostReplace-API mit SDKs

### PostReplace-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie eine Anforderung mit cURL gestellt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/replaceText?oldValue=a&newValue=a12" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 26,
  "Workbook": {
    "link": {
      "Href": "/test.xlsx",
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

Die Verwendung eines SDK ist die schnellste Methode, um diese Funktionalität zu integrieren. Ein SDK übernimmt die Details der unteren Schichten, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}