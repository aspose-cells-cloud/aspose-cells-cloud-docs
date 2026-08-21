---
title: "Ersätt text i en Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Ersätt i arbetsbok"
type: docs
url: /sv/workbook/replace-text/
aliases: [  /sv/replace-text-in-a-workbook/ ]
weight: 60
keywords: "Aspose.Cells Cloud, Ersätt text, Excel-arbetsbok, XLSX, ODS, REST API, Kalkylark, SDK"
description: "Ersätt text i Excel-filer (XLS, XLSX, XLSM, XLSB) och OpenDocument-kalkylark (ODS) med Aspose.Cells Cloud REST API. Tillgängligt via cURL och ett stort urval SDK:er (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, m.fl.)."
---

Denna REST API ersätter text i en Excel-arbetsbok.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```
### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parametername   | Typ    | Plats  | Beskrivning                                              |
| --------------- | ------ | ------ | -------------------------------------------------------- |
| name            | string | path   | Namn på arbetsboksfilen.                                 |
| sheetName       | string | path   | Namn på kalkylbladet där ersättningen ska ske.          |
| oldValue        | string | query  | Text som ska ersättas.                                   |
| newValue        | string | query  | Text som ska ersätta den gamla texten.                   |
| folder          | string | query  | Mappväg som innehåller arbetsboken.                      |
| storageName     | string | query  | Namn på lagringstjänsten där arbetsboken finns.          |

### **Svar**

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
        "Title": "Ladda ner som CSV",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Ladda ner som HTML",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Ladda ner som ODS",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Ladda ner som PDF",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Ladda ner som tabellavgränsad textformat",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Ladda ner som TIFF",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Ladda ner som Microsoft Excel 2003",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Ladda ner som Microsoft Excel 2007",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Ladda ner som XPS",
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

**HTTP-statuskoder**

| Kod | Betydelse                 | Beskrivning                                             |
|-----|---------------------------|---------------------------------------------------------|
| 200 | OK                        | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktorisering saknas      | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast        | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel         | Oväntat serverfel.                                      |

## Hur man använder PostReplace API med SDK:er

### PostReplace API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt anropa Aspose.Cells webbtjänster. Exemplet nedan visar hur man gör en begäran med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att integrera den här funktionen. En SDK hanterar detaljer på låg nivå, så att du kan fokusera på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

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