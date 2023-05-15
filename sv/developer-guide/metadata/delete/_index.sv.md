---
title: Ta bort metadata på Excel-filer
second_title: Aspose.Cells Cloud Documen
linktitle: Radera utan att använda lagring
type: docs
url: /sv/metadata/delete/
keywords: Deleting metadata from Excel files
description: Aspose.Cells Cloud REST API stöder radering av metadata från Excel-filer. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 55
---
Denna REST API indikerar att `metadata` ska raderas från flera Excel filer.


## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/metadata/delete
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| fil| fil| formData| Fil att ladda upp|
| typ| sträng| fråga| Allt|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/DeleteMetadata) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/metadata/delete" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'  
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-familj


 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Metedata-Delete.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-MetaData-Delete.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Metadata-Delete.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}
{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LiteCellsMetadata-Delete.py" >}}
{{< /tab >}}
{{< /tabs >}}
