﻿---
title: Pivot-Feld in Pivot-Tabelle hinzufügen
second_title: Aspose.Cells Cloud Documen
linktitle: Pivot-Feld hinzufügen
type: docs
url: /de/pivot-tables/add-pivot-field/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: Add a pivot field in a pivot table
description: Aspose.Cells Cloud REST API unterstützt das Hinzufügen eines Pivot-Felds in einer Pivot-Tabelle. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 40
---
Dieser REST API gibt das Pivot-Feld `add` in die Pivot-Tabelle an
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Tabellenname| Schnur| Weg| Der Arbeitsblattname.|
| PivotTableIndex| ganze Zahl| Weg| Index der Pivot-Tabelle|
| PivotFieldType| Schnur| Anfrage| Der Feldbereichstyp.|
| Anfrage|| Körper| Dto, das Feldindizes enthält|
| NeedReCalculate| boolesch| Anfrage| FALSCH|
| Ordner| Schnur| Anfrage| Ordner des Dokuments.|
| Speichername| Schnur| Anfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.
 
Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row"  \
-X PUT \
-d '{"Data":[1,2]}'
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
 
 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
 
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
 
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}




