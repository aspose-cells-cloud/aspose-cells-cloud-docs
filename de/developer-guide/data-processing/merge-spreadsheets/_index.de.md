---
title: Aspose.Cells Cloud Web API - Mehrere Tabellenkalkulationen zu einer einzigen Tabelle zusammenführen
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: Tabellenkalkulation zusammenführen
type: docs
url: /de/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: Einfaches Zusammenführen lokaler Tabellenkalkulationsdateien in verschiedenen Formaten (XLSX, CSV, PDF) mithilfe der Excel API
weight: 100
kwords: Excel API, Tabellen zusammenführen, Office Cloud, REST API, Tabellen zusammenführen, CSV-Format, JSON, Markdow
---
Führen Sie mehrere lokale Tabellenkalkulationsdateien in einer einzigen Datei zusammen und unterstützen Sie dabei die Ausgabe in über 30 Dateiformaten.

## **Tabellenkalkulation zusammenführen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
| Kalkulationstabelle| Datei| FormData| Laden Sie die Tabellenkalkulationsdatei hoch.|
| Ausgabeformat| Zeichenfolge| Abfrage| Geben Sie das Ausgabedateiformat an.|
| mergeInOneSheet| Boolescher Wert| Abfrage| Geben Sie an, ob alle Daten in einem einzigen Arbeitsblatt zusammengefasst werden sollen.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad für die Ausgabearbeitsmappe. Der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Geben Sie den Speichernamen der Ausgabedatei an.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Definieren Sie die zu verwendenden benutzerdefinierten Schriftarten.|
| Region| Zeichenfolge| Abfrage| Legen Sie den Tabellenbereich fest.|
| Passwort| Zeichenfolge| Abfrage| Geben Sie das Kennwort zum Öffnen der Tabellenkalkulationsdatei ein.|

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

## Wo sollten wir die Merge Local-Tabelle API verwenden?

Wenn Sie mehrere Datendateien zusammenführen müssen, können Sie diese API verwenden.

## Warum sollten Sie das Merge Local Spreadsheet API verwenden?

- Kein Cloud-Speicherplatz erforderlich, einfach direkt zusammenführen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Merge Local-Tabelle API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)bietet eine öffentlich zugängliche Programmierschnittstelle, die es Benutzern ermöglicht, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, mehrere Tabellenblätter mit einem kurzen Code zu einem Tabellenblatt zusammenzuführen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}
