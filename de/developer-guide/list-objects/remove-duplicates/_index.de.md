---
title:  Listenobjekt entfernt Duplikate
description:  Entfernen Sie Duplikate im Listenobjekt.
url: /de/list-objects/remove-duplicates/
weight: 20
---
 Dieser REST API gibt an, Duplikate für das Listenobjekt zu entfernen.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates

```

 Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg||
|Blattname|Zeichenfolge|Weg||
|listObjectIndex|Ganze Zahl|Weg||
|Ordner|Zeichenfolge|Abfrage||
|Speichername|Zeichenfolge|Abfrage||



 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectRemoveDuplicates) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht die Durchführung von REST-Interaktionen direkt über einen Webbrowser.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie man mit cURL Anrufe zur Cloud API tätigt.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im GitHub-Repository.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
