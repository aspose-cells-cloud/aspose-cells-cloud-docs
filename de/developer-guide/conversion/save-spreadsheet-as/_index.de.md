---
title: Aspose.Cells Cloud Web API - Tabelle als Formatdatei speichern
second_title: Documen
ArticleTitle: Save Spreadsheet as a Format fil
linktitle: Tabelle speichern a
type: docs
url: /de/save-spreadsheet-as/
keywords: spreadsheet conversion, Save as, Excel to PDF, Excel to CSV, RES
description: Konvertieren Sie mühelos in der Cloud gespeicherte Tabellenkalkulationen in verschiedene Formate, einschließlich XLSX, PDF und CSV, mit unserem robusten API
weight: 100
kwords: Excel API, Office Cloud, REST, Tabellenkalkulation, PDF, CSV, JSON, Markdown, konvertieren Excel Dateien, Tabellenkalkulation speichern unter, Aspose.Cells Cloud Web AP
---
Speichern Sie eine Cloud-Tabellenkalkulationsdatei/Excel als Formatdatei im Cloud-Speicher.

## **Tabelle speichern unter API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| (Erforderlich) Der Name der zu konvertierenden Arbeitsmappendatei.|
| Format| Zeichenfolge| Abfrage| (Erforderlich) Das gewünschte Ausgabeformat (z. B. „Xlsx“, „Pdf“, „Csv“).|
| saveOptionsData| Klasse| Körper| (Optional) Optionsdaten speichern. Der Standardwert ist null.|
| Ordner| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
| Speichername| Zeichenfolge| Abfrage|(Optional) Der Name des Speichers, wenn benutzerdefinierter Cloud-Speicher verwendet wird. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Speichername der Ausgabedatei.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Verwenden Sie benutzerdefinierte Schriftarten.|
| Region| Zeichenfolge| Abfrage| Die Tabellenbereichseinstellung.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

### **Antwort**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Warum sollten Sie den Save Spread API verwenden?

- Sie können Cloud-Dateien jederzeit und überall in verschiedene Formate konvertieren.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Konvertierungstabelle in JSON API mit SDKs?

### Tabelle als API-Spezifikation speichern

 Der[Tabelle als API-Spezifikation speichern](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, eine Tabelle als Formatdatei mit kurzem Code zu speichern.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{< /tab >}}
{{< /tabs >}}
