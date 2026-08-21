---
title: "Leere Zeilen in Tabellenkalkulation entfernen"
ArticleTitle: "Leere Zeilen in Tabellenkalkulation entfernen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Leere Zeilen in Tabellenkalkulation entfernen"
type: docs
url: /de/cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, leere Zeilen entfernen, Tabellenkalkulation, API"
description: "Löscht alle leeren Zeilen aus einer Tabellenkalkulationsdatei."
weight: 100
---

## Das Entfernen leerer Zeilen in Tabellenkalkulationen über Aspose.Cells Cloud-Webdienste

Diese Methode entfernt Zeilen aus einer Tabellenkalkulation, die vollständig leer sind und weder Daten noch Objekte enthalten. Sie durchsucht alle Arbeitsblätter und identifiziert Zeilen, in denen jede Zelle leer ist. Der Vorgang erfolgt direkt in der Tabellenkalkulation, sodass nur Zeilen ohne Inhalt gelöscht werden. Dies hilft dabei, die Tabellenkalkulation zu bereinigen und unnötige leere Zeilen zu entfernen, wodurch die Daten übersichtlicher und einfacher zu verwalten werden. Benutzer sollten sicherstellen, dass die Tabellenkalkulation vor Durchführung dieses Vorgangs gesichert wird, da gelöschte Zeilen nicht wiederhergestellt werden können.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | Datei  | FormData                    | Hochladen der Tabellenkalkulationsdatei. |
| outPath        | Zeichenkette | Query                       | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. |
| outStorageName | Zeichenkette | Query                       | Name des Ausgabedatenspeichers. |
| region         | Zeichenkette | Query                       | Regionale/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsparsetzung und länderspezifisches Verhalten. |
| password       | Zeichenkette | Query                       | Das Passwort zum Öffnen der Tabellenkalkulationsdatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| Spreadsheet    | Datei | Hochladen der Tabellenkalkulationsdatei. |

### **Antwort**

```json
{
  "ResponseFile": "Binärer Dateistream"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|-------------|
| 200 | OK | Die bearbeitete Tabellenkalkulationsdatei mit entfernten leeren Zeilen wird zurückgegeben. |
| 400 | Ungültige Anforderung | Ungültige URL oder Anforderungsparameter. |
| 401 | Nicht autorisiert | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 404 | Nicht gefunden | Quelldatei nicht zugänglich. |
| 413 | Anforderungstext zu groß | Anforderungstext überschreitet die zulässige Größe. |
| 500 | Interner Serverfehler | In der Tabellenkalkulation ist beim Abruf von Daten ein Fehler aufgetreten. |

## Verwenden des Entfernens leerer Zeilen in Tabellenkalkulationen mit SDKs

### Spezifikation für das Entfernen leerer Zeilen in Tabellenkalkulationen

Die [API-Spezifikation zum Entfernen leerer Zeilen in Tabellenkalkulationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen direkte REST-Interaktionen aus einem Webbrowser heraus.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}
{< tab tabNum="1" >}
```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=de-DE&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "Binärer Dateistream"
}
```
{< /tab >}
{< /tabs >}

### Verwenden der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre ProjektAufgaben zu konzentrieren. Bitte überprüfen Sie den <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
`[TBD]`
---