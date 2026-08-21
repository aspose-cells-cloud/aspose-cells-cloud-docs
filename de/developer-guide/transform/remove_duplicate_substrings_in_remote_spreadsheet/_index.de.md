---
title: "Doppelte Teilzeichenfolgen in entfernter Tabellendatei entfernen"
ArticleTitle: "Doppelte Teilzeichenfolgen in entfernter Tabellendatei entfernen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Doppelte Teilzeichenfolgen in entfernter Tabellendatei entfernen"
type: docs
url: /de/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, Doppelte Teilzeichenfolgen entfernen, API"
description: "API zum Finden und Entfernen wiederholter Teilzeichenfolgen innerhalb von Zellen eines angegebenen Bereichs in einer Arbeitsmappe."
weight: 1
---

## Entfernen doppelter Teilzeichenfolgen in entfernter Tabellendatei mit Aspose.Cells Cloud-Webdiensten

Findet und entfernt wiederholte Teilzeichenfolgen in jeder Zelle des gewählten Bereichs unter Verwendung benutzerdefinierter oder vordefinierter Trennzeichen, wobei Formeln, Formatierungen und Datenvalidierungen erhalten bleiben.

**Wie Duplikate erkannt werden**  
1. Jeder Zellwert wird mithilfe der gewählten Trennzeichen in Teilzeichenfolgen aufgeteilt.  
2. Das Tool vergleicht Teilzeichenfolgen **innerhalb derselben Zelle** und behält nur die **erste Vorkommensart** jedes Duplikats bei.  
3. Die bereinigten Teilzeichenfolgen werden wieder mit denselben Trennzeichen verbunden und in die Zelle zurückgeschrieben.  

**Optionen für Trennzeichen**  
- Vordefinierte Liste: Komma, Semikolon, Leerzeichen, Tabulator, Zeilenumbruch  
- `Custom` – geben Sie beliebige Zeichen ein; mehrere Zeichen werden als ein zusammengefasstes Trennzeichen behandelt  
- `TreatConsecutiveDelimitersAsOne` – fügt benachbarte Trennzeichen zu einem einzigen Separator zusammen  

Nur Zellen mit Zeichentyp werden verarbeitet; Zahlen, boolesche Werte und Formeln werden vor dem Aufteilen in Zeichenfolgen umgewandelt (Formeln gehen dabei verloren). Gibt die Anzahl der bereinigten Zellen sowie den aktualisierten Arbeitsmappen-Stream zurück.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|---------------|--------|------------------------------------|--------------|
| name | string | Pfad | (Erforderlich) Der Name der Arbeitsmappendatei, die abgerufen werden soll. |
| worksheet | string | Pfad | Gibt das Tabellenblatt der Tabellendatei an. |
| range | string | Pfad | Gibt den Tabellenblattbereich der Tabellendatei an. |
| delimiters | string | Abfrage | Trennzeichen zur Aufteilung von Zellwerten (z. B. Komma, Semikolon, Leerzeichen, Tabulator, Zeilenumbruch). Erforderlich. |
| treatConsecutiveDelimitersAsOne | boolean | Abfrage | Fügt benachbarte Trennzeichen zu einem einzigen Separator zusammen. Standardwert: true. Optional. |
| caseSensitive | boolean | Abfrage | Führt eine groß-/kleinschreibungsabhängige Vergleichung bei der Erkennung von Duplikaten durch. Optional. |
| folder | string | Abfrage | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert: null. |
| storageName | string | Abfrage | (Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. |
| region | string | Abfrage | Regionale/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Optional. |
| password | string | Abfrage | Das Passwort zum Öffnen der Tabellendatei. Optional. |

### Parameter im Anforderungstext

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| - | - | Für diesen Vorgang ist kein Anforderungstext erforderlich. |

### **Antwort**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-codierter Arbeitsmappen-Stream"
}
```

**HTTP-Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Vorgang erfolgreich; gibt die Anzahl der bereinigten Zellen sowie den aktualisierten Arbeitsmappen-Stream zurück. |
| 400 | Bad Request | Ein oder mehrere Anforderungsparameter fehlen oder sind ungültig. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder JWT-Token fehlt/ungültig. |
| 413 | Payload Too Large | Die Anforderung überschreitet die zulässigen Größenbegrenzungen. |
| 500 | Internal Server Error | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

## Verwendung von „Doppelte Teilzeichenfolgen in entfernter Tabellendatei entfernen“ mit SDKs

### Spezifikation für „Doppelte Teilzeichenfolgen in entfernter Tabellendatei entfernen“

Die [API-Spezifikation für „Doppelte Teilzeichenfolgen in entfernter Tabellendatei entfernen“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}
{< tab tabNum="1" >}
```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-codierter Arbeitsmappen-Stream"
}
```
{< /tab >}
{< /tabs >}

### Verwendung von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Bitte prüfen Sie den <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---