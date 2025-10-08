---
title: Aspose.Cells Cloud Web API - Verschieben Sie ein Arbeitsblatt an eine neue Position in der Tabelle
second_title: Documen
ArticleTitle: Move worksheet to new position in Spreadshee
linktitle: Arbeitsblatt in Tabellenkalkulation verschieben
type: docs
url: /de/move-worksheet-in-spreadsheet/
keywords: Move Worksheet, Aspose.Cells Cloud Web API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Excel AP
description: Mit MoveWorksheet API können Benutzer ein bestimmtes Arbeitsblatt innerhalb einer Arbeitsmappe effizient neu positionieren und so die Organisation und Zugänglichkeit von Tabellenkalkulationsdaten verbessern.
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, Arbeitsblatt verschieben, Arbeitsmappenorganisation, PDF, CSV, JSON, Markdown
---
Verschieben Sie ein Arbeitsblatt an eine neue Position in einer Kalkulationstabelle.

## **Arbeitsblatt aus Tabellenkalkulation API verschieben**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei hoch.|
|Arbeitsblatt|Zeichenfolge|Abfrage|Der aktuelle Name des zu verschiebenden Arbeitsblatts.|
|Position|Ganze Zahl|Abfrage|Die neue Position für das Arbeitsblatt.|
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

## Wo sollten wir das Arbeitsblatt „Verschieben“ in der Tabelle API verwenden?

Wenn Sie ein Arbeitsblatt in Tabellenkalkulationen an eine neue Position verschieben müssen, können Sie diese API verwenden.

## Warum sollten Sie das Arbeitsblatt „Verschieben“ in der Tabelle API verwenden?

- Verschieben Sie Arbeitsblätter schnell aus Tabellenkalkulationen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie das Arbeitsblatt „Verschieben“ in der Tabelle API mit SDKs

### Arbeitsblatt in Tabellenkalkulation verschieben API Spezifikation

 Der[Arbeitsblatt in Tabellenkalkulation verschieben API Spezifikation](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) bietet eine öffentlich zugängliche Programmierschnittstelle, um direkte REST-Interaktionen von einem Webbrowser aus zu ermöglichen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, Arbeitsblätter mit einem kurzen Code in der Tabelle zu verschieben.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
Die folgenden Codebeispiele zeigen, wie die Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
