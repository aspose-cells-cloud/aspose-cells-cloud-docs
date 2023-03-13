---
title: Fil herunterladen
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/file/download/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: Erfahren Sie, wie Sie Dateien mit Aspose Cells Cloud REST API SDK-Unterstützungsarten von Entwicklungssprachen herunterladen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 100
---
Dieser REST API zeigt `download file` an.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg| Dateipfad zB '/folder/file.ext'|
| Speichername| Schnur| Anfrage| Speichername|
| versionId| Schnur| Anfrage| Dateiversions-ID zum Herunterladen|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/DownloadFile) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.
 
Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash

{
    Stream
}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-Familie
 
 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
 
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
 
 
 
 

