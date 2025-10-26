---
title: Aspose.Cells Cloud Web API - Komprimieren Sie die Größe der Tabelle
second_title: Documen
ArticleTitle: Compress the size of the Spreadshee
linktitle: Tabellenkalkulation komprimieren
type: docs
url: /de/compress-spreadsheet/
keywords: Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web AP
description: Mit der Compress Spreadsheet API können Benutzer die Dateigröße von Tabellenkalkulationen effizient reduzieren, indem sie bestimmte Komprimierungsstufen anwenden, den Speicher optimieren und die Leistung verbessern
weight: 100
kwords: Excel, Office Cloud, REST, Tabellenkalkulationskomprimierung, Dateigrößenoptimierung, PDF, CSV, Json, Markdow
---
Komprimieren Sie die Größe der Tabelle.

## **Tabelle komprimieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die zu komprimierende Tabellenkalkulationsdatei hoch.|
|Ebene|Ganze Zahl|Abfrage|Gibt die anzuwendende Komprimierungsstufe an, die von 0 (keine Komprimierung) bis 9 (maximale Komprimierung) reicht.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die komprimierte Arbeitsmappe gespeichert wird. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Name des Ausgabedateispeichers.|
|Region|Zeichenfolge|Abfrage|Die Tabellenbereichseinstellung.|
|Passwort|Zeichenfolge|Abfrage|Das zum Öffnen der Tabellenkalkulationsdatei erforderliche Kennwort.|

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

## Wo sollten wir die Komprimierungstabelle API verwenden?

Wenn Sie die Größe von Tabellenkalkulationen reduzieren müssen, können Sie diese API verwenden.

## Warum sollten Sie die Komprimierungstabelle API verwenden?

- Die Tabelle ist zu groß und die Dateigröße muss reduziert werden.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Komprimierungstabelle API mit SDKs

### Komprimieren Sie die Tabellenkalkulation API Spezifikation

 Der[Komprimieren Sie die Tabellenkalkulation API Spezifikation](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) bietet eine öffentlich zugängliche Schnittstelle für REST-Interaktionen, die direkte API-Aufrufe von einem Webbrowser aus ermöglicht.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, die Größe der Tabelle mit kurzem Code zu komprimieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs mit Aspose.Cells-Webdiensten interagieren:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
