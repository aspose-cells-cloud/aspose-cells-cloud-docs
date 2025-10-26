---
title: Aspose.Cells Cloud Web API - Tabellenkalkulationsinhalte durchsuchen
second_title: Documen
ArticleTitle: Search Spreadsheet Conten
linktitle: Tabelleninhalt durchsuchen
type: docs
url: /de/search-spreadsheet-content/
keywords: Excel, Office Cloud, REST API, Spreadsheet Search, PDF Export, CSV Handling, JSON Formatting, Markdown Integration, Match Empty Cells in Exce
description: Suchen Sie effizient nach Text in lokalen Tabellenkalkulationsdateien mit unserem API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulationssuche, PDF Export, CSV-Verarbeitung, JSON-Formatierung, Markdown-Integration, Match Empty Cells in Excel
---
Suchen Sie mit unserer API nach Text in lokalen Tabellenkalkulationsdateien.

## **Tabellenkalkulationsinhalt durchsuchen API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/content
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei zur Suche hoch.|
|Suchtext|Zeichenfolge|Abfrage|Der Text, nach dem in der Tabelle gesucht werden soll.|
|Groß-/Kleinschreibung ignorieren|Boolescher Wert|Abfrage|Geben Sie an, ob die Groß-/Kleinschreibung bei der Suche ignoriert werden soll.|
|Arbeitsblatt|Zeichenfolge|Abfrage|Geben Sie das Arbeitsblatt an, in dem gesucht werden soll.|
|Zellbereich|Zeichenfolge|Abfrage|Geben Sie den zu durchsuchenden Zellbereich an.|
|Region|Zeichenfolge|Abfrage|Die Regionseinstellung für die Tabelle.|
|Passwort|Zeichenfolge|Abfrage|Das zum Öffnen der Tabellenkalkulationsdatei erforderliche Kennwort.|

### **Antwort**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Wo sollten wir den Suchinhalt innerhalb der Tabelle API verwenden?

Wenn Sie Inhalte in der Tabelle suchen müssen, können Sie diese API verwenden.

## Warum sollten Sie den Suchinhalt in der Tabelle API verwenden?

- Mit dieser Nummer API können Sie mühelos Inhalte in einer Tabelle suchen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Suche nach defekten Links in der Tabelle API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen die einfache Implementierung von Suchinhalten in Tabellenkalkulationen für Zellen mit minimalem Code.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
