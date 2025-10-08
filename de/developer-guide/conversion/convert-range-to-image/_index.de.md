---
title: Aspose.Cells Cloud Web API - Konvertieren Sie einen Tabellenbereichsdatensatz in ein Bild
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to an Imag
linktitle: Bereich in Bild konvertieren
type: docs
url: /de/convert-range-to-image/
keywords: Aspose.Cells Cloud Web API, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Format
description: Konvertieren Sie Bereichsdaten aus einer lokalen Tabellenkalkulations-/Excel-Datei in eine Bilddatei
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, Bildkonvertierung, PNG, SVG, TIFF, JSON, Markdown
---
Konvertieren Sie Bereichsdaten aus einer lokalen Tabellenkalkulations-/Excel-Datei in eine Bilddatei. Unterstützt**BILDFORMATE:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Bereich in Bild konvertieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei zur Konvertierung hoch.|
|Arbeitsblatt|Zeichenfolge|Abfrage|Der Arbeitsblattname von Spreadsheet/Excel|
|Reichweite|Zeichenfolge|Abfrage|Definieren Sie den zu konvertierenden Zellbereich (z. B. A1:C10).|
|Format|Zeichenfolge|Abfrage|Geben Sie das Ausgabedateiformat an (z. B. PNG, SVG, TIFF).|
|Überschriften drucken|Boolescher Wert|Abfrage|Geben Sie an, ob Zeilen- und Spaltenüberschriften gedruckt werden sollen.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist; der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Name des Ausgabedateispeichers.|
|SchriftartenStandort|Zeichenfolge|Abfrage|Benutzerdefinierte Schriftarten zur Verwendung bei der Konvertierung.|
|regoin|Zeichenfolge|Abfrage|Definieren Sie die Einstellung für den Tabellenbereich.|
|Passwort|Zeichenfolge|Abfrage|Kennwort zum Öffnen der Tabellenkalkulationsdatei, falls geschützt.|

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

## Warum sollten Sie den Bereich in Bild API konvertieren?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich den Konvertierungsbereich in Bild API mit SDKs?

### Bereich in Bild konvertieren API Spezifikation

 Der[Bereich in Bild konvertieren API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToImage) bietet eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von Ihrem Webbrowser aus ermöglicht.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, einen Datenbereich mit einem kurzen Code in ein Bild zu konvertieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
