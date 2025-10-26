---
title: Aspose.Cells Cloud Web API - Bereich in Tabellenkalkulation austauschen
second_title: Documen
ArticleTitle: Swap Range Data in a Spreadshee
linktitle: Rang tauschen
type: docs
url: /de/swap-range/
keywords: Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, RES
description: Die Funktion „Bereiche austauschen für Excel API“ bietet ein leistungsstarkes Tool zum Austauschen beliebiger Spalten, Zeilen, Bereiche oder einzelner Zellen innerhalb einer Excel-Datei. Mit dieser Funktion können Benutzer ihre Tabellen effizient neu anordnen und dabei sicherstellen, dass die ursprüngliche Datenformatierung erhalten bleibt und alle vorhandenen Formeln weiterhin korrekt funktionieren. Mit dieser Funktion können Benutzer ihre Datenmanipulationsaufgaben optimieren und die Integrität ihrer Tabellenkalkulationen wahren.
weight: 100
kwords: Excel, Office Cloud, REST, PDF, CSV, Json, Markdown
---
Tauschen Sie Daten zwischen zwei beliebigen Spalten, Zeilen, Bereichen oder einzelnen Zellen in einer Excel-Datei aus.

## **Swap-Bereich API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei hoch.|
|Arbeitsblatt1|Zeichenfolge|Abfrage|Geben Sie das Arbeitsblatt an, das die Quelle des Austauschdatenbereichs ist.|
|Bereich1|Zeichenfolge|Abfrage|Geben Sie die Quelle für die Austauschdaten an.|
|Arbeitsblatt2|Zeichenfolge|Abfrage|Geben Sie das Arbeitsblatt an, das das Ziel des Austauschdatenbereichs ist.|
|Bereich2|Zeichenfolge|Abfrage|Geben Sie das Ziel für den Datenaustausch an.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Speichername der Ausgabedatei.|
|Region|Zeichenfolge|Abfrage|Die Tabellenbereichseinstellung.|
|Passwort|Zeichenfolge|Abfrage|Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

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

## Wo sollten wir den Swap Range API verwenden?

Wenn Sie Bereichsdaten in einer Tabelle austauschen müssen, können Sie diese API verwenden.

## Warum sollten Sie den Swap Range API verwenden?

- Tauschen Sie Bereichsdaten schnell in einer Excel-Tabelle aus.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie den Swap-Bereich API mit SDKs

### Swap Range API Spezifikation

 Der[Swap Range API Spezifikation](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, den Bereich durch kurzen Code auszutauschen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
