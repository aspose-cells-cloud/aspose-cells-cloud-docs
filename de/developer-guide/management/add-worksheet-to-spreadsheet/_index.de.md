---
title: Aspose.Cells Cloud Webb API - Hinzufügen eines Arbeitsblatts zu einer Tabelle
second_title: Documen
ArticleTitle: Add a Worksheet to a Spreadshee
linktitle: Arbeitsblatt zu Tabellenkalkulation hinzufügen
type: docs
url: /de/add-worksheet-to-spreadsheet/
keywords: Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, RES
description: Mit dem Cloud Web Aspose.Cells können Entwickler effizient ein neues Arbeitsblatt zu einer Arbeitsmappe hinzufügen und haben die Kontrolle über Typ, Position und Namen des Arbeitsblatts. Diese Funktionalität verbessert die Verwaltung und Flexibilität von Arbeitsmappen.
weight: 100
kwords: Excel, Office Cloud, REST, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Verwalten von Excel Arbeitsblättern, Dynamische Tabellenkalkulationserstellung
---
Hinzufügen eines Arbeitsblatts zur Tabelle, wobei Typ und Speicherort des Arbeitsblatts angegeben werden.

|**Arbeitsblatttyp** | Beschreibung|
|:- |:- |
|**VB** | Visual Basic-Modul|
|**Arbeitsblatt** | Arbeitsblatt|
|**Diagramm** | Diagrammblatt|
|**BIFF4Macro** | BIFF4-Makroblatt|
|**InternationalMacro** | Internationales Makroblatt|
|**Andere** | Internationales Makroblatt|
|**Dialog** | Dialog-Arbeitsblatt|

## **Arbeitsblatt zur Tabelle hinzufügen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Tabellenkalkulationsdatei hochladen.|
|Blatttyp|Zeichenfolge|Abfrage|Gibt den Namen des neuen Arbeitsblatts an. Wenn kein Name angegeben wird, wird ein Standardname zugewiesen.|
|Position|Ganze Zahl|Abfrage|Gibt die Position an, an der das neue Arbeitsblatt eingefügt werden soll. Wenn keine Angabe erfolgt, wird das Arbeitsblatt am Ende der Arbeitsmappe eingefügt.|
|Blattname|Zeichenfolge|Abfrage|Gibt den Typ des hinzuzufügenden Arbeitsblatts an. Wenn kein Wert angegeben wird, wird ein Standardarbeitsblatttyp verwendet.|
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

## Wo sollten wir das Arbeitsblatt zur Tabelle API hinzufügen?

Wenn Sie ein Arbeitsblatt für eine Kalkulationstabelle hinzufügen müssen, können Sie diese API verwenden.

## Warum sollten Sie das Arbeitsblatt zur Tabelle API hinzufügen?

- Fügen Sie der Tabelle ein Arbeitsblatt hinzu und geben Sie den Typ und den Speicherort des Arbeitsblatts an.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie „Arbeitsblatt zu Tabellenkalkulation hinzufügen“ API mit SDKs

### Arbeitsblatt zur Tabellenkalkulation API hinzufügen Spezifikation

 Der[Arbeitsblatt zur Tabellenkalkulation API hinzufügen Spezifikation](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, mit einem kurzen Code ein Arbeitsblatt zu einer Tabelle hinzuzufügen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs API-Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
