---
title: Byt ut text i ett Excel arbetsblad
second_title: Aspose.Cells Cloud Documen
linktitle: Byt ut i arbetssläden
type: docs
url: /sv/replace-text-in-a-worksheet/
url: /sv/worksheets/replace-text/
aliases: [/replace-text-in-a-workbook/]
keywords: Find text from Microsoft Excel (XLS, XLSX, XLSM, XLSB) and Open Document Spreadsheet (ODS) worksheet
description: Aspose.Cells Cloud REST API stöder att hitta text från Excel kalkylblad. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 70
---
Denna REST API indikerar till `replace` text i ett Excel kalkylblad.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokument namn.|
| arknamn| sträng| väg| Arbetsbladsnamn.|
| gammalt värde| sträng| fråga| Den gamla texten ska ersättas.|
| nyttVärde| sträng| fråga| Den nya texten att ersätta med.|
| mapp| sträng| fråga| Dokumentets mapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorsheetTextReplace) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/replaceText?oldValue=b&newValue=b11" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

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

## Cloud SDK-familj
 
 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Text-ReplaceTextWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-text-ReplaceTextWorksheet-replace-text-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Text-PostWorsheetTextReplace-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-replace_text-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ReplaceTextInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Text-ReplaceTextWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-text-ReplaceTextWorksheet-replace-text-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Text-ReplaceTextWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "ff17714a94632832ff5ae7d77ba511f6" >}}

{{< /tab >}}

{{< /tabs >}}
