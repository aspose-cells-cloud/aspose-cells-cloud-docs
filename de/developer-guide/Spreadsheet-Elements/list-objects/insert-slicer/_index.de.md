---
title:  Slicer zum Einfügen von Listenobjekten
second_title: Aspose.Cells Cloud Documen
linktitle: Slice einfügen
type: docs
keywords: Insert slicer for list object
url: /de/list-objects/insert-slicer/
description:  Slicer für Listenobjekt einfügen.
weight: 20
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Slicer zum Einfügen von Listenobjekten
---
Dieser REST API gibt das Einfügen eines Slicers für ein Listenobjekt in ein Excel-Arbeitsblatt an.

## RSET API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer

```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg||
|Blattname|Zeichenfolge|Weg||
|listObjectIndex|Ganze Zahl|Weg||
|Spaltenindex|Ganze Zahl|Abfrage||
|Zielzellenname|Zeichenfolge|Abfrage||
|Ordner|Zeichenfolge|Abfrage||
|Speichername|Zeichenfolge|Abfrage||

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectInsertSlicer) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

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

Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um grundlegende Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im GitHub-Repository.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}

{{< /tab >}}

{{< /tabs >}}
