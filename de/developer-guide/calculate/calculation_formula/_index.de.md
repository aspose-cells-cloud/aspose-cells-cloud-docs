---
title: "Formel berechnen"
ArticleTitle: "Formel berechnen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Formel berechnen"
type: docs
url: /de/cells/calculate/formula
aliases: []
keywords: "Aspose Cells, Formel berechnen, Tabellenkalkulation, API"
description: "Berechnen Sie eine Formel in einer Tabellenkalkulation mithilfe der Aspose.Cells Cloud API."
weight: 100
---

## Die Formelberechnung von Aspose.Cells Cloud-Webdiensten

Berechnet eine angegebene Formel in einem gegebenen Arbeitsblatt einer hochgeladenen Tabellenkalkulationsdatei und gibt die resultierende Tabellenkalkulationsdatei als Datenstrom zurück. Dieser Vorgang unterstützt regionsabhängige Verarbeitung über den Parameter **region** und kann passwortgeschützte Dateien öffnen.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|-------------------|--------|------------------------------------|--------------|
| Spreadsheet       | Datei  | FormData                           | Hochladen der Tabellenkalkulationsdatei. |
| worksheet         | String | Query                              | Name des Arbeitsblatts, das die Formel enthält. |
| formula           | String | Query                              | Die zu berechnende Formel (z. B. `=SUMME(A1:B2)`). |
| region            | String | Query                              | Regionale Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und regionsabhängiges Verhalten. |
| password          | String | Query                              | Das Passwort zum Öffnen der Tabellenkalkulationsdatei. |

### Parameter für den Anforderungstext

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| [TBD]         | [TBD] | [TBD] |

### **Antwort**

```json
{
  "File": "<binärer Datenstrom der resultierenden Tabellenkalkulation>"
}
```

**Antwort-Statuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die Berechnung war erfolgreich; die resultierende Tabellenkalkulationsdatei wird zurückgegeben. |
| 400 | Ungültige Anforderung | Einer oder mehrere Anforderungsparameter fehlen oder sind ungültig. |
| 401 | Nicht autorisiert | Die Authentifizierung ist fehlgeschlagen oder das JWT-Token fehlt/ist ungültig. |
| 413 | Anforderungstext zu groß | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Interner Serverfehler | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

## So verwenden Sie die Formelberechnung mit SDKs

### Spezifikation der Formelberechnung

Die [API-Spezifikation „Formel berechnen“](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUMME(A1%3AB2)&region=de-DE&password=MeinPasswort" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@beispiel.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "<binärer Datenstrom der resultierenden Tabellenkalkulation>"
}
```

{< /tab >}

{< /tabs >}

### Verwenden der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractisiert die niederleveligen Details, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
 `[TBD]`
---