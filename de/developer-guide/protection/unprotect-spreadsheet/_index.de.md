---
title: Aspose.Cells Cloud Web API - Tabellenkalkulation mit Passwort aufheben
second_title: Documen
ArticleTitle: Unprotect the Spreadsheet with passwor
linktitle: Tabellenkalkulation aufheben
type: docs
url: /de/unprotect-spreadsheet/
keywords: Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Managemen
description: Entfernt effizient den zweischichtigen Passwortschutz aus Excel-Tabellen und unterstützt sowohl das Öffnen als auch das Ändern von Passwörtern mit fortschrittlichen Verschlüsselungstechniken
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen
---
Wendet die Funktion zum Aufheben des Kennwortschutzes für Excel-Tabellen an und unterstützt sowohl das Öffnen als auch das Ändern von Kennwörtern.

## **Tabellenkalkulation API entsperren**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei hoch, um sie ungeschützt zu lassen.|
|Passwort|Zeichenfolge|Abfrage|Das Verschlüsselungskennwort für die Tabellenkalkulationsdatei.|
|Passwort ändern|Zeichenfolge|Abfrage|Das zum Ändern der geschützten Datei erforderliche Kennwort.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die ungeschützte Arbeitsmappe gespeichert wird. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Gibt den Speichernamen der Ausgabedatei an.|
|Region|Zeichenfolge|Abfrage|Definiert die Tabellenbereichseinstellungen.|

### **Antwort**

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

## Wo sollten wir die Funktion „Leere Spalten der Tabelle löschen“ API verwenden?

Wenn Sie Daten transformieren müssen, können Sie diese API verwenden.

## Warum sollten Sie die Funktion „Leere Spalten in Tabellenkalkulationen löschen“ API verwenden?

- Löschen Sie schnell alle leeren Spalten, die keine Daten oder andere Objekte enthalten, aus einer Excel-Tabelle.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Funktion „Leere Spalten in Tabellenkalkulationen löschen“ API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen das einfache Löschen leerer Spalten für Zellen in Tabellenkalkulationen mit minimalem Code.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
