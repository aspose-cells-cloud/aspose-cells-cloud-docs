---
title: "Aspose.Cells Cloud Excel Textsuche Web-API – Text in entferntem Arbeitsblatt finden"
second_title: "Dokument"
ArticleTitle: "Text in entfernter Excel-Tabellendatei suchen – Spezifische Daten finden"
linktitle: "Inhalte entfernter Arbeitsblätter durchsuchen"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Aspose Cells, Excel API, Textsuche, entferntes Arbeitsblatt"
description: "Suchen Sie mit der Aspose.Cells Cloud API nach Text, Zahlen oder Formeln in einem entfernten Excel-Arbeitsblatt. Unterstützt groß-/kleinschreibungsunabhängige Suche und passwortgeschützte Dateien."
weight: 100
---

## **Inhalte im entfernten Arbeitsblatt durchsuchen**

Suchen Sie programmgesteuert nach spezifischem Text in beliebigen Excel-Arbeitsblättern mithilfe der Aspose.Cells Cloud API. Der Dienst kann Text, Zahlen oder Formeln in entfernten Dateien finden, die in einer Cloud-Speicherung gespeichert sind, und so automatisierte Workflows für Datenentdeckung, Inhaltsanalyse und Prüfung von Tabellenkalkulationen ermöglichen.

### **Web-API**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter**

| Parametername   | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                      |
| --------------- | ------- | ---------------------------------- | ------------------------------------------------------------------------------------------------- |
| name            | String  | Pfad                               | **Erforderlich.** Der Dateiname der Zielarbeitsmappe (z. B. `jahresbericht.xlsx`).               |
| worksheet       | String  | Pfad                               | **Erforderlich.** Das Arbeitsblatt innerhalb der Arbeitsmappe, in dem die Suche erfolgt.         |
| searchText      | String  | Abfrage                            | **Erforderlich.** Der genaue Text oder die Zahl, die gesucht werden soll.                        |
| ignoreCase      | Boolean | Abfrage                            | **Optional.** Wenn `true`, erfolgt die Suche groß-/kleinschreibungsunabhängig. Standard ist `false`. |
| folder          | String  | Abfrage                            | **Optional.** Pfad zum Ordner, der die Arbeitsmappe enthält. Falls nicht angegeben, wird das Stammverzeichnis verwendet. |
| storageName     | String  | Abfrage                            | **Optional.** Name einer benutzerdefinierten Cloud-Speicherung. Falls nicht angegeben, wird die Standard-Speicherung verwendet. |
| region          | String  | Abfrage                            | **Optional.** Gebietsschema-Einstellung (z. B. `de-DE`), die die Textvergleichung beeinflussen kann. |
| password        | String  | Abfrage                            | **Optional.** Passwort für eine geschützte Arbeitsmappe. Weglassen, falls die Datei nicht verschlüsselt ist. |

### **Antwort**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Gesamt",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Gesamt",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** – Array von Treffern. Jedes Element enthält die Zelladresse (`cellName`), den gefundenen Text (`text`) und wie oft er in dieser Zelle vorkommt (`occurrences`).
- **code** – vom Dienst zurückgegebener HTTP-Statuscode.
- **status** – Textuelle Beschreibung des Ergebnisses.

### **Fehlercodes**

- **400 Bad Request** – Ungültige API-URI oder fehlerhafte Parameter.
- **401 Unauthorized** – Fehlender oder ungültiger OAuth 2.0-Token.
- **404 Not Found** – Die Arbeitsmappe oder das Arbeitsblatt kann nicht gefunden werden.
- **500 Server Error** – Beim Verarbeiten der Anfrage ist ein unerwarteter Fehler aufgetreten.

## Wofür sollte die Suche nach Inhalten im Arbeitsblatt der Spreadsheet API verwendet werden?

- **Compliance-Audit der Arbeitsmappe:** Finden Sie schnell sensible Begriffe (z. B. „Vertraulich“) in der gesamten Datei.
- **Datenverknüpfung über Arbeitsblätter hinweg:** Suchen Sie eine Projektnummer oder einen Kundennamen, der auf mehreren Arbeitsblättern vorkommt.
- **Vorlagenverifikation:** Bestätigen Sie nach der Erstellung von Berichten, dass Platzhalter wie `{{Date}}` ersetzt wurden.
- **Historische Datenanalyse:** Suchen Sie in veralteten Tabellenkalkulationen nach spezifischen Ereigniscodes, um frühere Geschäftslogik zu verstehen.

## Warum sollte man die Suche nach Inhalten im Arbeitsblatt der Spreadsheet API verwenden?

- **Entwicklerfreundlich:** SDKs für viele Programmiersprachen beschleunigen die Entwicklung und sind vollständig dokumentiert.
- **Geringere Arbeitskosten:** Reduziert den Bedarf an Mitarbeitern für manuelle Datenaufbereitung.
- **Pay-per-Use:** Sie zahlen nur für die tatsächlich getätigten API-Aufrufe.
- **Kein Wartungsaufwand:** Keine Server zu verwalten, keine Softwareupdates und keine Kompatibilitätsprobleme.
- **Beibehaltung komplexer Excel-Formatierung** beim Exportieren der Ergebnisse in PDF oder andere Formate.

## Wie verwendet man die Suche nach defekten Links im Arbeitsblatt der Spreadsheet API mit SDKs?

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Suche nach Inhalten im Arbeitsblatt von Tabellenkalkulationen mit minimalem Codeaufwand implementieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.