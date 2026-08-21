---
title: "Sammanfoga en Excel-arbetsbok i en annan arbetsbok"
second_title: "Dokument"
linktitle: "Sammanfoga en Excel-arbetsbok i en annan arbetsbok"
type: docs
url: /sv/merge-an-excel-file-into-the-excel-file/
aliases: [  /sv/merge-excel-workbooks/ , /sv/workbook/merge/ ]
keywords: "Excel-sammanfogning, Aspose.Cells Cloud, arbetsboks-API, REST-API, kalkylbladssammanfogning, molntjänst, autentisering, mergeWith, cURL-exempel"
description: "Steg-för-steg-guide för att sammanfoga en Excel-arbetsbok i en annan med Aspose.Cells Cloud REST API (v3.0). Inkluderar autentisering, nödvändig mergeWith-parameter, cURL-exempel och SDK-kodavsnitt."
ArticleTitle: "Sammanfoga en Excel-arbetsbok i en annan arbetsbok med Aspose.Cells Cloud API"
weight: 50
---

## REST-API

Detta REST-API sammanfogar en Excel-**arbetsbok** i en annan arbetsbok.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/merge
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### **Frågeparameter**

| Parameternamn   | Typ    | Beskrivning                                                   |
| --------------- | ------ | ------------------------------------------------------------- |
| folder          | string | Mapp som innehåller den ursprungliga arbetsboken.             |
| storageName     | string | Namn på lagringsutrymmet.                                     |
| **mergeWith**   | string | Namn på den arbetsbok som ska sammanfogas till målarbetsboken. |

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
        "Title": "Ladda ner som tabellavgränsat textformat",
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

| Kod | Betydelse                   | Beskrivning                                         |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filter har tillämpats framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur du använder PostWorkbooksMerge-API:et med SDK:er

### PostWorkbooksMerge API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt för API:et att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL, inklusive nödvändiga autentiseringshuvuden.


{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Sammanfoga test2.xlsx till test.xlsx
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/merge?mergeWith=test2.xlsx" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access-token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
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
        "Title": "Ladda ner som tabellavgränsat textformat",
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
  },
  "Code": 200,
  "Status": "OK"
}
```

Svaret returnerar ett `Workbook`-objekt som innehåller metadata om den sammanfogade arbetsboken, inklusive länkar för att ladda ner resultatet i olika format (CSV, PDF, HTML, etc.).

Svarshuvuden

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---