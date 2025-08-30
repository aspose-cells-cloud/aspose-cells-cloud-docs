---
title: Holen Sie sich Cells Property
type: docs
url: /de/get-cells-properties/
weight: 130
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Get Cells Eigenschaften
---
Dieser REST API zeigt, wie `get a specific cell` in einer Excel-Datei verwendet wird.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Blattname| Schnur| Weg| Arbeitsblattname.|
| Zellen- oder Methodenname| Schnur| Weg|Der Name der Zelle oder Methode. (Wert des Methodennamens: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn und cellName.)|
| Ordner| Schnur| Abfrage| Ordner des Dokuments.|
| Speichername| Schnur| Abfrage| Speichername.|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

### **Cloud SDK-Familie**

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

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

### **So erhalten Sie eine bestimmte Zelle**

- [Abrufen von Zelldaten aus einem Arbeitsblatt](/cells/de/get-cell-data-from-a-worksheet/)
- [Holen Sie sich die erste Zelle aus dem Arbeitsblatt Excel](/cells/de/get-first-cell-from-excel-worksheet/)
- [Holen Sie sich die letzte Zelle des Arbeitsblatts Excel](/cells/de/get-last-cell-of-excel-worksheet/)
- [Holen Sie sich MaxRow aus dem Arbeitsblatt Excel](/cells/de/get-maxrow-from-excel-worksheet/)
- [Holen Sie sich MaxDataRow aus dem Arbeitsblatt Excel](/cells/de/get-maxdatarow-from-excel-worksheet/)
- [Holen Sie sich MaxColumn aus dem Arbeitsblatt Excel](/cells/de/get-maxcolumn-from-excel-worksheet/)
- [Holen Sie sich MaxDataColumn aus dem Arbeitsblatt Excel](/cells/de/get-maxdatacolumn-from-excel-worksheet/)
- [Holen Sie sich MinRow aus dem Arbeitsblatt Excel](/cells/de/get-minrow-from-excel-worksheet/)
- [Holen Sie sich MinDataRow aus dem Arbeitsblatt Excel](/cells/de/get-mindatarow-from-excel-worksheet/)
- [Holen Sie sich MinColumn aus dem Arbeitsblatt Excel](/cells/de/get-mincolumn-from-excel-worksheet/)
- [Holen Sie sich MinDataColumn aus dem Arbeitsblatt Excel](/cells/de/get-mindatacolumn-from-excel-worksheet/)
