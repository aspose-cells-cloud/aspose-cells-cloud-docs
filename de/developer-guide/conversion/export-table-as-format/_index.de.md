---
title: Aspose.Cells Cloud Web API – Exportieren Sie die Daten einer Tabellenkalkulation in eine Formatdatei
second_title: Documen
ArticleTitle: Export a Spreadsheet Table data as a Format file
linktitle: Tabelle in angegebenes Format exportieren
type: docs
url: /de/export-table-as-format/
keywords: Spreadsheet Conversion, Aspose.Cells Cloud Web API, Export Table, RESTI, PDF, CSV, Excel, JSON, Markdow
description: Konvertiert Tabellen aus Tabellenkalkulationen im Cloud-Speicher effizient in verschiedene angegebene Formate
weight: 100
kwords: Tabellenkalkulationskonvertierung, PDF, CSV, Excel, JSON, Markdown, Tabellenexport
---
Exportieren Sie eine Cloud-Tabelle/Excel-Tabelle in eine Datei mit einem anderen Format.

## **Tabelle exportieren als Format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg|(Erforderlich) Der Name der abzurufenden Arbeitsmappendatei.|
|Arbeitsblatt|Zeichenfolge|Weg|Name des Arbeitsblatts.|
|Tabellenname|Zeichenfolge|Weg|Name der Tabelle.|
|Format|Zeichenfolge|Abfrage|(Erforderlich) Das gewünschte Format (z. B. „png“, „pdf“, „svg“).|
|Ordner|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|Speichername|Zeichenfolge|Abfrage|(Optional) Der Name des Speichers, wenn benutzerdefinierter Cloud-Speicher verwendet wird. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad für den Ausgabespeicher. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Name des Ausgabedateispeichers.|
|SchriftartenStandort|Zeichenfolge|Abfrage|Speicherort für benutzerdefinierte Schriftarten.|
|Region|Zeichenfolge|Abfrage|Einstellung für den Tabellenkalkulationsbereich.|
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

## Warum sollten Sie die Export-Tabelle im Format API verwenden?

- Sie können Cloud-Dateien jederzeit und überall in verschiedene Formate konvertieren.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Tabellenkalkulationstabelle im Format API mit SDKs?

### Tabelle als Format API Spezifikation exportieren

 Der[Tabelle als Format API Spezifikation exportieren](https://reference.aspose.cloud/cells/#/ConversionController/ExportTableAsFormat) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, Tabellendaten aus einer Kalkulationstabelle in eine Formatdatei mit kurzem Code zu exportieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{< /tab >}}
{{< tab tabtabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
