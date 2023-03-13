---
title: Automatisches Anpassen einer Spalte auf einem Excel-Arbeitsblatt
second_title: Aspose.Cells Cloud Documen
linktitle: Spalte
type: docs
url: /de/worksheets/autofit/column/
aliases: [/autofit-single-column-of-worksheet/]
keywords: Autofit a column on an Excel workshee
description: Aspose.Cells Cloud REST API unterstützt die automatische Anpassung einer Spalte auf einem Excel Arbeitsblatt. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 10
---
Dieser REST API gibt an, dass eine Spalte auf einem Excel-Arbeitsblatt automatisch angepasst werden soll.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg||
| Tabellenname| Schnur| Weg||
| erste Spalte| ganze Zahl| Anfrage||
| letzteSpalte| ganze Zahl| Anfrage||
| autoFitterOptions|| Körper||
| erste Reihe| ganze Zahl| Anfrage||
| letzte Reihe| ganze Zahl| Anfrage||
| Ordner| Schnur| Anfrage||
| Speichername| Schnur| Anfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.
 
Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=2&firstColumn=2" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells" : true, "IgnoreHidden" : true, "OnlyAuto" : true}' 

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


{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "9b4ccf2e3ba7d0f1d2a625d6cd40d2fd" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "3f17376a8d99f16f703fdb52c08a05ff" >}}

{{< /tab >}}

{{< /tabs >}}




