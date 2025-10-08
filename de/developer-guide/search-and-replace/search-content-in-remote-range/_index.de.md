---
title: Aspose.Cells Cloud Web API - Suchbereichsinhalt in Remote-Tabellen
second_title: Documen
ArticleTitle: Search Range Content in Remote Spreadshee
linktitle: Remote Range-Inhalte durchsuchen
type: docs
url: /de/search-content-in-remote-range/
keywords: Excel API, Remote Spreadsheet Search, Cloud Storage, Data Retrieval, Spreadsheet Search, Text Search AP
description: Suchen Sie effizient nach Text innerhalb eines angegebenen Bereichs einer Remote-Tabelle, die im Cloud-Speicher gespeichert ist, mithilfe der Excel API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, Textsuche, JSON, CSV, PDF, Markdown, Match Blank Cells in Exce
---
Suchen Sie nach einem bestimmten Text innerhalb eines Bereichs einer Remote-Tabelle.

## **Suche nach Inhalten im Remote-Bereich API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg|Der Name der Tabellenkalkulationsdatei.|
|Arbeitsblatt|Zeichenfolge|Weg|Der Name des Arbeitsblatts.|
|Zellbereich|Zeichenfolge|Weg|Der Zellbereich, in dem gesucht werden soll.|
|Suchtext|Zeichenfolge|Abfrage|Der zu suchende Text.|
|Groß-/Kleinschreibung ignorieren|Boolescher Wert|Abfrage|Geben Sie an, ob bei der Suche die Groß- und Kleinschreibung ignoriert werden soll.|
|Ordner|Zeichenfolge|Abfrage|Der Ordner, in dem die Datei gespeichert ist.|
|Speichername|Zeichenfolge|Abfrage|(Optional) Der Name des Speichers, wenn benutzerdefinierter Cloud-Speicher verwendet wird. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
|regoin|Zeichenfolge|Abfrage|Die Tabellenbereichseinstellung.|
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

## Wo sollten wir den Suchinhalt im Bereich der Tabelle API verwenden?

Wenn Sie Inhalte innerhalb des Tabellenkalkulationsbereichs suchen müssen, können Sie diese API verwenden.

## Warum sollten Sie den Suchinhalt im Bereich der Tabelle API verwenden?

- Mit dieser Nummer API können Sie mühelos Inhalte innerhalb eines entfernten Tabellenkalkulationsbereichs durchsuchen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Suche nach defekten Links im Bereich der Tabelle API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen die einfache Implementierung von Suchinhalten innerhalb von Tabellenkalkulationen für Zellen mit minimalem Code.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
