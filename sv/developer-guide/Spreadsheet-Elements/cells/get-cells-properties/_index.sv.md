---
title: Skaffa fastigheten Cells
type: docs
url: /sv/get-cells-properties/
weight: 130
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Hämta Cells Egenskaper
---
Denna REST API visar hur man gör `get a specific cell` i en Excel-fil.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokumentnamn.|
| arknamn| sträng| väg| Arbetsbladets namn.|
| cellEllerMetodnamn| sträng| väg|Cellens eller metodens namn. (Metodnamnsvärde: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn och cellName.)|
| mapp| sträng| fråga| Dokumentets mapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### **Cloud SDK-familjen**

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### **Hur man får tag på en specifik cell**

- [Hämta celldata från ett kalkylblad](/cells/sv/get-cell-data-from-a-worksheet/)
- [Hämta första cellen från arbetsbladet Excel](/cells/sv/get-first-cell-from-excel-worksheet/)
- [Hämta sista cellen i arbetsbladet Excel](/cells/sv/get-last-cell-of-excel-worksheet/)
- [Hämta MaxRow från arbetsbladet Excel](/cells/sv/get-maxrow-from-excel-worksheet/)
- [Hämta MaxDataRow från arbetsbladet Excel](/cells/sv/get-maxdatarow-from-excel-worksheet/)
- [Hämta MaxColumn från arbetsbladet Excel](/cells/sv/get-maxcolumn-from-excel-worksheet/)
- [Hämta MaxDataColumn från arbetsbladet Excel](/cells/sv/get-maxdatacolumn-from-excel-worksheet/)
- [Hämta MinRow från arbetsbladet Excel](/cells/sv/get-minrow-from-excel-worksheet/)
- [Hämta MinDataRow från arbetsbladet Excel](/cells/sv/get-mindatarow-from-excel-worksheet/)
- [Hämta MinColumn från arbetsbladet Excel](/cells/sv/get-mincolumn-from-excel-worksheet/)
- [Hämta MinDataColumn från arbetsbladet Excel](/cells/sv/get-mindatacolumn-from-excel-worksheet/)
