---
title: Flytta vik
second_title: Documen
linktitle: Flytta vik
type: docs
url: /sv/move-folder/
keywords: Move folder API, Excel API, Folder management, REST API, Aspose.Cells, Cloud storag
description: Den här dokumentationen ger en omfattande guide till hur man använder Flytta mapp API för att hantera mappar inom molnlagringen Aspose.Cells.
weight: 100
kwords: Excel API, Flytta mapp API, Office Moln, REST API, Kalkylbladshantering, PDF, CSV, JSON, Markdown, Matcha alla tomma celler i ett Excel-kalkylblad
---
## **Excel API: Flytta mapp**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Funktionsbeskrivning**

Denna API låter användare flytta en mapp från en plats till en annan inom Aspose.Cells-molnlagringen. Det är viktigt för att organisera filer och hantera molnlagring effektivt.

###  Begäranparametrarna för**flyttaMapp** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|----------------|--|------------------------|--------------------------------------------------------|
| srcPath| Sträng| Väg| Källsökvägen för mappen som ska flyttas.|
| destPath| Sträng| Fråga| Målsökvägen dit mappen ska flyttas.|
| srcLagringsnamn| Sträng| Fråga| Namnet på källlagringen.|
| destStorageName| Sträng| Fråga| Namnet på destinationslagringen.|

### **Svarsbeskrivning**

```json
{
Void
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
