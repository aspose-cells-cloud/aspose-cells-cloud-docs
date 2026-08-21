---
title: "Aspose.Cells Cloud Replace-Web-API – Text in entfernter Arbeitsmappe aktualisieren"
secondtitle: "Dokument"
ArtikelTitel: "Text in entfernter Arbeitsmappe mit Aspose.Cells Cloud API suchen und ersetzen"
linktitle: "Inhalt entfernter Arbeitsmappe ersetzen"
type: docs
url: /de/replace-content-in-remote-worksheet/
keywords: "Aspose.Cells, Text ersetzen, entfernte Arbeitsmappe, Excel-API, Cloud-Tabellendokument, suchen und ersetzen, REST-API"
description: "Ersetzen Sie Text in einer bestimmten Arbeitsmappe einer Excel-Datei, die in Aspose Cloud gespeichert ist. Unterstützt passwortgeschützte Arbeitsmappen, regionsbewusste Suche und Massenaktualisierungen."
weight: 100
---

Ersetzen Sie angegebenen Text innerhalb einer bestimmten Arbeitsmappe entfernter Excel-Dateien. Aktualisieren Sie den Inhalt gezielter Tabellenblätter effizient mithilfe der Aspose.Cells-Such- und-Ersetzen-API für präzise Bearbeitung von Arbeitsmappen.

## **Ersetzen des Inhalts in entfernter Arbeitsmappe – API**

### **Web-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anfrageparameter**

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                                 |
| :-------------- | :----- | :--------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name            | String | Pfad                               | Der Name der Arbeitsmappe, die in der Cloud-Speicherung gespeichert ist und bearbeitet werden soll (z. B. `"sales_report.xlsx"`, `"budget_2024.xls"`).                     |
| worksheet       | String | Pfad                               | Der Name des spezifischen Tabellenblatts, in dem die Suchen-und-Ersetzen-Operation durchgeführt werden soll (z. B. `"Q1_Sales"`, `"Sheet1"`).                               |
| searchText      | String | Abfrage                            | Der Suchtext, der im angegebenen Tabellenblatt gesucht werden soll. Die Suche gilt für alle Zellen im Tabellenblatt, sofern nicht weiter eingeschränkt.                      |
| replaceText     | String | Abfrage                            | Der Text, der alle Vorkommen von `searchText` im angegebenen Tabellenblatt ersetzen wird.                                                                                  |
| folder          | String | Abfrage                            | Der Pfad des Cloud-Speicherordners, in dem sich die Quellarbeitsmappe befindet (z. B. `"/reports/monthly/"`, `"/finance/"`).                                                 |
| storageName     | String | Abfrage                            | _(Optional)_ Der Name des benutzerdefinierten Cloud-Speichers (z. B. `"CorporateS3"`, `"AzureArchive"`). Falls nicht angegeben, wird der Standard-Cloud-Speicher für Ihr Konto verwendet. |
| region          | String | Abfrage                            | _(Optional)_ Legt die Lokalisierung für die Textverarbeitung fest, was sich auf die Zeichencodierung und die sprachspezifische Suchfunktion im Tabellenblatt auswirken kann (z. B. `"de-DE"`, `"fr-FR"`). |
| password        | String | Abfrage                            | _(Optional)_ Falls die Arbeitsmappe passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu bearbeiten.                                              |

**Beispielanfrage (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/sales_report.xlsx/worksheets/Sheet1/replace/content?searchText=OldValue&replaceText=NewValue&folder=/reports" \
     -H "Authorization: Bearer {access_token}"
```

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### **Fehlercodes**

| Code | Beschreibung                             | Eintrittsfall                                                     |
|------|------------------------------------------|-------------------------------------------------------------------|
| 400  | Bad Request (Ungültige Anfrage)          | Die Anfrage-URI ist fehlerhaft oder erforderliche Parameter fehlen. |
| 401  | Unauthorized (Nicht autorisiert)         | Zugriffstoken fehlt, ist ungültig oder die Clientanmeldedaten sind falsch. |
| 404  | Not Found (Nicht gefunden)               | Die angegebene Arbeitsmappe oder das angegebene Tabellenblatt kann nicht gefunden werden. |
| 500  | Internal Server Error (Interner Serverfehler) | Beim Verarbeiten der Anfrage ist ein unerwarteter Fehler aufgetreten. |

## Wofür sollte die Ersetzung des Tabellenblattinhalts in entfernten Tabellendokumenten per API verwendet werden?

- **Batch-Cloud-Dateiaktualisierung**: Ändern Sie den Inhalt mehrerer Excel-Dateien, die in Cloud-Speicherdiensten wie AWS S3 und Azure Blob gespeichert sind.
- **Dynamische Befüllung von Cloud-Vorlagen**: Batch-Befüllung dynamischer Daten für in der Cloud gespeicherte Berichtsvorlagen.
- **Überregionsdateisynchronisierung**: Synchronisieren Sie die Inhaltskonsistenz von Excel-Dateien in Cloud-Speicherdiensten über verschiedene geografische Regionen hinweg.

## Warum sollten Sie die Ersetzung des Tabellenblattinhalts in entfernten Tabellendokumenten per API verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen an, was eine schnelle Entwicklung ermöglicht, und wird mit umfassender Dokumentation geliefert. Im Vergleich zum Aufbau eigener Diagramm-Renderlösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Geringere Personalkosten**: Reduziert den Bedarf an Mitarbeitern für die Zusammenstellung von Dokumenten.
- **Pay-per-use (Bezahlen nach Verbrauch)**: Keine Vorabinvestition; Sie zahlen nur für tatsächlich genutzte API-Aufrufe.
- **Keine Wartungskosten**: Keine Notwendigkeit, Server zu warten, Software zu aktualisieren oder Kompatibilitätsprobleme zu bearbeiten.

## Wie Sie die Ersetzung des Tabellenblattinhalts in entfernten Tabellendokumenten per API mit SDKs verwenden

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Ersetzung des Tabellenblattinhalts in Tabellendokumenten mit minimalem Codeaufwand implementieren können.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs mit Aspose.Cells-Webdiensten interagieren:
---