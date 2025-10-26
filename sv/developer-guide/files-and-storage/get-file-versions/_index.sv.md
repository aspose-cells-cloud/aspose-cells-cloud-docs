---
title: Hämta filversion
second_title: Documen
linktitle: Hämta filversion
type: docs
url: /sv/get-file-versions/
keywords: file versions, Excel API, Office Cloud, REST API, spreadsheet management, document histor
description: Hämta och hantera versioner av filer som lagras i Aspose.Cells-molnet, vilket förbättrar dokumenthantering och samarbete
weight: 100
kwords: Hämta filversioner, Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, dokumenthantering
---
## **Excel API: Hämta filversioner**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Funktionsbeskrivning**

 De**GetFileVersions** API låter användare hämta olika versioner av en specifik fil som lagras i Aspose.Cells-molnet. Denna funktion är avgörande för att upprätthålla dokumentintegritet och spåra ändringar över tid.

###  Begäranparametrarna för**GetFileVersions** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| väg| Sträng| Väg| Sökvägen till filen för vilken versioner ska hämtas.|
| lagringsnamn| Sträng| Fråga| Namnet på lagringsplatsen där filen finns.|

### **Svarsbeskrivning**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)tillhandahåller ett omfattande programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK effektiviserar utvecklingen genom att abstrahera komplexiteter på låg nivå, vilket gör att utvecklare kan fokusera på kärnfunktioner. Utforska[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells-webbtjänster över olika programmeringsspråk:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{< /tab >}}
{{< /tabs >}}
