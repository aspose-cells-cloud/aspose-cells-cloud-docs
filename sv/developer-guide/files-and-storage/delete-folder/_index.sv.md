---
title: Ta bort mapp
second_title: Documen
linktitle: Ta bort mapp
type: docs
url: /sv/delete-folder/
keywords: Delete folder, Aspose.Cells API, RESTful API, Excel file management, cloud storag
description: Lär dig hur du tar bort en mapp i Aspose.Cells med hjälp av deleteFolder API, inklusive parametrar och kodexempel.
weight: 100
kwords: Excel API, Office Moln, REST API, Kalkylbladshantering, PDF, CSV, JSON, Markdown, ta bort mapp i Excel-kalkylblad
---
## **Excel API: Ta bort mapp**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Funktionsbeskrivning**

`deleteFolder` API låter användare ta bort en specifik mapp från molnlagringen som är kopplad till Aspose.Cells. Detta kan vara användbart för att upprätthålla organiseringen och hantera lagring effektivt.

###  Begäranparametrarna för**ta bort mapp** API är

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| väg| Sträng| Väg| Sökvägen till mappen som ska raderas.|
| lagringsnamn| Sträng| Fråga| Namnet på lagringsplatsen där mappen finns.|
| rekursiv| Booleansk| Fråga| Anger om borttagningen ska vara rekursiv, vilket även tar bort allt innehåll i mappen.|

### **Svarsbeskrivning**

```json
{
Void
}
```

## OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på låg nivå, vilket gör att du kan fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
