---
title: Aspose.Cells Cloud Web API - Konvertieren Sie Tabellendaten einer Kalkulationstabelle in eine CSV-Datei
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Csv file
linktitle: Tabelle in CS konvertieren
type: docs
url: /de/convert-table-to-csv/
keywords: convert table to csv, convert spreadsheet to csv, Excel to CSV conversion, cloud conversio
description: Konvertiert effizient eine Tabelle aus einer Kalkulationstabelle auf Ihrem lokalen Laufwerk in eine CSV-Datei mit unserem API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Tabelle zu CSV, Konvertierung von lokal zu Cloud
---
Konvertieren Sie eine lokale Kalkulationstabelle/Excel in eine CSV-Datei.

## **Tabelle in CSV konvertieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|-------------|-|------------------------|-------------------------------------------|
| Kalkulationstabelle| Datei| FormData| Laden Sie die Tabellenkalkulationsdatei hoch.|
| Arbeitsblatt|Zeichenfolge| Abfrage| Name des Arbeitsblatts in der Tabelle.|
| Tabellenname|Zeichenfolge| Abfrage|Name der zu konvertierenden Tabelle.|
| Ausgangspfad|Zeichenfolge| Abfrage| (Optional) Ordnerpfad, in dem die Arbeitsmappe gespeichert ist; Standardwert ist null.|
| outStorageName|Zeichenfolge| Abfrage| Name des Ausgabedateispeichers.|
| SchriftartenStandort|Zeichenfolge| Abfrage| Pfad zur Verwendung benutzerdefinierter Schriftarten.|
| Region|Zeichenfolge| Abfrage| Definiert die Einstellung für den Tabellenbereich.|
| Passwort|Zeichenfolge| Abfrage| Passwort zum Öffnen der Tabellenkalkulationsdatei.|

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

## Warum sollten Sie die Funktion „Tabelle in CSV konvertieren API“ verwenden?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Konvertierungstabelle in CSV API mit SDKs?

### Tabelle in CSV konvertieren API Spezifikation

 Der[Tabelle in CSV konvertieren API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToCsv) bietet eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, die Daten einer Tabellenkalkulation mit einem kurzen Code in eine CSV-Datei zu konvertieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
