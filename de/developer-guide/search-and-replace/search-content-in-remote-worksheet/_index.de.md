---
title: Aspose.Cells Cloud Web API - Arbeitsblattinhalt in Remote-Tabellen suchen
second_title: Documen
ArticleTitle: Search Worksheet Content in Remote Spreadshee
linktitle: Inhalt des Remote-Arbeitsblatts suchen
type: docs
url: /de/search-content-in-remote-worksheet/
keywords: Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet AP
description: Effiziente Suche nach Text in einem Arbeitsblatt einer Remote-Tabelle, die in der Cloud gespeichert ist
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen, Remote-Arbeitsblattsuche
---
Suchen Sie nach einem bestimmten Text in einem Arbeitsblatt einer Remote-Tabelle, die im Cloud-Speicher gespeichert ist.

## **Schnittstellendetails**

## **Inhalt im Remote-Arbeitsblatt suchen**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg|Der Name der zu durchsuchenden Arbeitsmappendatei.|
|Arbeitsblatt|Zeichenfolge|Weg|Der Name des Arbeitsblatts.|
|Suchtext|Zeichenfolge|Abfrage|Der zu durchsuchende Text.|
|Groß-/Kleinschreibung ignorieren|Boolescher Wert|Abfrage|Gibt an, ob die Groß-/Kleinschreibung während der Suche ignoriert werden soll.|
|Ordner|Zeichenfolge|Abfrage|Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist.|
|Speichername|Zeichenfolge|Abfrage|(Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Wenn dieser Name weggelassen wird, wird der Standardspeicher verwendet.|
|Region|Zeichenfolge|Abfrage|Die Tabellenbereichseinstellung.|
|Passwort|Zeichenfolge|Abfrage|Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

### **Antwort**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
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

## Wo sollten wir den Suchinhalt im Arbeitsblatt der Tabelle API verwenden?

Wenn Sie im Arbeitsblatt einer Tabelle nach Inhalten suchen müssen, können Sie diese Nummer API verwenden.

## Warum sollten Sie den Suchinhalt im Arbeitsblatt der Tabelle API verwenden?

- Mit diesem API können Sie mühelos Inhalte in einem Remote-Tabellenblatt suchen.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Suche nach defekten Links im Arbeitsblatt der Tabelle API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen die einfache Implementierung von Suchinhalten in Arbeitsblättern oder Tabellen für Zellen mit minimalem Code.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
