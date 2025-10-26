---
title: Aspose.Cells Cloud Web API - Konvertieren Sie Daten aus einem Tabellenkalkulationsbereich in eine CSV-Datei
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to a CSV file.
linktitle: Bereich in CS konvertieren
type: docs
url: /de/convert-range-to-csv/
keywords: Convert range to csv, convert spreadsheet to csv, Aspose Cloud Web API, cloud conversion, Excel to cs
description: Konvertieren Sie einen angegebenen Bereich aus einer lokalen Tabellenkalkulationsdatei in ein CSV-Format mithilfe von Excel API und gewährleisten Sie so eine nahtlose Cloud-Ausführung
weight: 100
kwords: Bereich in CSV, Tabellenkalkulation in CSV konvertieren, Aspose Cloud Web API, Cloud-Konvertierung, Excel in CSV
---
 Konvertieren Sie Bereichsdaten aus einer lokalen Tabellenkalkulations-/Excel-Datei in eine[CSV](https://docs.fileformat.com/spreadsheet/csv/) Datei.

## **Bereich in CSV konvertieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei hoch.|
|Arbeitsblatt|Zeichenfolge|Abfrage|Der Arbeitsblattname von Spreadsheet/Excel|
|Reichweite|Zeichenfolge|Abfrage|Geben Sie den Zellbereich an (z. B. A1:C10).|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert wird. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Name des Ausgabedateispeichers.|
|SchriftartenStandort|Zeichenfolge|Abfrage|Geben Sie bei Bedarf benutzerdefinierte Schriftarten an.|
|Region|Zeichenfolge|Abfrage|Definiert die Einstellung für den Tabellenbereich.|
|Passwort|Zeichenfolge|Abfrage|Zum Öffnen der Tabellenkalkulationsdatei ist ein Kennwort erforderlich.|

### **Antwort**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream",
        }
    }
]
```

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Warum sollten Sie die Funktion „Diagramm in CSV konvertieren API“ verwenden?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Funktion „Diagramm in CSV API konvertieren“ mit SDKs?

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv) beschreibt eine öffentlich zugängliche API, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

## Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, einen Datenbereich mit einem kurzen Code in eine CSV-Datei zu konvertieren.
 Entdecken Sie die vollständige Liste der Aspose.Cells Cloud SDKs in unserem[GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
