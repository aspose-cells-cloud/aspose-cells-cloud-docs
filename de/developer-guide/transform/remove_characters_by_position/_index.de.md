---
title: "Zeichen nach Position entfernen"
ArticleTitle: "Zeichen nach Position entfernen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Zeichen nach Position entfernen"
type: docs
url: /cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, Zeichen entfernen, API"
description: "Löscht Zeichen aus Zellen nach Position in einer Tabellenkalkulation."
weight: 100
---

## Das „Zeichen nach Position entfernen“-Verfahren von Aspose.Cells Cloud-Webdiensten

Entfernt Zeichen aus jeder Zelle im Zielbereich nach Position (erste/letzte N Zeichen, vor/nach einem Teilzeichenfolge oder zwischen zwei Trennzeichen), während Formeln, Formatierungen und Datenvalidierungen erhalten bleiben.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername             | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                         |
|---------------------------|---------|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | Datei   | FormData                           | Hochladen der Tabellenkalkulationsdatei.                                                                           |
| theFirstNCharacters       | Integer | Abfrage                            | Gibt an, die ersten n Zeichen aus ausgewählten Zellen zu entfernen. Optional.                                      |
| theLastNCharacters        | Integer | Abfrage                            | Gibt an, die letzten n Zeichen aus ausgewählten Zellen zu entfernen. Optional.                                     |
| allCharactersBeforeText   | String  | Abfrage                            | Entfernt Text, der vor einer bestimmten Teilzeichenfolge steht. Optional.                                          |
| allCharactersAfterText    | String  | Abfrage                            | Entfernt Text, der nach einer bestimmten Teilzeichenfolge steht. Optional.                                         |
| caseSensitive             | Boolean | Abfrage                            | Beeinflusst den Modus „Substring“ und „CustomChars“, wenn aktiviert. Optional.                                     |
| worksheet                 | String  | Abfrage                            | Gibt das Tabellenblatt der Tabellenkalkulation an. Optional.                                                       |
| range                     | String  | Abfrage                            | Gibt den Tabellenblattbereich der Tabellenkalkulation an (z. B. `A1:B10`). Optional.                               |
| outPath                   | String  | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. Optional.               |
| outStorageName            | String  | Abfrage                            | Name des Ausgabespeichers. Optional.                                                                               |
| region                    | String  | Abfrage                            | Region-/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `en-US`, `fr-FR`). Optional.                     |
| password                  | String  | Abfrage                            | Das Passwort zum Öffnen der Tabellenkalkulationsdatei. Optional.                                                   |

### Anforderungstextparameter

| Parametername | Typ  | Beschreibung                    |
| -------------- | ---- | ------------------------------- |
| Spreadsheet    | Datei | Hochladen der Tabellenkalkulationsdatei. |

### **Antwort**

```json
{
  "status": "OK",
  "message": "Zeichen erfolgreich entfernt.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Der Vorgang wurde erfolgreich abgeschlossen, und die verarbeitete Datei wird zurückgegeben. |
| 400 | Bad Request | Die Anfrage ist fehlerhaft oder enthält ungültige Parameter. |
| 401 | Unauthorized | Die Authentifizierung ist fehlgeschlagen oder das JWT-Token fehlt/ist ungültig. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Auf der Serverseite ist ein unerwarteter Fehler aufgetreten. |

## So verwenden Sie „Zeichen nach Position entfernen“ mit SDKs

### Spezifikation für „Zeichen nach Position entfernen“

Die [Spezifikation der „Zeichen nach Position entfernen“-API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# HTTPS für eine sichere Verbindung verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "Zeichen erfolgreich entfernt.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Verwenden von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert niedrigere Details, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---