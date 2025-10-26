---
title: Aspose.Cells Cloud Web API – Exportieren Sie Daten aus einem Tabellenkalkulationsbereich als Formatdatei
second_title: Documen
ArticleTitle: Export a Spreadsheet Range data as a Format file
linktitle: Bereich als Forma exportieren
type: docs
url: /de/export-range-as-format/
keywords: Aspose.Cells Cloud Web API, Export range, Spreadsheet conversion, REST API, PDF, CSV, JSON, Markdown, Excel workshee
description: Konvertieren Sie einen bestimmten Bereich einer Tabelle im Cloud-Speicher in verschiedene Formate wie PDF, CSV oder Bildformate, ohne die Datei herunterzuladen
weight: 100
kwords: Tabellenkalkulationskonvertierung, REST API, PDF, CSV, JSON, Markdown, Excel Arbeitsblatt
---
Exportieren Sie eine Cloud-Tabelle/einen Bereich vom Typ Excel in eine Formatdatei. Die Formatdatei kann in der Cloud gespeichert oder in den lokalen Speicher exportiert werden.

## **Exportbereich als Format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg|(Erforderlich) Der Name der abzurufenden Arbeitsmappendatei.|
|Arbeitsblatt|Zeichenfolge|Weg|Der Arbeitsblattname von Spreadsheet/Excel|
|Reichweite|Zeichenfolge|Weg|Der zu konvertierende Bereich (z. B. A1:C12).|
|Format|Zeichenfolge|Abfrage|(Erforderlich) Das gewünschte Ausgabeformat (z. B. „png“, „pdf“, „svg“).|
|Ordner|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|Speichername|Zeichenfolge|Abfrage|(Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Wird dieser Name weggelassen, wird standardmäßig der Standardspeicher verwendet.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad für die Ausgabedatei. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Der Name des Ausgabedateispeichers.|
|SchriftartenStandort|Zeichenfolge|Abfrage|Speicherort für benutzerdefinierte Schriftarten.|
|Region|Zeichenfolge|Abfrage|Die Regionseinstellung der Tabelle.|
|Passwort|Zeichenfolge|Abfrage|Das zum Öffnen der Tabellenkalkulationsdatei erforderliche Kennwort.|

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

## Warum sollten Sie den Export-Tabellenkalkulationsbereich als Format API verwenden?

- Sie können Cloud-Dateien jederzeit und überall in verschiedene Formate konvertieren.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich den Export-Tabellenkalkulationsbereich im Format API mit SDKs?

### Exportbereich als Format API Spezifikation

 Der[Exportbereich als Format API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ExportRangeAsFormat) bietet eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt über einen Webbrowser ermöglicht.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen ermöglicht, einen Tabellendatenbereich mit einem kurzen Code in eine Formatdatei zu exportieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
