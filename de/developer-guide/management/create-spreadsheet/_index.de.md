---
title: Aspose.Cells Cloud Web API - Erstellen Sie eine neue Tabelle mit einer Tabellenvorlage
second_title: Documen
ArticleTitle: Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc
linktitle: Tabellenkalkulation erstellen
type: docs
url: /de/create-spreadsheet/
keywords: Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancemen
description: Mit Excel API können Benutzer eine neue Tabelle mit einem bestimmten Namen erstellen und optionale Vorlagen für vordefinierte Inhalte oder Formatierungen unterstützen, wodurch die Benutzerproduktivität gesteigert wird
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen, Tabellenkalkulationserstellung, Vorlagenunterstützung, Produktivitätssteigerung
---
Erstellen Sie eine neue Tabelle. Dabei kann es sich entweder um eine leere Tabelle oder um eine verwendbare Tabelle handeln, die auf der Grundlage der angegebenen Vorlage erstellt wurde.

## **Tabellenkalkulation erstellen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|---------- ||----------------------- |----- |
|Format| Zeichenfolge| Abfrage| Gibt den Namen der neuen Tabelle an. Dieser Name wird zur Identifizierung der Tabelle im System verwendet.|
| Vorlage| Zeichenfolge| Abfrage| Optional. Falls angegeben, wird die neue Tabelle basierend auf der angegebenen Vorlage erstellt. Dies kann nützlich sein, um vordefinierte Layouts und Stile anzuwenden.|
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

## Wo sollten wir die Tabellenkalkulation API verwenden?

Wenn Sie eine neue Tabelle benötigen, können Sie diese Nummer API verwenden.

## Warum sollten Sie die Tabellenkalkulation API verwenden?

- Sie können nicht nur eine leere Tabelle erstellen, sondern auch eine bestimmte Tabelle basierend auf einer Vorlage.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Tabellenkalkulation API mit SDKs

### Tabellenkalkulation erstellen API Spezifikation

 Der[Tabellenkalkulation erstellen API Spezifikation](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, die Tabelle mit kurzem Code zu erstellen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
