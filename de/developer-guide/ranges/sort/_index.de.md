---
title:  Bereichssortierung
second_title: Aspose.Cells Cloud Documen
linktitle: Herr
type: docs
keywords: Range Sort
url: /de/ranges/sort/
description:  Legt einen Umrissrahmen um einen Bereich von Zellen fest.
weight: 20
---
Dieser REST API gibt die Bereichssortierung an.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

 Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg|Der Name der Arbeitsmappe.|
|Blattname|Zeichenfolge|Weg|Der Arbeitsblattname.|
|rangeOperate|Klasse|Körper| Bereichssortierungsanfrage|
|Ordner|Zeichenfolge|Abfrage|Originaler Arbeitsmappenordner.|
|Speichername|Zeichenfolge|Abfrage|Speichername.|



 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht die Durchführung von REST-Interaktionen direkt über einen Webbrowser.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie man mit cURL Anrufe zur Cloud API tätigt.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
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

