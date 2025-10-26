---
title: Aspose.Cells Cloud Web API - Konvertieren eines Tabellenkalkulationsdiagramms in eine PDF-Datei
second_title: Documen
ArticleTitle: Converting a Spreadsheet Chart to a Pdf file
linktitle: Diagramm in PD konvertieren
type: docs
url: /de/convert-chart-to-pdf/
keywords: convert an Excel chart to pdf, convert spreadsheet to pdf, Aspose Cloud Web  API, cloud conversion, Excel to PD
description: Diese API konvertiert Diagramme aus Tabellenkalkulationen auf einem lokalen Laufwerk in PDF Datei nahtlos
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulationskonvertierung, PDF, CSV, JSON, Markdown, Diagramm in PDF konvertieren, Cloud-Konvertierung
---
 Konvertieren Sie ein Diagramm aus einer lokalen Tabellenkalkulationsdatei/Excel in eine[PDF](https://docs.fileformat.com/pdf/) Datei.

## **Diagramm in PDF konvertieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|-------------- ||--------------------- |--------------------------------------------------- |
| Kalkulationstabelle|Datei| FormData| Laden Sie die Tabellenkalkulationsdatei hoch.|
| Arbeitsblatt| Zeichenfolge| Abfrage| Der Name des Arbeitsblatts, das das Diagramm enthält.|
| Diagrammindex|Ganze Zahl| Abfrage| Der Index des zu konvertierenden Diagramms.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die konvertierte Datei gespeichert ist. Der Standardwert ist null.|
| outStorageName| Zeichenfolge| Abfrage| Name des Ausgabedateispeichers.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Verwenden Sie bei Bedarf benutzerdefinierte Schriftarten.|
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

## Wo sollten Sie die Funktion „Diagramm in PDF konvertieren API“ verwenden?

- Exportieren Sie die Diagramme in der Tabelle als PDF.

## Warum sollten Sie die Funktion „Diagramm in PDF konvertieren API“ verwenden?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Funktion „Diagramm in PDF konvertieren API“ mit SDKs?

### Diagramm in PDF konvertieren API Spezifikation

 Der[Diagramm in PDF konvertieren API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

## Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, ein Diagramm mit einem kurzen Code in eine PDF-Datei zu konvertieren.
Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
