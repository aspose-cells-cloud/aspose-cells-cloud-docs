---
title:  Slicer zum Einfügen von Listenobjekten
second_title: Aspose.Cells Cloud Documen
linktitle: Slice einfügen
type: docs
keywords: Insert slicer for list object
url: /de/list-objects/insert-slicer/
description:  Slicer für Listenobjekt einfügen.
weight: 20
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Slicer zum Einfügen von Listenobjekten
---
 Dieser REST API gibt an, dass in einem Excel-Arbeitsblatt ein Slicer für ein Listenobjekt eingefügt werden soll.

## RSET API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer

```

 Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg||
|Blattname|Zeichenfolge|Weg||
|Listenobjektindex|Ganze Zahl|Weg||
|SpaltenIndex|Ganze Zahl|Abfrage||
|Zielzellenname|Zeichenfolge|Abfrage||
|Ordner|Zeichenfolge|Abfrage||
|Speichername|Zeichenfolge|Abfrage||



 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectInsertSlicer) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

Mit dem Befehlszeilentool cURL können Sie ganz einfach auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Anrufe an Cloud API tätigen.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
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

Die Verwendung eines SDK ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im GitHub-Repository.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an die Webdienste Aspose.Cells tätigen:
