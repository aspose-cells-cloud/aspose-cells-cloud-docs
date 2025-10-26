---
title: Aspose.Cells Cloud Web API - Exportieren einer Kalkulationstabelle als Formatdatei
second_title: Documen
ArticleTitle: Export a Spreadsheet as a Format fil
linktitle: Tabellenkalkulation als Forma exportieren
type: docs
url: /de/export-spreadsheet-as-format/
keywords: Export spreadsheet, Aspose.Cells Cloud Web API, Convert spreadsheet, Spreadsheet formats, XLSX, PDF, CSV, JSON, Markdow
description: Konvertiert effizient im Cloud-Speicher gespeicherte Tabellenkalkulationen in verschiedene Formate wie XLSX, PDF und CSV
weight: 100
kwords: Excel, Office Cloud, REST, Tabellenkalkulationskonvertierung, PDF, CSV, JSON, Markdow
---
Exportieren Sie eine Cloud-Tabelle/Excel in eine Datei mit einem anderen Format.

## **Tabellenkalkulation als Format API exportieren**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| (Erforderlich) Der Name der abzurufenden Arbeitsmappendatei.|
| Format| Zeichenfolge| Abfrage| (Erforderlich) Das gewünschte Ausgabeformat (z. B. „Xlsx“, „Pdf“, „Csv“).|
| Ordner| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
| Speichername| Zeichenfolge| Abfrage|(Optional) Der Name des Speichers, wenn benutzerdefinierter Cloud-Speicher verwendet wird. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert wird. Der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Speichername der Ausgabedatei.|
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

## Warum sollten Sie die Exporttabelle im Format API verwenden?

- Sie können Cloud-Dateien jederzeit und überall in verschiedene Formate konvertieren.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Exporttabelle im Format API mit SDKs?

### Tabellenkalkulation als Format API Spezifikation exportieren

 Der[Tabellenkalkulation als Format API Spezifikation exportieren](https://reference.aspose.cloud/cells/#/ConversionController/ExportSpreadsheetAsFormat) bietet eine öffentlich zugängliche Programmierschnittstelle zur nahtlosen Durchführung von REST-Interaktionen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, eine Tabelle mit kurzem Code in eine Formatdatei zu exportieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen die Interaktion mit Aspose.Cells Webdiensten via verschiedenen SDKs:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
