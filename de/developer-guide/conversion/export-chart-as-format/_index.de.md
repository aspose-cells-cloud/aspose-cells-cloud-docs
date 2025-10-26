---
title: Aspose.Cells Cloud Web API - Exportieren eines Tabellenkalkulationsdiagramms als Formatdatei
second_title: Documen
ArticleTitle: Export a Spreadsheet Chart as a Format fil
linktitle: Diagramm als Forma exportieren
type: docs
url: /de/export-chart-as-format/
keywords: Export Chart, Aspose.Cells Cloud Web API, Spreadsheet Conversion, PDF Export, Image Export, REST, Excel, CSV, JSO
description: Konvertiert Diagramme aus in der Cloud gespeicherten Tabellen effizient in bestimmte Formate wie PDF oder direkt in Bilder, ohne sie herunterzuladen
weight: 100
kwords: Diagramm exportieren, REST, Tabellenkalkulationskonvertierung, PDF, CSV, JSON, Markdown, Excel, Bildformat
---
Exportieren Sie eine Cloud-Tabelle/ein Excel-Diagramm mit dem Aspose.Cells Cloud Web API in eine Datei in einem anderen Format.

## **Diagramm exportieren als Format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| (Erforderlich) Der Name der abzurufenden Arbeitsmappendatei.|
| Arbeitsblatt| Zeichenfolge| Weg| Arbeitsblattname|
| Diagrammindex| Ganze Zahl| Weg| Diagrammindex|
| Format| Zeichenfolge| Abfrage| (Erforderlich) Das gewünschte Ausgabeformat (z. B. „png“, „pdf“, „svg“).|
| Ordner| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist; der Standardwert ist null.|
| Speichername| Zeichenfolge| Abfrage|(Optional) Der Name des Speichers, wenn benutzerdefinierter Cloud-Speicher verwendet wird. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist; der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Name des Ausgabedateispeichers.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Verwenden Sie benutzerdefinierte Schriftarten.|
| Region| Zeichenfolge| Abfrage| Die Tabellenbereichseinstellung.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

### **Antwort**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Warum sollten Sie das Tabellenkalkulationsdiagramm im Format API exportieren?

- Sie können Cloud-Dateien jederzeit und überall in verschiedene Formate konvertieren.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich das Tabellenkalkulationsdiagramm im Format API mit SDKs?

### Diagramm als Format API Spezifikation exportieren

 Der[Diagramm als Format API Spezifikation exportieren](https://reference.aspose.cloud/cells/#/ConversionController/ExportChartAsFormat) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, Tabellendiagrammdaten mit einem kurzen Code in eine Formatdatei zu exportieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
