---
title: Aspose.Cells Cloud Web API - Konvertieren Sie Tabellendaten einer Kalkulationstabelle in ein Bild
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to an Imag
linktitle: Tabelle in Bild konvertieren
type: docs
url: /de/convert-table-to-image/
keywords: table to image, Aspose.Cells Cloud Web API, cloud conversion, spreadsheet to image, image format
description: Konvertieren Sie eine lokale Tabellenkalkulationstabelle effizient in eine Bilddatei mit dem Aspose.Cells Cloud Web API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Tabelle in Bild konvertieren, Cloud-Konvertierung, Bilddateiformate, Tabellenkalkulationskonvertierung
---
 Konvertieren Sie eine lokale Kalkulationstabelle/Excel-Tabellendaten in ein Bild. Unterstützt**BILDFORMATE:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Tabelle in Bild konvertieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei hoch.|
|Arbeitsblatt|Zeichenfolge|Abfrage|Der Arbeitsblattname von Spreadsheet/Excel|
|Tabellenname|Zeichenfolge|Abfrage|Name der zu konvertierenden Tabelle.|
|Format|Zeichenfolge|Abfrage|Gewünschtes Bilddateiformat (z. B. PNG, SVG).|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem das konvertierte Bild gespeichert wird. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Geben Sie den Speichernamen der Ausgabedatei an.|
|SchriftartenStandort|Zeichenfolge|Abfrage|Verwenden Sie bei Bedarf benutzerdefinierte Schriftarten.|
|Region|Zeichenfolge|Abfrage|Definiert die Tabellenbereichseinstellungen.|
|Passwort|Zeichenfolge|Abfrage|Für den Zugriff auf die Tabellenkalkulationsdatei ist ein Kennwort erforderlich.|

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

## Warum sollten Sie die Funktion „Tabelle in Bild konvertieren“ API verwenden?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Konvertierungstabelle in Bild API mit SDKs?

### Tabelle in Bild konvertieren API Spezifikation

 Der[Tabelle in Bild konvertieren API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToImage) bietet eine öffentlich zugängliche Programmierschnittstelle für die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, Tabellendaten einer Kalkulationstabelle mit einem kurzen Code in ein Bild zu konvertieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{< /tab >}}
{{< /tabs >}}
