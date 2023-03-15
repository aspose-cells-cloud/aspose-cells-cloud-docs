---
title: Importieren Sie Daten mit der Verwendung von storag
second_title: Aspose.Cells Cloud Documen
linktitle: Importieren Sie Daten mit Speicher
type: docs
url: /de/import/with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/]
description: "Cells.Cloud API für Excel betreiben: Daten in Excel-Arbeitsblatt importieren"
weight: 10
---
Dieser REST API gibt `import data` in der Datei Excel an.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg||
| Ordner| Schnur| Anfrage||
| Speichername| Schnur| Anfrage| Speichername.|
| Daten importieren|| Körper||

**Die Parameter der Importdatenoptionen**sind darin beschrieben[der Referenzlink](/cells/de/import/#import-data-option-parameter).

 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.
 
Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
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
 
 
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

