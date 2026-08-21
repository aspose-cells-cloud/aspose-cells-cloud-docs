---
title: "Zeichen aus entfernter Tabellendatei entfernen"
ArticleTitle: "Zeichen aus entfernter Tabellendatei entfernen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "remove-characters-in-remote-spreadsheet"
type: docs
url: /de/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, Zeichen entfernen, Textverarbeitung"
description: "Löscht benutzerdefinierte Zeichen, vordefinierte Zeichensätze oder beliebige Teilzeichenfolgen aus jeder Zelle des ausgewählten Bereichs, während Formeln, Formatierungen und Datenvalidierungen in einer entfernten Tabellendatei beibehalten werden."
weight: 100
---

## Das Entfernen von Zeichen aus entfernter Tabellendatei mit Aspose.Cells Cloud-Webdiensten

Löscht benutzerdefinierte Zeichen, vordefinierte Zeichensätze oder beliebige Teilzeichenfolgen aus jeder Zelle des ausgewählten Bereichs, während Formeln, Formatierungen und Datenvalidierungen in einer entfernten Tabellendatei beibehalten werden.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername         | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                                          |
|-----------------------|---------|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                  | string  | Path                                | (Erforderlich) Der Name der abzurufenden Arbeitsmappe.                                                                                                                               |
| worksheet             | string  | Path                                | Gibt das Tabellenblatt der Tabellendatei an.                                                                                                                                         |
| range                 | string  | Path                                | Gibt den Bereich des Tabellenblatts an.                                                                                                                                              |
| removeTextMethod      | string  | Query                               | Gibt den Typ der Textentfernungs-Methode an.                                                                                                                                         |
| characterSets         | string  | Query                               | Gibt die Zeichensätze an.                                                                                                                                                            |
| removeCustomValue     | string  | Query                               | Gibt den benutzerdefinierten zu entfernenden Wert an.                                                                                                                                |
| caseSensitive         | boolean | Query                               | Wirkt sich auf den Modus `Substring` und `CustomChars` aus, sofern aktiviert.                                                                                                        |
| folder                | string  | Query                               | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.                                                                                      |
| storageName           | string  | Query                               | (Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Bei Weglassung wird der Standardspeicher verwendet.                                     |
| region                | string  | Query                               | Regionale/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsauswertung und länderspezifisches Verhalten.             |
| password            | string  | Query                               | Das Passwort zum Öffnen der Tabellendatei.                                                                                                                                           |

### Parameter des Anforderungstextes

| Parametername | Typ   | Beschreibung |
| ------------- | ----- | ------------ |
| *None*        | *None* | Dieser Vorgang erfordert keinen Anforderungstext. |

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Zeichen erfolgreich entfernt.",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**Antwort-Statuscodes**

| Code | Bedeutung              | Beschreibung                                                                 |
|------|------------------------|------------------------------------------------------------------------------|
| 200  | OK                     | Die Zeichen wurden erfolgreich entfernt und die Arbeitsmappe aktualisiert. |
| 400  | Bad Request            | Ein oder mehrere Parameter fehlen oder sind ungültig.                      |
| 401  | Unauthorized           | Authentifizierung fehlgeschlagen – fehlender oder ungültiger JWT-Token.    |
| 413  | Payload Too Large      | Die Anforderungsgröße überschreitet das zulässige Limit.                   |
| 500  | Internal Server Error  | Auf Serverseite ist ein unerwarteter Fehler aufgetreten.                   |

## Verwendung des Entfernens von Zeichen aus entfernter Tabellendatei mit SDKs

### Spezifikation: Zeichen aus entfernter Tabellendatei entfernen

Die [API-Spezifikation für „Zeichen aus entfernter Tabellendatei entfernen“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool cURL verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Sichere Verbindung über HTTPS herstellen
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Zeichen erfolgreich entfernt.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Beispiel.xlsx",
      "Path": "/documents/Beispiel.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Verwendung der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---