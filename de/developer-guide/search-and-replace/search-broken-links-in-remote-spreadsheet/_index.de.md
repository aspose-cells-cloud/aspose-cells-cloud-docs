---
title: Aspose.Cells Cloud Web API - Suche nach defekten Links in Remote-Tabellen
second_title: Documen
ArticleTitle: Search for Broken Links in Remote Spreadsheet
linktitle: Suche nach Remote-Tabellenkalkulationen Defekter Link
type: docs
url: /de/search-broken-links-in-remote-spreadsheet/
keywords: broken links, remote spreadsheet, Excel API, cloud storage, hyperlink checker, dead URL detection, REST AP
description: Effiziente Suche nach defekten Links in Remote-Tabellen, die in Cloud-Umgebungen gespeichert sind
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, defekte Links, Hyperlink-Validierung, Cloud-Speicher
---
Suchen Sie nach defekten Links in Remote-Tabellen, die in Cloud-Umgebungen gespeichert sind.

## **Suche nach defekten Links in Remote-Tabelle API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg|Der Name der zu durchsuchenden Arbeitsmappendatei.|
|Arbeitsblatt|Zeichenfolge|Abfrage|Geben Sie das Arbeitsblatt für die Suche an.|
|Zellbereich|Zeichenfolge|Abfrage|Geben Sie den Zellenbereich für die Suche an.|
|Ordner|Zeichenfolge|Abfrage|Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist.|
|Speichername|Zeichenfolge|Abfrage|(Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Wenn dieser Name weggelassen wird, wird der Standardspeicher verwendet.|
|Region|Zeichenfolge|Abfrage|Die Tabellenbereichseinstellung.|
|Passwort|Zeichenfolge|Abfrage|Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

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

## Wo sollten wir die Suche nach defekten Links in der Tabelle API verwenden?

Wenn Sie in der Tabelle nach defekten Links suchen müssen, können Sie diese Nummer API verwenden.

## Warum sollten Sie die Suche nach defekten Links in der Tabelle API verwenden?

- Suchen Sie effizient nach defekten Links in Remote-Tabellen, die in Cloud-Umgebungen gespeichert sind.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Suche nach defekten Links in der Tabelle API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchController/SearchBrokenLinksInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen die Implementierung einer in Tabellenkalkulationen nach Zellen unterteilten Suche mit minimalem Code.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs mit Aspose.Cells-Webdiensten interagieren:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
