---
title: Aspose.Cells Cloud Web API - Löschen eines Arbeitsblatts aus der Tabelle
second_title: Documen
ArticleTitle: Delete a worksheet from the Spreadshee
linktitle: Arbeitsblatt aus Tabellenkalkulation löschen
type: docs
url: /de/delete-worksheet-from-spreadsheet/
keywords: delete worksheet, spreadsheet management, Aspose.Cells Cloud Web API, REST API, workbook structure, remove worksheet
description: Dieser Endpunkt API ermöglicht es Benutzern, ein bestimmtes Arbeitsblatt aus einer Arbeitsmappe zu löschen, wodurch die Verwaltung von Arbeitsmappenstrukturen vereinfacht wird, indem unnötige oder redundante Arbeitsblätter eliminiert werden
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Arbeitsblätter verwalten Excel, Redundante Arbeitsblätter löschen
---
Löschen Sie ein Arbeitsblatt aus einer Kalkulationstabelle.

## **Arbeitsblatt aus Tabelle API löschen**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:-               |:-     |:-                         |:-           |
| Kalkulationstabelle|Datei| FormData| Laden Sie die Tabellenkalkulationsdatei hoch.|
| Blattname| Zeichenfolge| Abfrage| Gibt den Namen oder die Kennung des zu löschenden Arbeitsblatts an. Dieser Parameter ist erforderlich und muss mit dem Namen eines vorhandenen Arbeitsblatts in der Arbeitsmappe übereinstimmen.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
| outStorageName| Zeichenfolge| Abfrage| Speichername der Ausgabedatei.|
| Region| Zeichenfolge| Abfrage| Die Tabellenbereichseinstellung.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

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

## Wo sollten wir das Arbeitsblatt aus der Tabelle API löschen?

Wenn Sie ein Arbeitsblatt aus Tabellenkalkulationen löschen müssen, können Sie diese API verwenden.

## Warum sollten Sie das Arbeitsblatt aus der Tabelle API löschen?

- Entfernen Sie schnell Arbeitsblätter aus Tabellenkalkulationen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie das Arbeitsblatt „Löschen“ aus der Tabelle API mit SDKs

### Arbeitsblatt aus der Tabelle API löschen Spezifikation

 Der[Arbeitsblatt aus der Tabelle API löschen Spezifikation](https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, mit einem kurzen Code ein Arbeitsblatt aus der Tabelle zu löschen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
