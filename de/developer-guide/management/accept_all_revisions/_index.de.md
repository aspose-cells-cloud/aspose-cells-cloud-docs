---
title: "Alle Überarbeitungen akzeptieren"
ArticleTitle: "Alle Überarbeitungen akzeptieren – Aspose.Cells Cloud"
second_title: "Dokument"
linktype: "docs"
url: /cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, Tabellenkalkulation, Überarbeitungen"
description: "Alle Überarbeitungen in einer Tabellenkalkulationsdatei mit der Aspose.Cells Cloud API akzeptieren."
weight: 100
---

## AcceptAllRevisions von Aspose.Cells Cloud-Webdiensten

Akzeptiert alle Überarbeitungen in der hochgeladenen Tabellenkalkulationsdatei und gibt die verarbeitete Arbeitsmappe zurück.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername      | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|--------------------|--------|------------------------------------|--------------|
| Spreadsheet        | Datei  | FormData (HTTP-Body)               | Tabellenkalkulationsdatei hochladen. |
| outPath            | string | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null. |
| outStorageName     | string | Abfrage                            | Speichername für die Ausgabedatei. |
| fontsLocation      | string | Abfrage                            | Benutzerdefinierte Schriftarten verwenden. |
| region             | string | Abfrage                            | Regionale/sprachliche Einstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password           | string | Abfrage                            | Das Passwort zum Öffnen der Tabellenkalkulationsdatei. |

### Parameter im Anforderungstext

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| Spreadsheet   | Datei | Tabellenkalkulationsdatei hochladen. |

### **Antwort**

```json
{
  "File": "Binärstrom der verarbeiteten Tabellenkalkulation"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die Überarbeitungen wurden erfolgreich akzeptiert und die verarbeitete Datei wird zurückgegeben. |
| 400 | Bad Request | Die Anforderung ist ungültig (z. B. fehlende erforderliche Datei oder ungültige Parameter). |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder JWT-Token fehlt/ist ungültig. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Ein unerwarteter Fehler ist auf dem Server aufgetreten. |

## Verwendung von AcceptAllRevisions mit SDKs

### AcceptAllRevisions-Spezifikation

Die [AcceptAllRevisions API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Sichere Verbindung über HTTPS verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=de-DE&password=12345" \
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
  "File": "Binärstrom der verarbeiteten Tabellenkalkulation"
}
```

{< /tab >}

{< /tabs >}

### Verwendung der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="[TBD]" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
 `[TBD]`
---