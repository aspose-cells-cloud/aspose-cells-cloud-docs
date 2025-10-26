---
title: Fügen Sie eine Pivot-Tabelle in ein Excel-Arbeitsblatt ein
second_title: Documen
linktitle: Hinzufügen
type: docs
url: /de/pivot-tables/add/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: Add a pivot table in an Excel worksheet
description: Aspose.Cells Cloud REST API unterstützt das Hinzufügen einer Pivot-Tabelle in einem Excel Arbeitsblatt. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Hinzufügen einer Pivot-Tabelle in einem Excel-Arbeitsblatt
---
Dieser REST API zeigt `add` eine Pivot-Tabelle im Arbeitsblatt an.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Blattname| Schnur| Weg| Der Arbeitsblattname.|
| Anfrage|| Körper| CreatePivotTableRequest dto im Anforderungstext.|
| Ordner| Schnur| Abfrage| Ordner des Dokuments.|
| Speichername| Schnur| Abfrage| Speichername.|
| Quelldaten| Schnur| Abfrage| Die Daten für den neuen PivotTable-Cache.|
|Zielzellenname| Schnur| Abfrage| Die Zelle in der oberen linken Ecke des Zielbereichs des PivotTable-Berichts.|
| Tabellenname| Schnur| Abfrage| Der Name des neuen PivotTable-Berichts.|
| useSameSource| Boolescher Wert| Abfrage| Gibt an, ob dieselbe Datenquelle verwendet wird, wenn eine andere vorhandene PivotTable diese Datenquelle bereits verwendet hat. Wenn die Eigenschaft „true“ ist, wird Speicherplatz gespart.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.
 
Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an Cloud API tätigen.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v  "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables"
-X PUT \
-d '{"Name":"MyPivot", "SourceData":"A5:E10", "DestCellName":"H20", "UseSameSource":true, "PivotFieldRows":[1], "PivotFieldColumns":[1], "PivotFieldData ":[1]}'\
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-Familie
 
 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
 
Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}
