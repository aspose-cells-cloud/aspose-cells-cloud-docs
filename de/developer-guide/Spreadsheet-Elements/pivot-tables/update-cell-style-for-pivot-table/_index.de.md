---
title: Aktualisieren Sie den Zellenstil für die Pivot-Tabelle
second_title: Aspose.Cells Cloud Documen
linktitle: Format
type: docs
url: /de/pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: Update cell style for a pivot table
description: Aspose.Cells Cloud REST API unterstützt die Aktualisierung des Zellenstils für eine Pivot-Tabelle. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift.
weight: 90
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Zellenstil für Pivot-Tabelle aktualisieren
---
Dieser REST API gibt die Aktualisierungszelle `style` für die Pivot-Tabelle an.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Blattname| Schnur| Weg| Der Arbeitsblattname.|
| PivotTableIndex| ganze Zahl| Weg| Pivot-Tabellenindex|
| Spalte| ganze Zahl| Abfrage||
| Reihe| ganze Zahl| Abfrage||
| Stil|| Körper| Stil dto im Anforderungstext.|
| needReCalculate| Boolescher Wert| Abfrage|FALSCH|
| Ordner| Schnur| Abfrage| Ordner des Dokuments.|
| Speichername| Schnur| Abfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.
 
Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
-X POST \
-d '{"Font":{"Name":"Arial", "Size":10}}'  \
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
 
 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um grundlegende Details und ermöglicht Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
 
Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
 
 
 
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}




