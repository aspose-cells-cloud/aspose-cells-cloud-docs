---
title: Kopieren Sie den Bereich in ein Arbeitsblatt mit der Einfügeoption
second_title: Aspose.Cells Cloud Documen
linktitle: Polizist
type: docs
url: /de/ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: Copy a range in an Excel worksheet with paste options
description: Aspose.Cells Cloud REST API unterstützt das Kopieren eines Bereichs in einem Excel Arbeitsblatt mit Einfügeoptionen. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 20
---
Dieser REST API gibt an, dass der Bereich im Arbeitsblatt auf ein Excel-Arbeitsblatt kopiert werden soll.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Name der Arbeitsmappe|
| Tabellenname| Schnur| Weg| Arbeitsblattname|
| ReichweiteOperate|| Körper| copydata, copystyle, copyto, copyvalue|
| Ordner| Schnur| Anfrage| Arbeitsmappenordner.|
| Speichername| Schnur| Anfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRanges) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.
 
Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"Operate\": \"string\", \"Source\": { \"ColumnCount\": 0, \"ColumnWidth\": 0, \"FirstColumn\": 0, \"FirstRow\": 0, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 0, \"RowHeight\": 0, \"Worksheet\": \"string\" }, \"Target\": { \"ColumnCount\": 0, \"ColumnWidth\": 0, \"FirstColumn\": 0, \"FirstRow\": 0, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 0, \"RowHeight\": 0, \"Worksheet\": \"string\" }, \"PasteOptions\": { \"OnlyVisibleCells\": true, \"PasteType\": \"string\", \"SkipBlanks\": true, \"Transpose\": true }}"

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

```csharp

string Client_Id = "Use your Client_Id";

string Client_Secret = "Use your Client_Secret";

//Copy Range in a Worksheet with Paste Options - URL

string url = "http://api.aspose.cloud/v3.0/cells/sampleRangeCopyTo.xlsx/worksheets/Sheet1/ranges";

//JSON - Part of Request Body

string strJson = "{ \"Operate\": \"copyto\", \"Source\": { \"ColumnCount\": 5, \"ColumnWidth\": 8.43, \"FirstColumn\": 1, \"FirstRow\": 0, \"RowCount\": 7, \"RowHeight\": 15, }, \"Target\": { \"ColumnCount\": 5, \"ColumnWidth\": 8.43, \"FirstColumn\": 10, \"FirstRow\": 20, \"RowCount\": 7, \"RowHeight\": 15, } , \"PasteOptions\": { \"OnlyVisibleCells\": true, \"PasteType\": \"All\", \"SkipBlanks\": true, \"Transpose\": false } }";

//Sign the URL

string surl = Sign(url, Client_Id, Client_Secret);

//Process Command - Post Signed URL with JSON body

using (Stream stream = ProcessCommand(surl, "Post", strJson, "json"))

{

	//Your code

}

```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "4b9529b9d4238c301f3ee4855843874b" >}}

{{< /tab >}}

{{< /tabs >}}




