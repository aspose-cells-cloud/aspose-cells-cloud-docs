---
title: Aktualisieren Sie ein Listenobjekt in einem Arbeitsblatt Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Update
type: docs
url: /de/list-objects/update/
aliases: [/update-a-list-object-or-table-inside-the-worksheet/,/tables/update/]
keywords: Update a list object(table) in an Excel worksheet
description: Aspose.Cells Cloud REST API unterstützt das Aktualisieren eines Listenobjekts (einer Tabelle) in einem Excel Arbeitsblatt. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 20
---
Dieser REST API weist auf `update` und `list object` Eigenschaften hin.

 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| Dokumentname.|
| Blattname| Zeichenfolge| Weg| Der Arbeitsblattname.|
| listObjectIndex| ganze Zahl| Weg| Objektindex auflisten|
| listObject|| Körper| listObject dto im Anfragetext.|
| Ordner| Zeichenfolge| Abfrage| Ordner des Dokuments.|
| Speichername| Zeichenfolge| Abfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht die Durchführung von REST-Interaktionen direkt über einen Webbrowser.
 
Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie man mit cURL Anrufe zur Cloud API tätigt.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
-X POST \
-d "{ \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"AutoFilter\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"FilterColumns\": [ { \"FieldIndex\": 0, \"FilterType\": \"string\", \"MultipleFilters\": { \"MatchBlank\": true, \"MultipleFilterList\": [ {} ] }, \"ColorFilter\": { \"FilterByFillColor\": \"string\", \"Pattern\": \"string\", \"Color\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" }, \"ForegroundColorColor\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" }, \"BackgroundColor\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" } }, \"CustomFilters\": [ { \"FilterOperatorType\": \"string\" } ], \"DynamicFilter\": { \"DynamicFilterType\": \"string\" }, \"IconFilter\": { \"IconId\": 0, \"IconSetType\": \"string\" }, \"Top10Filter\": { \"Criteria\": \"string\", \"IsPercent\": true, \"IsTop\": true, \"Items\": 0 }, \"Visibledropdown\": \"string\" } ], \"Range\": \"string\", \"Sorter\": { \"CaseSensitive\": true, \"HasHeaders\": true, \"KeyList\": [ { \"Key\": 0, \"SortOrder\": \"string\", \"CustomList\": \"string\" } ], \"SortLeftToRight\": true } }, \"DisplayName\": \"string\", \"StartColumn\": 0, \"StartRow\": 0, \"EndColumn\": 0, \"EndRow\": 0, \"ListColumns\": [ { \"Name\": \"string\", \"TotalsCalculation\": \"string\" } ], \"ShowHeaderRow\": true, \"ShowTableStyleColumnStripes\": true, \"ShowTableStyleFirstColumn\": true, \"ShowTableStyleLastColumn\": true, \"ShowTableStyleRowStripes\": true, \"ShowTotals\": true, \"TableStyleName\": \"string\", \"TableStyleType\": \"string\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-Familie
 
 Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte schauen Sie sich die an[GitHub-Repository](https://github.com/aspose-cells-cloud) Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie hier.
 
Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
 
 
 

{{< tabs tabTotal="4" tabID="4" tabName1="C#" tabName2="VB.NET" tabName3="Java" tabName4="Go" >}}

{{< tab tabNum="1" >}}

```java



```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java



```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java



```

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c76d8684f0bb9a96cb74f64433a43b88" >}}

{{< /tab >}}

{{< /tabs >}}
