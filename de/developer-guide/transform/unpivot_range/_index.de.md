---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "Dokument"
linktype: "docs"
url: /de/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "Tauscht Zeilen und Spalten in der Tabellendatenbank aus."
weight: 10
---

## Die UnpivotRange von Aspose.Cells Cloud Webdiensten

Tauscht Zeilen und Spalten in der Tabellendatenbank aus.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                     |
|------------------|--------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Datei  | FormData                            | Hochladen der Tabellendatenbankdatei.                                                                                                                          |
| worksheet        | string | Abfrage                             | Der Name des Arbeitsblatts.                                                                                                                                     |
| cellArea         | string | Abfrage                             | Ein angegebener Datenbereich.                                                                                                                                   |
| skipEmptyValue   | boolean| Abfrage                             | Wenn auf `true` gesetzt, werden leere Werte übersprungen. Standardwert: `true`.                                                                                |
| outPath          | string | Abfrage                             | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist `null`.                                                                   |
| outStorageName   | string | Abfrage                             | Speichername der Ausgabedatei.                                                                                                                                 |
| region           | string | Abfrage                             | Region-/Spracheinstellung der Tabellendatenbank (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst die Zahlenformatierung, das Parsen von Datumsangaben und regionsabhängiges Verhalten. |
| password         | string | Abfrage                             | Das Passwort zum Öffnen der Tabellendatenbankdatei.                                                                                                            |

### Parameter im Anforderungstext

| Parametername | Typ | Beschreibung |
|---------------|-----|-------------|
| —             | —   | —           |

### **Antwort**

```json
{
  "File": "Binärstream"
}
```

**HTTP-Antwortstatuscodes**

| Code | Bedeutung             | Beschreibung                                      |
|------|-----------------------|---------------------------------------------------|
| 200  | OK                    | Die entpivottierte Tabellendatenbankdatei wird zurückgegeben. |
| 400  | Bad Request           | Ungültige Anforderungsparameter.                  |
| 401  | Unauthorized          | Authentifizierung fehlgeschlagen.                 |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error | Der Server ist auf einen unerwarteten Zustand gestoßen. |

## Verwendung von UnpivotRange mit SDKs

### Spezifikation von UnpivotRange

Die [UnpivotRange-API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells Cloud-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=de-DE&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Verwendung der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
 `[TBD]`
---