---
title: Datei verschieben
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/file/move/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: Erfahren Sie, wie Sie eine Datei mit Aspose Cells Cloud REST API SDK herunterladen, das verschiedene Entwicklungssprachen unterstützt. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 100
---
Dieser REST API gibt `move file` an
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| srcPath| Zeichenfolge| Weg| Quelldateipfad, z. B. „/src.ext“|
| destPath| Zeichenfolge| Abfrage| Zieldateipfad, z. B. „/dest.ext“|
| srcStorageName| Zeichenfolge| Abfrage| Name des Quellspeichers|
| destStorageName| Zeichenfolge| Abfrage| Name des Zielspeichers|
| versionId| Zeichenfolge| Abfrage| Zu verschiebende Dateiversions-ID|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/MoveFile) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht die Durchführung von REST-Interaktionen direkt über einen Webbrowser.
 
Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie man mit cURL Anrufe zur Cloud API tätigt.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
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
 
 Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte schauen Sie sich die an[GitHub-Repository](https://github.com/aspose-cells-cloud) Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie hier.
 
Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
 
 