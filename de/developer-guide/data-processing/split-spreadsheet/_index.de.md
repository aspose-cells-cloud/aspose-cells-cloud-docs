---
title: Aspose.Cells Cloud WEb API - Teilen Sie die Tabelle in separate Dateien auf
second_title: Documen
ArticleTitle: Split the Spreadsheet into separate files
linktitle: Tabellenkalkulation teilen
type: docs
url: /de/split-spreadsheet/
keywords: Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdow
description: Teilen Sie eine lokale Tabelle in mehrere Dateien in verschiedenen Formaten auf, ohne dass ein Cloud-Speicher erforderlich ist
weight: 100
kwords: Excel API, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Lokale Tabellenkalkulation aufteilen, Cloud-Verarbeitung, Dateiverwaltung, Fehlerbehandlung
---
Teilen Sie die lokale Tabelle in separate Dateien mit 30 Ausgabedateiformaten auf, ohne dass Cloud-Speicher erforderlich ist.

## **Geteilte Tabelle API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Kalkulationstabelle| Datei| FormData| Laden Sie die zu teilende Tabellenkalkulationsdatei hoch.|
| aus| Ganze Zahl| Abfrage| Geben Sie den Index des ersten Arbeitsblatts an.|
| Zu| Ganze Zahl| Abfrage| Geben Sie den letzten Arbeitsblattindex an.|
| Ausgabeformat| Zeichenfolge| Abfrage| Definieren Sie das Ausgabedateiformat.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad zum Speichern der Ausgabearbeitsmappe. Der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Definieren Sie den Speichernamen der Ausgabedatei.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Geben Sie bei Bedarf benutzerdefinierte Schriftarten an.|
| regoin| Zeichenfolge| Abfrage| Legen Sie den Tabellenbereich fest.|
| Passwort| Zeichenfolge| Abfrage| Geben Sie das Kennwort für den Zugriff auf die Tabellenkalkulationsdatei ein.|

## **Antwort**

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

## Wo sollten wir die Split-Tabelle API verwenden?

Wenn Sie eine Tabelle in mehrere Dateien aufteilen müssen, können Sie diese API verwenden.

## Warum sollten Sie das Split Spreadsheet API verwenden?

- Kein Cloud-Speicherplatz erforderlich, einfach direkt aufteilen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die geteilte Tabelle API mit SDKs

### Split Spreadsheet API Spezifikation

 Der[Split Spreadsheet API Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) bietet eine öffentlich zugängliche Programmierschnittstelle zum Ausführen von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, Tabellenkalkulationen mit kurzem Code in separate Dateien aufzuteilen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
