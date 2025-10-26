---
title: Aspose.Cells Cloud Web API - Exportieren eines Tabellenkalkulations-Arbeitsblatts als Formatdatei
second_title: Documen
ArticleTitle: Export a Spreadsheet Worksheet as a Format fil
linktitle: Arbeitsblatt exportieren
type: docs
url: /de/export-worksheet-as-format/
keywords: Export worksheet, Cloud storage conversion, File format transformation, API for spreadsheet
description: Konvertiert effizient ein Arbeitsblatt aus dem Cloud-Speicher in verschiedene Formate wie PDF, CSV und Bilder
weight: 100
kwords: Arbeitsblatt exportieren, Cloud-Konvertierung, PDF, Bildformate, Excel, REST API, CSV, JSON, Markdown, Leere Zellen in Exce verarbeiten
---
Exportieren Sie eine Cloud-Tabelle/ein Excel-Arbeitsblatt mit dem Aspose.Cells Cloud Web API in eine Datei in einem anderen Format.

## **Arbeitsblatt exportieren als Format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg|(Erforderlich) Der Name der abzurufenden Arbeitsmappendatei.|
|Arbeitsblatt|Zeichenfolge|Weg|(Erforderlich) Das zu konvertierende Arbeitsblatt.|
|Format|Zeichenfolge|Abfrage|(Erforderlich) Das gewünschte Ausgabeformat (z. B. „png“, „pdf“, „svg“).|
|Ordner|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|Speichername|Zeichenfolge|Abfrage|(Optional) Der Name des benutzerdefinierten Cloud-Speichers. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Pfad zum Ausgabeordner. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|(Optional) Speichername der Ausgabedatei.|
|SchriftartenStandort|Zeichenfolge|Abfrage|(Optional) Geben Sie bei Bedarf benutzerdefinierte Schriftarten an.|
|Region|Zeichenfolge|Abfrage|Die Tabellenbereichseinstellung.|
|Passwort|Zeichenfolge|Abfrage|Das Kennwort für den Zugriff auf die Tabellenkalkulationsdatei.|

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

## Warum sollten Sie das Arbeitsblatt „Tabellenkalkulation exportieren“ im Format API verwenden?

- Sie können Cloud-Dateien jederzeit und überall in verschiedene Formate konvertieren.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich das Arbeitsblatt „Tabellenkalkulation exportieren“ im Format API mit SDKs?

### Arbeitsblatt als Format API-Spezifikation exportieren

 Der[Arbeitsblatt als Format API Spezifikation exportieren](https://reference.aspose.cloud/cells/#/ConversionController/ExportWorksheetAsFormat) bietet eine öffentlich zugängliche Programmierschnittstelle zum Ausführen von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, ein Tabellenkalkulationsblatt mit kurzem Code in eine Formatdatei zu exportieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
