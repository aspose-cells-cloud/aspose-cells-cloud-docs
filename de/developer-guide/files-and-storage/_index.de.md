---
title: Dateien und Speicher
second_title: Documen
type: docs
url: /de/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: Umfassende Anleitung zur Verwendung der Aspose Cells Cloud für Dateispeichervorgänge, einschließlich Hochladen, Herunterladen und Verwalten von Dateien. SDK-Unterstützung für verschiedene Programmiersprachen wie Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 100
kwords: Aspose Cells, Cloud-Speicher, REST API, Dateiverwaltung, Excel, PDF, CSV, JSON, Markdow
---
 Aspose.Cells Cloud bietet umfassende Hilfsfunktionen für die Arbeit mit Dateien, die in Aspose.Cells Cloud Storage oder einen anderen Cloud-Speicher Ihrer Wahl hochgeladen wurden. Hilfe bei der Einrichtung von Drittanbieter-Speicher finden Sie unter[Aspose Cloud UI-Hilfethemen](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud bietet eine Reihe von APIs für Datei-, Ordner- und Speichervorgänge.**

## **So laden Sie eine Datei hoch**

### Datei hochladen API Informationen

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg|Pfad zur hochzuladenden Datei, einschließlich Dateiname und Erweiterung (z. B. /file.ext oder /Ordner 1/file.ext). Wenn der Inhalt mehrteilig ist und der Pfad den Dateinamen nicht enthält, wird versucht, ihn aus dem Dateinamenparameter im Content-Disposition-Header abzurufen.|
| Datei| Datei| formData| Hochzuladende Datei|
| Speichername| Schnur| Abfrage| Speichername|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/UploadFile) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel für das Hochladen einer Datei

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}

## **So laden Sie eine Datei herunter**

### Datei API herunterladen Informationen

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg| Dateipfad (z. B. „/Ordner/Datei.ext“)|
| Speichername| Schnur| Abfrage| Speichername|
| Versions-ID| Schnur| Abfrage| ID der herunterzuladenden Dateiversion|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/DownloadFile) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispieldatei herunterladen

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="13" tabName13="Request" tabName14="Response" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```bash
{
    Stream
}
```

{{< /tab >}}
{{< /tabs >}}

## **So löschen Sie eine Datei**

### Informationen zum Löschen der Datei API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg| Dateipfad (z. B. „/Ordner/Datei.ext“)|
| Speichername| Schnur| Abfrage| Speichername|
| Versions-ID| Schnur| Abfrage| Zu löschende Dateiversions-ID|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/DeleteFile) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="15" tabName15="Request" tabName16="Response" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/book12.xlsx" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **So kopieren Sie eine Datei**

### Informationen zur Datei API kopieren

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Quellpfad| Schnur| Weg| Quelldateipfad (z. B. „/Ordner/Datei.ext“)|
|Zielpfad| Schnur| Abfrage| Zieldateipfad|
| srcStorageName| Schnur| Abfrage| Name des Quellspeichers|
| Zielspeichername| Schnur| Abfrage| Zielspeichername|
| Versions-ID| Schnur| Abfrage| Zu kopierende Dateiversions-ID|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/CopyFile) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel zum Kopieren einer Datei

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName18="Response" >}}

{{< tab tabNum="17" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **So verschieben Sie eine Datei**

### Informationen zur Datei API verschieben

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Quellpfad| Schnur| Weg| Quelldateipfad (z. B. „/src.ext“)|
|Zielpfad| Schnur| Abfrage| Zieldateipfad (z. B. „/dest.ext“)|
| srcStorageName| Schnur| Abfrage| Name des Quellspeichers|
| Zielspeichername| Schnur| Abfrage| Zielspeichername|
| Versions-ID| Schnur| Abfrage| Zu verschiebende Dateiversions-ID|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/MoveFile) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel zum Verschieben einer Datei

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

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

## **So erstellen Sie einen Ordner**

### Ordner erstellen API Informationen

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg|Zu erstellender Ordnerpfad (z. B. „Ordner_1/Ordner_2/') |
| Speichername| Schnur| Abfrage| Speichername|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel zum Erstellen eines Ordners

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="3" tabName3="Request" tabName4="Response" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **So erhalten Sie Dateien in einem Ordner**

### Informationen zu Dateien API abrufen

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg| Ordnerpfad (z. B. „/Ordner“)|
| Speichername| Schnur| Abfrage| Speichername|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel zum Abrufen von Dateien

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="5" tabName5="Request" tabName6="Response" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **So löschen Sie einen Ordner**

### Ordner löschen API Informationen

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg| Ordnerpfad (z. B. „/Ordner“)|
| Speichername| Schnur| Abfrage| Speichername|
| rekursiv| Boolescher Wert| Abfrage|FALSCH|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel zum Löschen eines Ordners

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="7" tabName7="Request" tabName8="Response" >}}

{{< tab tabNum="7" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **So kopieren Sie einen Ordner**

### Ordner kopieren API Informationen

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Quellpfad| Schnur| Weg| Quellordnerpfad (z. B. „/src“)|
|Zielpfad| Schnur| Abfrage| Zielordnerpfad (z. B. „/dst“)|
| srcStorageName| Schnur| Abfrage| Name des Quellspeichers|
| Zielspeichername| Schnur| Abfrage| Zielspeichername|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel zum Kopieren eines Ordners

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="21" tabName21="Request" tabName22="Response" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **So verschieben Sie einen Ordner**

### Ordner verschieben API Informationen

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Quellpfad| Schnur| Weg| Zu verschiebender Ordnerpfad (z. B. „/Ordner“)|
|Zielpfad| Schnur| Abfrage| Zielordnerpfad zum Verschieben (z. B. „/dst“)|
| srcStorageName| Schnur| Abfrage| Name des Quellspeichers|
| Zielspeichername| Schnur| Abfrage| Zielspeichername|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel für das Verschieben von Ordnern

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="23" tabName23="Request" tabName24="Response" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="24" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **So prüfen Sie, ob Speicher vorhanden ist**

### Speicher vorhanden API Informationen

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Speichername| Schnur| Weg| Speichername|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel für „Speicher vorhanden“

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="33" tabName33="Request" tabName34="Response" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```bash
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **So prüfen Sie, ob eine Datei oder ein Ordner vorhanden ist**

### Objekt vorhanden API Informationen

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg| Datei- oder Ordnerpfad (z. B. „/file.ext“ oder „/folder“)|
| Speichername| Schnur| Abfrage| Speichername|
| Versions-ID| Schnur| Abfrage| Dateiversions-ID|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel für „Objekt vorhanden“

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="37" tabName37="Request" tabName38="Response" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```bash
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **So ermitteln Sie die Festplattennutzung**

### Informationen zur Datenträgernutzung API abrufen

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Speichername| Schnur| Abfrage| Speichername|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel für die Datenträgernutzung abrufen

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="40" tabName40="Request" tabName41="Response" >}}

{{< tab tabNum="40" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
```

{{< /tab >}}
{{< /tabs >}}

## **So erhalten Sie Dateiversionen**

### Informationen zu Dateiversionen API abrufen

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Weg| Schnur| Weg| Dateipfad (z. B. „/file.ext“)|
| Speichername| Schnur| Abfrage| Speichername|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Beispiel zum Abrufen von Dateiversionen

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="46" tabName46="Request" tabName47="Response" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="47" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}
