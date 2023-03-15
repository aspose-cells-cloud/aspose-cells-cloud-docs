---
title: Rufen Sie ein Listenobjekt in einem Excel-Arbeitsblatt ab
second_title: Aspose.Cells Cloud Documen
linktitle: Ge
type: docs
url: /de/list-objects/get/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/get/]
keywords: Get a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API unterstützt das Abrufen eines Listenobjekts (einer Tabelle) in ein Excel-Arbeitsblatt. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 9
---
Dieser REST API zeigt `get` eine Liste von Objektinformationen nach Index an oder konvertiert eine `list object`-Datei in ein anderes Format in einem Excel-Arbeitsblatt.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Tabellenname| Schnur| Weg| Der Arbeitsblattname.|
| Listenobjektindex| ganze Zahl| Weg| Objektindex auflisten.|
| Format| Schnur| Anfrage| Exportformat.|
| Ordner| Schnur| Anfrage| Ordner des Dokuments.|
| Speichername| Schnur| Anfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.
 
Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
	"ListObject": {
		"AutoFilter": {
			"FilterColumns": [],
			"Range": "B2:F11",
			"Sorter": {
				"CaseSensitive": false,
				"HasHeaders": false,
				"KeyList": [],
				"SortLeftToRight": false
			}
		},
		"DisplayName": "Table3",
		"StartColumn": 1,
		"StartRow": 1,
		"EndColumn": 5,
		"EndRow": 10,
		"ListColumns": [{
			"Name": "Column1",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 1,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$B$2:$B$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column2",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 2,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$C$2:$C$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column3",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 3,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$D$2:$D$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column4",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 4,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$E$2:$E$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column5",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 5,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$F$2:$F$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}],
		"ShowHeaderRow": true,
		"ShowTableStyleColumnStripes": false,
		"ShowTableStyleFirstColumn": false,
		"ShowTableStyleLastColumn": false,
		"ShowTableStyleRowStripes": true,
		"ShowTotals": false,
		"TableStyleName": "None",
		"TableStyleType": "None",
		"link": {
			"Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
			"Rel": "self"
		}
	},
	"Code": 200,
	"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-Familie
 
 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
 
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
 
Dieser REST API erhält ein Excel `listobject`-Objekt in eine andere Formatdatei.


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< /tabs >}}
