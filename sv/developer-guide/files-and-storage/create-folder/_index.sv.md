---
title: Skapa mapp i Excel AP
second_title: Developer Guide for Aspose.Cell
linktitle: Skapa mapp
type: docs
url: /sv/create-folder/
keywords: Excel API, Create Folder, Office Cloud, REST API, Cloud Storage, Folder Management, Excel, Spreadsheet, PDF, CSV, JSON, Markdow
description: Lär dig hur du skapar en mapp i Excel API med hjälp av REST
weight: 100
kwords: Skapa mapp, Excel API, Office Moln, REST API, Molnlagring, Mapphantering, Matcha alla tomma celler i ett Excel-arbetsblad
---
## **Excel API: Skapa mapp**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Funktionsbeskrivning**

 De**skapamapp** API låter användare skapa en ny mapp i den angivna sökvägen inom molnlagringen för Excel API. Denna funktion är avgörande för att organisera filer och underhålla en strukturerad katalog.

###  Begäranparametrarna för**skapamapp** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|----------|--|------------------------|---------------------------------|
| väg| Sträng| Väg| Sökvägen där mappen ska skapas.|
| lagringsnamn| Sträng| Fråga| Namnet på den lagring som ska användas.|

### **Svarsbeskrivning**

```json
{
Void
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
