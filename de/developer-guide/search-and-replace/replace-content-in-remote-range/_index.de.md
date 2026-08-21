---
title: "Aspose.Cells Cloud Replace Web API – Text in Remote Spreadsheet Range aktualisieren"
second_title: "Dokumentation"
ArticleTitle: "Massenhaftes Ersetzen von Text in Cloud-Excel-Dateien – Find & Replace API"
linktitle: "Inhalt entfernter Bereiche ersetzen"
type: docs
url: /replace-content-in-remote-range/
keywords: "Text in entferntem Excel-Bereich ersetzen, Aspose.Cells Cloud API, Excel finden und ersetzen, Cloud-Tabelleneditor, entfernte Excel-Datei aktualisieren"
description: "Verwenden Sie Aspose.Cells Cloud, um Text in einem bestimmten Bereich einer entfernten Excel-Datei zu suchen und zu ersetzen. Unterstützt Authentifizierung, Fehlerbehandlung und mehrsprachige SDKs."
weight: 100
---

Führen Sie massenhaftes Ersetzen von Texten in entfernten Excel-Dateien durch, die in der Cloud gespeichert sind. Suchen und aktualisieren Sie gezielt Textzeichenfolgen innerhalb ausgewählter Bereiche effizient mithilfe der Aspose.Cells Find & Replace API.

## **Inhalt in entferntem Bereich ersetzen – API**

### Web-API

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter**

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                 |
| :------------ | :---- | :------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | Pfad                             | Der Name der Arbeitsmappe, die in der Cloud gespeichert ist und bearbeitet werden soll (z. B. `"report.xlsx"`).                                            |
| searchText    | String | Abfrage                          | Die Zeichenfolge, die im angegebenen Arbeitsblatt und Zellbereich gesucht werden soll. Unterstützt exakte Textübereinstimmung.                              |
| replaceText   | String | Abfrage                          | Die Zeichenfolge, die alle Vorkommen von `searchText` im angegebenen Bereich ersetzen soll.                                                                |
| worksheet     | String | Pfad                             | Der Name des Arbeitsblatts, in dem der Find- und Replace-Vorgang durchgeführt wird.                                                                         |
| cellArea      | String | Pfad                             | Der spezifische Zellbereich (z. B. `"A1:D20"`), in dem die Textsuche und -ersetzung erfolgt.                                                                |
| folder        | String | Abfrage                          | Der Pfad des Cloud-Speicherordners, in dem sich die Quell-Arbeitsmappe befindet.                                                                            |
| storageName   | String | Abfrage                          | _(Optional)_ Der Name des Cloud-Speichers, in dem sich die Arbeitsmappe befindet. Falls weggelassen, wird der Standard-Cloud-Speicher verwendet.           |
| region        | String | Abfrage                          | _(Optional)_ Legt die Locale für die Textverarbeitung fest, was sich auf die Groß-/Kleinschreibung und Zeichencodierung bei Suchvorgängen auswirken kann (z. B. `"de-DE"`, `"en-US"`). |
| password      | String | Abfrage                          | _(Optional)_ Falls die Arbeitsmappe passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu bearbeiten.                             |

### **Antwort**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

Ein erfolgreicher Aufruf gibt die folgende konkrete JSON-Payload zurück:

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### Fehlercodes

| Code | Nachricht     | Wann auftritt                                        |
| ---- | ------------- | ---------------------------------------------------- |
| 400  | Bad Request   | Die Anforderungs-URI oder -Parameter sind fehlerhaft. |
| 401  | Unauthorized  | Fehlender oder ungültiger Authentifizierungstoken.  |
| 404  | Not Found     | Die angegebene Arbeitsmappe konnte nicht gefunden oder aufgerufen werden. |
| 500  | Server Error  | Ein interner Serverfehler während der Verarbeitung der Arbeitsmappe. |

## Wofür sollte die Replace Content of Range in Remote Spreadsheet API verwendet werden?

- **Batch-Cloud-Datei-Aktualisierung**: Ändern Sie den Inhalt mehrerer Excel-Dateien, die in Cloud-Speichern wie AWS S3 oder Azure Blob gespeichert sind.
- **Dynamische Befüllung von Cloud-Templates**: Batch-Befüllung dynamischer Daten für Berichtsvorlagen, die in der Cloud gespeichert sind.
- **Überregionsdateisynchronisierung**: Synchronisieren Sie die Inhaltskonsistenz von Excel-Dateien in Cloud-Speichern über verschiedene geografische Regionen hinweg.

## Warum sollte man die Replace Content of Range in Remote Spreadsheet API verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, was eine schnelle Entwicklung und umfassende Dokumentation ermöglicht. Im Vergleich zur Erstellung benutzerdefinierter Lösungen reduziert dies die Entwicklungsarbeit erheblich.
- **Kostensenkung**: Reduziert den Bedarf an speziellen Positionen für die Dokumentenkonsolidierung.
- **Pay-per-Use**: Keine Vorabinvestition; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.
- **Keine Wartungskosten**: Keine Notwendigkeit, Server zu warten, Software zu aktualisieren oder Kompatibilitätsprobleme zu lösen.
- **Beibehaltung komplexer Excel-Formatierung** in einem universell zugänglichen PDF-Format.

## Verwendung der Replace Content of Range in Remote Spreadsheet API mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie das Ersetzen von Inhalten in Tabellenblättern mit minimalem Codeaufwand umsetzen können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}