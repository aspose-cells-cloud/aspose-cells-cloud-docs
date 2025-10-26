---
title: Aspose.Cells Cloud Web API - Leere Zeilen in Spreadsheet löschen
second_title: Documen
ArticleTitle: Delete Blank Rows in a Spreadshee
linktitle: Leere Zeile löschen
type: docs
url: /de/delete-spreadsheet-blank-rows/
keywords: Delete blank rows, Excel API, Spreadsheet cleaning, Aspose.Cells Cloud Web API, Remove empty row
description: Löschen Sie effizient alle leeren Zeilen in einer Tabelle, die keine Daten oder Objekte enthalten, und verbessern Sie so die Datenorganisation
weight: 100
kwords: Excel, REST, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen, Leere Zeilen entfernen
---
Löschen Sie alle leeren Zeilen, die keine Daten oder andere Objekte enthalten, aus einer Excel-Tabelle.

## **DeleteSpreadsheetBlankRows AP**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei hoch.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Name des Ausgabedateispeichers.|
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

## Wo sollten wir die Funktion „Leere Zeilen in der Tabelle löschen“ API verwenden?

Wenn Sie Daten transformieren müssen, können Sie diese API verwenden.

## Warum sollten Sie die Funktion „Leere Zeilen in der Tabelle löschen“ API verwenden?

- Löschen Sie schnell alle leeren Zeilen, die keine Daten oder andere Objekte enthalten, aus einer Excel-Tabelle.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Funktion „Leere Zeilen in Tabellenkalkulationen löschen“ API mit SDKs

### Löschen von leeren Tabellenzeilen API Spezifikation

 Der[Löschen von leeren Tabellenzeilen API Spezifikation](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, leere Tabellenzeilen mit einem kurzen Code zu löschen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}
{{< /tab >}}
{{< /tabs >}}
