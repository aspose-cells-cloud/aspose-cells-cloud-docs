---
title: Aspose.Cells Cloud Web API – Konvertieren Sie Tabellendaten einer Kalkulationstabelle in eine JSON-Datei
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Json file
linktitle: Tabelle in JSO konvertieren
type: docs
url: /de/convert-table-to-json/
keywords: Excel API, JSON conversion, spreadsheet to JSON, cloud file conversion, REST API, Aspose.Cell
description: Konvertieren Sie eine lokale Tabellenkalkulationstabelle effizient in das JSON-Format mithilfe von Excel API. Diese Methode ermöglicht eine nahtlose Dateiverarbeitung ohne Cloud-Speicher
weight: 100
kwords: Excel API, JSON-Konvertierung, Cloud-Dateikonvertierung, Tabellenkalkulation, REST API, Aspose.Cells, lokale Laufwerksverarbeitung, Dateiformatkonvertierung
---
Konvertieren Sie eine lokale Kalkulationstabelle/Excel-Tabelle mit dem Aspose.Cells Cloud Web API in eine JSON-Datei.

## **Tabelle in Json konvertieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|-------------|-|-----------------------|----------------------------------------------|
| Kalkulationstabelle| Datei| FormData| Laden Sie die Tabellenkalkulationsdatei hoch.|
| Arbeitsblatt|Zeichenfolge| Abfrage| Geben Sie den Arbeitsblattnamen der Tabelle an.|
| Tabellenname|Zeichenfolge| Abfrage| Geben Sie den Namen der zu konvertierenden Tabelle an.|
| Ausgangspfad|Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist; der Standardwert ist null.|
| outStorageName|Zeichenfolge| Abfrage| Geben Sie den Speichernamen der Ausgabedatei an.|
| SchriftartenStandort|Zeichenfolge| Abfrage| Verwenden Sie für die Konvertierung benutzerdefinierte Schriftarten.|
| Region|Zeichenfolge| Abfrage|Definieren Sie die Regionseinstellungen für die Tabelle.|
| Passwort|Zeichenfolge| Abfrage| Das zum Öffnen der Tabellenkalkulationsdatei erforderliche Kennwort.|

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

## Warum sollten Sie die Konvertierung von Tabellen in JSON API verwenden?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Konvertierungstabelle in JSON API mit SDKs?

### Tabelle in Json konvertieren API Spezifikation

 Der[Tabelle in Json konvertieren API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToJson) bietet eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt über einen Webbrowser ermöglicht.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, Tabellendaten einer Kalkulationstabelle mit einem kurzen Code in eine JSON-Datei zu konvertieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs mit Aspose.Cells-Webdiensten interagieren:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}
{{< /tab >}}
{{< /tabs >}}
