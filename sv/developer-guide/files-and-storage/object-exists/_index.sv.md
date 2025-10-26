---
title: Objekt finns
second_title: Documen
linktitle: Objekt finns
type: docs
url: /sv/object-exists/
keywords: Excel API, Object Exists, REST API, Aspose, File Management, Excel, Office Cloud, Spreadsheet, PDF, CSV, JSON, Markdow
description: Objektet finns API kontrollerar om en specifik fil eller mapp finns i molnlagringen Aspose.Cells
weight: 100
kwords: Excel API, Objektet finns, REST API, Aspose, Office Moln, Filhantering, Kalkylblad, PDF, CSV, JSON, Markdown, Kontrollera filens existens i Excel
---
## **Excel API: Objektet finns**

```
GET http://api.aspose.cloud/v4.0/cells/storage/exist/{path}
```

### **Funktionsbeskrivning**

`objectExists` API låter utvecklare verifiera förekomsten av en specifik fil eller mapp i molnlagringen Aspose.Cells.

###  Begäranparametrarna för**objektExisterar** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
|väg|Sträng|Väg|Sökvägen till filen eller mappen i molnlagringen.|
|lagringsnamn|Sträng|Fråga|Namnet på lagringsplatsen där filen finns.|
|versions-ID|Sträng|Fråga|Filens versions-ID (om tillämpligt).|

### **Svarsbeskrivning**

```json
{
  "Name": "ObjectExist",
  "Description": [
    "Object exists"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates that the file or folder exists."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    },
    {
      "Name": "IsFolder",
      "Description": [
        "True if it is a folder, false if it is a file."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ObjectExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ObjectExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ObjectExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ObjectExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ObjectExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ObjectExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ObjectExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ObjectExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
