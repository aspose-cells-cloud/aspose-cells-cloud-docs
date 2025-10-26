---
title: Aspose.Cells Cloud Web API - Teilen Sie eine Tabelle in mehrere Dateien auf, eine für jedes Arbeitsblatt
second_title: Documen
ArticleTitle: Split a spreadsheet into multiple files, one for each worksheet
linktitle: Remote-Tabelle in Clou teilen
type: docs
url: /de/split-remote-spreadsheet/
keywords: spreadsheet splitting, cloud spreadsheet API, split Excel file, multi-format outpu
description: Teilen Sie eine im Cloud-Speicher gespeicherte Tabelle ohne Download in mehrere Ausgabeformate auf
weight: 100
kwords: Excel, Office Cloud, REST, Tabellenkalkulation, PDF, CSV, JSON, Markdown, geteilte Remote-Tabelle
---
Teilen Sie die in der Cloud gespeicherte Tabelle in separate Dateien mit 30 Ausgabedateiformaten auf.

## **Geteilte Remote-Tabelle API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| Der Name der zu teilenden Arbeitsmappendatei.|
| Ordner| Zeichenfolge| Abfrage| Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist.|
| aus| Ganze Zahl| Abfrage| Beginnen Sie mit dem Arbeitsblattindex.|
| Zu| Ganze Zahl| Abfrage| Ende des Arbeitsblattindex.|
| Ausgabeformat| Zeichenfolge| Abfrage| Das gewünschte Ausgabeformat (z. B. „Xlsx“, „Pdf“, „Csv“).|
| Speichername| Zeichenfolge| Abfrage|(Optional) Der Name des Speichers, wenn benutzerdefinierter Cloud-Speicher verwendet wird. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Name des Ausgabedateispeichers.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Verwenden Sie benutzerdefinierte Schriftarten.|
| Region| Zeichenfolge| Abfrage| Die Tabellenbereichseinstellung.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

## **Antwort**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Wo sollten wir die Split Remote-Tabelle API verwenden?

Wenn Sie mehrere Datendateien zusammenführen müssen, können Sie diese API verwenden.

## Warum sollten Sie die Split Remote-Tabelle API verwenden?

- Cloud-Speicherdateien müssen nicht heruntergeladen werden und können direkt in der Cloud aufgeteilt werden.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Split Remote-Tabelle API mit SDKs

### Split Remote Spreadsheet API Spezifikation

 Der[Split Remote Spreadsheet API Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, die in der Cloud gespeicherte Tabelle mit kurzem Code in separate Dateien aufzuteilen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{< /tab >}}
{{< /tabs >}}
