---
title: Aspose.Cells Cloud Web API - Tabelleninhalt ersetzen
second_title: Documen
ArticleTitle: Replace Spreadsheet Conten
linktitle: Tabelleninhalt ersetzen
type: docs
url: /de/replace-spreadsheet-content/
keywords: Excel API, Spreadsheet manipulation, Replace text, Office Cloud integration, REST AP
description: Ersetzen Sie effizient Text in lokalen Tabellenkalkulationsdateien mit Aspose.Cells API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Text ersetzen in Excel, Leere Zellen abgleichen in Excel Arbeitsblatt
---
Ersetzen Sie angegebenen Text effizient in lokalen Tabellenkalkulationsdateien.

## **Tabelleninhalt ersetzen API**

```
PUT http://api.aspose.cloud/v4.0/cells/replace/content
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Kalkulationstabelle| Datei| FormData| Laden Sie die Tabellenkalkulationsdatei hoch.|
| Suchtext| Zeichenfolge| Abfrage|Der zu suchende Text.|
| replaceText| Zeichenfolge| Abfrage| Der zu ersetzende Text.|
| Arbeitsblatt| Zeichenfolge| Abfrage| Geben Sie das Arbeitsblatt für den Ersatz an.|
| Zellbereich| Zeichenfolge| Abfrage| Geben Sie den Zellbereich für die Ersetzung an.|
| Region| Zeichenfolge| Abfrage| Die Tabellenbereichseinstellung.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

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

## Wo sollten wir den Inhalt in der Tabelle API ersetzen?

Wenn Sie Inhalte in einer Tabelle durch ein Kennwort ersetzen müssen, können Sie API verwenden.

## Warum sollten Sie den Inhalt in der Tabelle API ersetzen?

- Ersetzen Sie Inhalte in Tabellen schnell durch Passwörter.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie den Inhalt in der Tabelle API mit SDKs ersetzen

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceSpreadsheetContent) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen, Inhalte in Tabellenkalkulationen für Zellen mit minimalem Code einfach zu ersetzen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs mit Aspose.Cells-Webdiensten interagieren:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
