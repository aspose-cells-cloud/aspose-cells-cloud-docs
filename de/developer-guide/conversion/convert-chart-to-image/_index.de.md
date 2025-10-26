---
title: Aspose.Cells Cloud Web API - Konvertieren Sie ein Tabellenkalkulationsdiagramm in ein Bild
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: Diagramm in Bild konvertieren
type: docs
url: /de/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: Konvertieren Sie ein Diagramm aus einer lokalen Tabellenkalkulations-/Excel-Datei in eine Bilddatei mit dem Aspose.Cells Cloud Web API
weight: 100
kwords: Konvertieren Sie ein Excel-Diagramm in Bild, PNG, SVG, TIFF, JPG, BMP, Spreadshee
---
Konvertieren Sie ein Diagramm aus einer lokalen Tabellenkalkulationsdatei/Excel in eine Datei im Bildformat. Unterstützt**BILDFORMATE:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Diagramm in Bild umwandeln API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die Tabellenkalkulationsdatei mit dem Diagramm hoch.|
|Arbeitsblatt|Zeichenfolge|Abfrage|Geben Sie gegebenenfalls den Arbeitsblattnamen an.|
|Diagrammindex|Ganze Zahl|Abfrage|Index des zu konvertierenden Diagramms.|
|Format|Zeichenfolge|Abfrage|(Erforderlich) Der gewünschte Bildtyp (z. B. SVG, PNG, JPG).|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist; der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Name des Speicherorts für die Ausgabedatei.|
|SchriftartenStandort|Zeichenfolge|Abfrage|Geben Sie bei Bedarf benutzerdefinierte Schriftarten an.|
|Region|Zeichenfolge|Abfrage|Legen Sie den Tabellenbereich fest.|
|Passwort|Zeichenfolge|Abfrage|Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

## **Antwort**

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

## Wo sollten Sie die Funktion „Diagramm in Bild API konvertieren“ verwenden?

- Exportieren Sie die Diagramme in der Tabelle als Bilder.

## Warum sollten Sie die Funktion „Diagramm in Bild konvertieren“ API verwenden?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Funktion „Diagramm in Bild API konvertieren“ mit SDKs?

### Diagramm in Bild konvertieren API Spezifikation

 Der[Diagramm in Bild konvertieren API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, ein Diagramm mit einem kurzen Code in ein Bild umzuwandeln.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
