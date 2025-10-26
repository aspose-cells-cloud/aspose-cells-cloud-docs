---
title: Aspose.Cells Cloud Web API - Inhalt in Remote-Tabelle ersetzen
second_title: Documen
ArticleTitle: Replace Content in Remote a Spreadshee
linktitle: Ersetzen Sie den Inhalt der Remote-Tabelle
type: docs
url: /de/replace-content-in-remote-spreadsheet/
keywords: Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacemen
description: Ersetzen Sie effizient Text in Remote-Tabellen mit Excel API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Inhalt ersetzen in Excel, Cloud-basierter Textersatz, Text in Remote-Tabelle ändern
---
Ersetzen Sie angegebenen Text effizient in einer Remote-Tabellenkalkulationsdatei.

## **Inhalt in Remote-Tabelle ersetzen API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| Der Name der zu ändernden Arbeitsmappendatei.|
| Suchtext| Zeichenfolge| Abfrage| Der Text, nach dem in der Tabelle gesucht werden soll.|
| replaceText| Zeichenfolge| Abfrage| Der Text, der die gefundenen Vorkommen ersetzen soll.|
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

## Wo sollten wir den Inhalt „Ersetzen“ in der Remote-Tabelle API verwenden?

Wenn Sie Inhalte in einer Remote-Tabelle ersetzen müssen, können Sie diese API verwenden.

## Warum sollten Sie den Inhalt in der Remote-Tabelle API ersetzen?

- Ersetzen Sie Inhalte in Remote-Tabellen schnell.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie den Inhalt in der Remote-Tabelle API mit SDKs ersetzen

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen, Inhalte in Tabellenkalkulationen für Zellen mit minimalem Code einfach zu ersetzen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
