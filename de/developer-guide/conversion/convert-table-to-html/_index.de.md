---
title: Aspose.Cells Cloud Web API - Konvertieren Sie die Daten einer Tabellenkalkulation in eine HTML-Datei
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Html fil
linktitle: Tabelle in HTM konvertieren
type: docs
url: /de/convert-table-to-html/
keywords: Excel Table to HTML, Spreadsheet Conversion, Aspose.Cells Cloud Web API, REST, Convert Excel to HTML, Table to HTML, Document Conversion, Cloud Service
description: Konvertieren Sie Tabellen aus lokalen Tabellenkalkulationsdateien einfach in das HTML-Format mit unserem Cloud-basierten API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, HTML, PDF, CSV, JSON, Markdown, Leere Zellen in Exce abgleichen
---
Konvertieren Sie die Daten einer lokalen Kalkulationstabelle/Excel in eine HTML-Datei.

## **Tabelle in HTML konvertieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
| Kalkulationstabelle| Datei| FormData| Laden Sie die zu konvertierende Tabellenkalkulationsdatei hoch.|
| Arbeitsblatt| Zeichenfolge| Abfrage| Der Arbeitsblattname von Spreadsheet/Excel|
| Tabellenname| Zeichenfolge| Abfrage| Der Name der zu konvertierenden Tabelle.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die konvertierte Datei gespeichert wird. Der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Der angegebene Speichername für die Ausgabedatei.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Geben Sie benutzerdefinierte Schriftarten für die Konvertierung an.|
| Region| Zeichenfolge| Abfrage| Definieren Sie die Tabellenbereichseinstellungen.|
| Passwort| Zeichenfolge| Abfrage| Das für den Zugriff auf die Tabellenkalkulationsdatei erforderliche Kennwort.|

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

## Warum sollten Sie die Funktion „Tabelle in HTML konvertieren API“ verwenden?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Konvertierung von Tabellen in HTML API mit SDKs?

### Tabelle in HTML konvertieren API Spezifikation

 Der[Tabelle in HTML konvertieren API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToHtml) beschreibt eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von Ihrem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, die Daten einer Tabellenkalkulation mit einem kurzen Code in eine HTML-Datei zu konvertieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen die Interaktion mit Aspose.Cells-Webdiensten mithilfe verschiedener SDKs:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}
