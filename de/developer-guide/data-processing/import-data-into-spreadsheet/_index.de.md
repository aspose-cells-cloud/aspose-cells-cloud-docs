---
title: Aspose.Cells Cloud Web API – Importieren Sie CSV-, JSON- oder XML-Daten in eine Tabellenkalkulationsdatei
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: Daten in Tabellenkalkulation importieren
type: docs
url: /de/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: Importieren Sie effizient Daten aus unterstützten Formaten wie CSV, JSON und XML in eine Tabelle mithilfe des Aspose.Cells Cloud Web API
weight: 100
kwords: Aspose.Cells Cloud Web API, Daten importieren, Office Cloud, REST, Tabellenkalkulation, CSV, JSON, XM
---
 Importieren Sie Daten in ein Tabellenblatt. Das unterstützte Format der importierten Datendatei ist[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) oder[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **Daten in Tabellenkalkulation importieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Datendatei| Datei| FormData| Laden Sie die zu importierende Datendatei hoch.|
| Kalkulationstabelle| Datei| FormData| Laden Sie die Zieltabellendatei hoch.|
| Arbeitsblatt| Zeichenfolge| Abfrage| Geben Sie das Arbeitsblatt für den Datenimport an.|
| Startzelle| Zeichenfolge| Abfrage|Geben Sie die Startposition für den Datenimport an.|
| einfügen| Boolescher Wert| Abfrage| Gibt an, ob die angegebenen Importdaten eingefügt oder überschrieben werden sollen.|
| convertNumericData| Boolescher Wert| Abfrage| Geben Sie an, ob numerische Daten während des Imports konvertiert werden sollen.|
| Splitter| Zeichenfolge| Abfrage| Geben Sie das Trennzeichen für das CSV-Format an.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Geben Sie den Speichernamen der Ausgabedatei an.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Definieren Sie die zu verwendenden benutzerdefinierten Schriftarten.|
| regoin| Zeichenfolge| Abfrage| Legen Sie die Tabellenbereichskonfiguration fest.|
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

## Wo sollten wir die Funktion „Daten in die Tabelle API importieren“ verwenden?

- Importieren großer Datenmengen in ein Tabellenkalkulationsblatt.
-  Das importierte Datendateiformat ist[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) Und[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## Warum sollten Sie die Funktion „Daten in Tabellenkalkulation importieren“ API verwenden?

- Importieren großer Datenmengen in Tabellenkalkulationen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie den Datenimport in die Tabelle API mit SDKs

### Daten in Tabellenkalkulation importieren API Spezifikation

 Der[Daten in Tabellenkalkulation importieren API Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) bietet eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von Ihrem Webbrowser aus ermöglicht.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, Daten mit einem kurzen Code in ein Tabellenkalkulationsarbeitsblatt zu importieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
