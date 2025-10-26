---
title: Aspose.Cells Cloud Web API - Arbeitsblattinhalt in Remote-Tabelle ersetzen
second_title: Documen
ArticleTitle: Replace Worksheet Content in Remote a Spreadshee
linktitle: Ersetzen Sie den Inhalt des Remote-Arbeitsblatts
type: docs
url: /de/replace-content-in-remote-worksheet/
keywords: Aspose.Cells Cloud Web API, Replace Content, Remote Worksheet, Cloud Spreadsheet, Text Replacement, Office Cloud Integratio
description: Ersetzen Sie effizient Text im Arbeitsblatt einer Remote-Tabelle mit Aspose.Cells API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen, ReplaceContentInRemoteWorksheet
---
Ersetzen Sie effizient angegebenen Text in einem Arbeitsblatt einer Remote-Tabellenkalkulationsdatei.

## **Inhalt im Remote-Arbeitsblatt ersetzen API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| Der Name der zu ändernden Arbeitsmappendatei.|
| Arbeitsblatt| Zeichenfolge| Weg| Geben Sie das Arbeitsblatt für den Ersatz an.|
| Suchtext| Zeichenfolge| Abfrage| Der Text, nach dem im Arbeitsblatt gesucht werden soll.|
| replaceText| Zeichenfolge| Abfrage| Der Text, durch den der gesuchte Text ersetzt werden soll.|
| Ordner| Zeichenfolge| Abfrage| Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist.|
| Speichername| Zeichenfolge| Abfrage|(Optional) Der Name des Speichers, wenn benutzerdefinierter Cloud-Speicher verwendet wird. Wenn dieser Name weggelassen wird, verwenden Sie den Standardspeicher.|
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

## Wo sollten wir den Inhalt des Arbeitsblatts in der Remote-Tabelle API ersetzen?

Wenn Sie den Inhalt eines Arbeitsblatts in einer Remote-Tabelle ersetzen müssen, können Sie API verwenden.

## Warum sollten Sie den Inhalt des Arbeitsblatts in der Remote-Tabelle API ersetzen?

- Ersetzen Sie schnell den Inhalt des Arbeitsblatts in Remote-Tabellen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie den Inhalt des Arbeitsblatts in Remote Spreadsheet API mit SDKs ersetzen

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen, den Inhalt von Arbeitsblättern in Tabellenkalkulationen mit minimalem Code einfach für Zellen zu ersetzen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen die Interaktion mit Aspose.Cells-Webdiensten mithilfe verschiedener SDKs:
