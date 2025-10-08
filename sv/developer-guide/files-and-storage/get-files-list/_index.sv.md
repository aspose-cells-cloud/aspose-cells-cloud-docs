---
title: Hämta fillista - Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: Hämta filer List
type: docs
url: /sv/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: Lär dig hur du hämtar en lista med filer från en angiven mapp med hjälp av Aspose.Cells API. Den här guiden ger information om förfrågningsparametrar, svarsstruktur och kodexempel i olika programmeringsspråk.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Molnfilhantering, Hämta fillista
---
## **Excel API: Hämta fillista**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Funktionsbeskrivning**

 De**getFilesList**API låter användare hämta en omfattande lista över filer och mappar som finns i en specifik katalog i molnlagringen Aspose.Cells. Denna slutpunkt är avgörande för att hantera filer effektivt och stöder olika filformat.

###  Begäranparametrarna för**getFilesList** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| väg| Sträng| Väg| Sökvägen till mappen i molnlagringen från vilken fillistan ska hämtas.|
| lagringsnamn| Sträng| Fråga| Namnet på lagringsutrymmet som ska åtkommas.|

### **Svarsbeskrivning**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare, vilket underlättar enkel integration och testning.

## Excel API SDK

 Att använda ett SDK är det optimala sättet att påskynda din utvecklingsprocess. Ett SDK hanterar detaljer på låg nivå, så att du kan koncentrera dig på dina projektuppgifter. För en komplett lista över Aspose.Cells Cloud SDK:er, besök[GitHub-arkiv](https://github.com/aspose-cells-cloud).

Följande kodexempel illustrerar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}
