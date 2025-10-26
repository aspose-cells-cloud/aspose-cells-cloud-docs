---
title: Aspose.Cells Cloud Web API - Bereichsinhalte in Remote-Tabellen ersetzen
second_title: Documen
ArticleTitle: Replace Range Content in Remote a Spreadshee
linktitle: Ersetzen Sie den Inhalt des Remote-Bereichs
type: docs
url: /de/replace-content-in-remote-range/
keywords: API, Excel API, Replace Content, Remote Spreadsheet, Cloud Storage, Text Replacement, REST AP
description: Ersetzen Sie effizient Text innerhalb bestimmter Bereiche von Remote-Tabellenkalkulationen mithilfe von Aspose.Cells Cloud API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen, Remote-Textersetzung, Cloud-Speicherintegration
---
Ersetzen Sie effizient angegebenen Text innerhalb eines Bereichs einer Remote-Tabellenkalkulationsdatei.

## **Inhalt im Remote-Bereich ersetzen API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| Der Name der zu ändernden Arbeitsmappendatei.|
| Suchtext| Zeichenfolge| Abfrage| Der Text, nach dem in der Tabelle gesucht werden soll.|
| replaceText| Zeichenfolge| Abfrage| Der Text, durch den der gesuchte Text ersetzt werden soll.|
| Arbeitsblatt| Zeichenfolge| Weg| Der Name des Arbeitsblatts, in dem die Ersetzung erfolgen soll.|
| Zellbereich| Zeichenfolge| Weg| Der spezifische Zellbereich für den Ersatz.|
| Ordner| Zeichenfolge| Abfrage| Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist.|
| Speichername| Zeichenfolge| Abfrage|(Optional) Der Name des Speichers, wenn benutzerdefinierter Cloud-Speicher verwendet wird. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
| Region| Zeichenfolge| Abfrage| Die Tabellenbereichseinstellung.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

### **Antwort**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
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

## Wo sollten wir den Inhalt des Bereichs im Remote-Arbeitsblatt API ersetzen?

Wenn Sie den Inhalt eines Bereichs in einer Remote-Tabelle ersetzen müssen, können Sie API verwenden.

## Warum sollten Sie den Inhalt des Bereichs in der Remote-Tabelle API ersetzen?

- Ersetzen Sie schnell den Inhalt von Range in Remote-Tabellen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie den Inhalt des Bereichs „Ersetzen“ in der Remote-Tabelle API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen, Inhalte in Tabellenkalkulationen für Zellen mit minimalem Code einfach zu ersetzen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
