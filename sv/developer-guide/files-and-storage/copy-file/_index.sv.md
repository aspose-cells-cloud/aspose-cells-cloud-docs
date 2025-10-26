---
title: Kopiera fil - Excel AP
second_title: Documen
linktitle: Kopiera fil
type: docs
url: /sv/copy-file/
keywords: Excel API, Office Cloud, REST API, Spreadsheet Copy, PDF Conversion, CSV Export, JSON Handling, Markdown Support, Copy Excel File, Match Blank Cell
description: Lär dig hur du använder CopyFile API för Excel för att effektivt duplicera kalkylblad och hantera olika filformat.
weight: 100
kwords: Excel API, Office Moln, REST API, Kalkylbladskopia, PDF Konvertering, CSV-export, JSON-hantering, Markdown-stöd, Kopiera Excel-fil, Matcha tomma celler
---
## **Excel API: Kopiera fil**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Funktionsbeskrivning**

 De**kopieraFil** API låter användare duplicera en Excel-fil från en angiven källsökväg till en destinationssökväg, vilket stöder olika lagringsalternativ.

###  Begäranparametrarna för**kopieraFil** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|-------------- ||--------------------- |-------------------------------------- |
| srcPath| Sträng| Väg| Källsökvägen för filen som ska kopieras.|
| destPath| Sträng| Fråga| Målsökvägen där filen ska sparas.|
| srcLagringsnamn| Sträng| Fråga| Namnet på källlagringen.|
| destStorageName| Sträng| Fråga| Namnet på destinationslagringen.|
| versions-ID| Sträng| Fråga| Valfritt versions-ID för filen som ska kopieras.|

### **Svarsbeskrivning**

```json
{
Void
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/FileController/CopyFile) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på låg nivå, vilket gör att du kan fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
