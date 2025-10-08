---
title: Aspose.Cells Cloud Web API - Arbeitsblatt in Spreadsheet umbenennen
second_title: Documen
ArticleTitle: Rename worksheet in Spreadshee
linktitle: Arbeitsblatt in Tabellenkalkulation umbenennen
type: docs
url: /de/rename-worksheet-in-spreadsheet/
keywords: Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet Organizatio
description: Der Web-Endpunkt API ermöglicht es Benutzern, ein bestimmtes Arbeitsblatt innerhalb einer Arbeitsmappe umzubenennen, wodurch die Organisation und Lesbarkeit verbessert wird
weight: 100
kwords: Excel API, Arbeitsblatt umbenennen, Arbeitsmappenverwaltung, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen
---
Benennen Sie den Arbeitsblattnamen in einer Tabelle um.

## **Arbeitsblattnamen in Tabellenkalkulation API umbenennen**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei hoch.|
|Quellname|Zeichenfolge|Abfrage|Aktueller Name des umzubenennenden Arbeitsblatts.|
|Zielname|Zeichenfolge|Abfrage|Neuer Name für das Arbeitsblatt.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Speichername der Ausgabedatei.|
|Region|Zeichenfolge|Abfrage|Tabellenkalkulationsbereichseinstellung.|
|Passwort|Zeichenfolge|Abfrage|Passwort zum Öffnen der Tabellenkalkulationsdatei.|

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

## Wo sollten wir das Arbeitsblatt „Umbenennen“ in der Tabelle API verwenden?

Wenn Sie Arbeitsblätter in Tabellenkalkulationen umbenennen müssen, können Sie API verwenden.

## Warum sollten Sie das Arbeitsblatt umbenennen in der Tabelle API verwenden?

- Benennen Sie Arbeitsblätter aus Tabellenkalkulationen schnell um.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie das Arbeitsblatt „Umbenennen“ in der Tabelle API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet)beschreibt eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen die einfache Implementierung der Umbenennung von Arbeitsblattnamen in Tabellen für Zellen mit minimalem Code.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
