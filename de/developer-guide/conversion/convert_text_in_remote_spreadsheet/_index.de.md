---
title: "Text in Remote Spreadsheet konvertieren"
ArticleTitle: "Text in Remote Spreadsheet konvertieren – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Text in Remote Spreadsheet konvertieren"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, Textkonvertierung, API"
description: "Konvertiert Text in einem angegebenen Bereich eines Arbeitsblatts, einschließlich Zahlenkonvertierung, Zeichenersetzung, Zeilenumbruchbehandlung und Normalisierung von accented Zeichen."
weight: 1000
---

## Die Textkonvertierung in Remote Spreadsheet von Aspose.Cells Cloud-Webdiensten

Gibt an, dass Zahlen, die als Text gespeichert sind, in das korrekte Zahlenformat konvertiert werden, unerwünschte Zeichen und Zeilenumbrüche durch gewünschte Zeichen ersetzt werden und accented Zeichen in ihre äquivalenten Zeichen ohne Akzente umgewandelt werden.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|------------------|--------|-----------------------------------|--------------|
| name             | string | Pfad | (Erforderlich) Der Name der abzurufenden Arbeitsmappe. |
| worksheet        | string | Pfad | Gibt das Arbeitsblatt der Tabelle an. |
| range            | string | Pfad | Gibt den Bereich des Arbeitsblatts an. |
| convertTextType  | string | Abfrage | Gibt den Typ der Textkonvertierung an. (Erforderlich) |
| sourceCharacters | string | Abfrage | Gibt die Quellzeichen an. (Optional) |
| targetCharacters | string | Abfrage | Gibt die Zielzeichen an. (Optional) |
| folder           | string | Abfrage | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. |
| storageName      | string | Abfrage | (Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Bei Weglassung wird der Standardspeicher verwendet. |
| region           | string | Abfrage | Regionale/Spracheinstellung der Tabelle (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsauswertung und länderspezifisches Verhalten. (Optional) |
| password         | string | Abfrage | Das Passwort zum Öffnen der Tabellendatei. (Optional) |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| - | - | - |

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Textkonvertierung erfolgreich abgeschlossen.",
  "Data": {
    // Details zum Konvertierungsergebnis, z. B. Anzahl der aktualisierten Zellen, können hier hinzugefügt werden.
  }
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die Textkonvertierung wurde erfolgreich abgeschlossen. |
| 400 | Bad Request | Die Anfrage war fehlerhaft formatiert oder es fehlten erforderliche Parameter. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder JWT-Token fehlt/ungültig. |
| 413 | Payload Too Large | Die Anforderungsnutzlast überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

## Verwendung der Textkonvertierung in Remote Spreadsheet mit SDKs

### Spezifikation der Textkonvertierung in Remote Spreadsheet

Die [API-Spezifikation für Textkonvertierung in Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# HTTPS für eine sichere Verbindung verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
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
  "Message": "Textkonvertierung erfolgreich abgeschlossen.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "Zahlen konvertiert, Zeichen ersetzt, Zeilenumbrüche normalisiert."
  }
}
```

{< /tab >}

{< /tabs >}

### Verwendung von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Weitere Informationen zu den verfügbaren Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
 `[TBD]`
---