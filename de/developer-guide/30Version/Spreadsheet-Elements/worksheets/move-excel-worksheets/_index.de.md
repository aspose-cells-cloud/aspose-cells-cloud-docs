---
title: "Verschieben eines Excel-Arbeitsblatts – Aspose.Cells Cloud API (v3.0)"
second_title: "Dokument"
linktitle: "Verschieben"
type: docs
url: /de/worksheets/move/
aliases: [  /de/move-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, Arbeitsblatt verschieben, Excel, REST-API, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "Erfahren Sie, wie Sie ein Excel-Arbeitsblatt an eine neue Position verschieben können, mithilfe der Aspose.Cells Cloud API (v3.0). Enthält Endpunkt, erforderliche Parameter, cURL-Beispiel und SDK-Code in C#, Java, Python und mehr."
weight: 20
ArticleTitle: "So verschieben Sie ein Excel-Arbeitsblatt mit Aspose.Cells Cloud API v3.0"
---

Diese REST-API verschiebt ein Arbeitsblatt innerhalb einer Excel-Arbeitsmappe.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### Anforderungsparameter

| Parametername | Typ    | Ort    | Beschreibung                                                                                                           |
| ------------- | ------ | ------ | ---------------------------------------------------------------------------------------------------------------------- |
| name          | string | path   | Name der Excel-Datei.                                                                                                 |
| sheetName     | string | path   | Name des zu verschiebenden Arbeitsblatts.                                                                             |
| moving        | object | body   | JSON-Objekt, das das Zielarbeitsblatt (`DestinationWorksheet`) und die relative Position (`Position`) angibt.         |
| folder        | string | query  | Pfad des Ordners, in dem die Arbeitsmappe gespeichert ist.                                                            |
| storageName   | string | query  | Name des Speicherdiensts.                                                                                             |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste aufzurufen. Das folgende Beispiel zeigt, wie ein Arbeitsblatt mit einer einzigen Anforderung verschoben wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

**Beispiel für Fehlerantwort**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Erforderlicher Parameter 'moving' fehlt."
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}