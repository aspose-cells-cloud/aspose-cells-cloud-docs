---
title: "Aspose.Cells Cloud Replace Web API – Text in Remote Spreadsheets aktualisieren"
second_title: "Dokument"
ArticleTitle: "Massen-Textersatz in Cloud-Excel-Dateien – Find & Replace API"
linktitle: "Inhalt in Remote-Tabellenkalkulation ersetzen"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, Inhalt ersetzen, Remote-Tabellenkalkulation, Find & Replace API, Cloud Excel, Massen-Textersatz"
description: "Nutzen Sie die Aspose.Cells Cloud Find & Replace API, um Text in Remote-Excel-Arbeitsmappen zu massenhaft aktualisieren. Sichere HTTPS-Endpunkt, OAuth2-Authentifizierung und sofort nutzbare SDK-Beispiele für schnelle Integration."
weight: 100
---

Führen Sie Massen-Textersatz in Cloud-gespeicherten Excel-Dateien durch. Suchen und aktualisieren Sie gezielt Textzeichenfolgen effizient mithilfe der Aspose.Cells Find & Replace API für Cloud-Tabellenkalkulationen.


## **Inhalt in Remote-Tabellenkalkulation durch API ersetzen**

### **Web-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anforderungsparameter

| Parametername   | Typ    | Ort      | Beschreibung                                                                                                                                                       |
| --------------- | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**        | String | Path     | Der Name der Arbeitsmappendatei, die im Cloud-Speicher gespeichert ist und bearbeitet werden soll (z. B. `"report.xlsx"`).                                        |
| **searchText**  | String | Query    | Die Zeichenfolge, die im gesamten Arbeitsblatt gesucht werden soll. Die Suche ist groß-/kleinschreibungsabhängig und gilt für alle Arbeitsblätter, sofern nicht durch andere Parameter eingeschränkt. |
| **replaceText** | String | Query    | Die Zeichenfolge, die jedes Vorkommen von `searchText` ersetzen wird.                                                                                             |
| **folder**      | String | Query    | Der Pfad des Cloud-Speicherordners, der die Quell-Arbeitsmappe enthält (z. B. `"/documents/quarterly/"`).                                                         |
| **storageName** | String | Query    | _(Optional)_ Der Name eines benutzerdefinierten Cloud-Speichers (z. B. `"MyS3Bucket"`). Falls nicht angegeben, wird der standardmäßig für das Konto konfigurierte Speicher verwendet. |
| **region**      | String | Query    | _(Optional)_ Gebietsschemabezeichner, der die Zeichencodierung und sprachspezifische Suchverhalten beeinflussen kann (z. B. `"en-US"`).                           |
| **password**    | String | Query    | _(Optional)_ Passwort zum Öffnen einer geschützten Arbeitsmappe.                                                                                                   |

### Antwort

Eine typische erfolgreiche Antwort gibt den Status des Vorgangs und die Anzahl durchgeführter Ersetzungen zurück:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Fehlercodes

- **400 Bad Request** – Ungültige Aspose.Cells Cloud API-URI.
- **401 Unauthorized** – Fehlender oder ungültiger OAuth 2.0-Zugriffstoken.
- **404 Not Found** – Die angegebene Tabellenkalkulationsdatei konnte nicht zugegriffen werden.
- **500 Server Error** – Ein unerwartetes serverseitiges Problem trat bei der Verarbeitung der Anforderung auf.

## Wann sollten Sie die API zum Ersetzen des Inhalts in Remote-Tabellenkalkulationen verwenden?

- **Massen-Cloud-Dateiaktualisierung** – Ändern Sie den Inhalt mehrerer Excel-Dateien, die in Cloud-Speichern wie AWS S3 oder Azure Blob gespeichert sind.
- **Dynamische Befüllung von Cloud-Templates** – Füllen Sie in der Cloud gespeicherte Berichtsvorlagen mit aktuellen Daten dynamisch aus.
- **Überregionale Dateisynchronisierung** – Halten Sie Excel-Dateien über verschiedene geografische Speicherregionen hinweg konsistent.

## Warum die API zum Ersetzen des Inhalts in Remote-Tabellenkalkulationen verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud stellt SDK-Bibliotheken für viele Programmiersprachen bereit, was den Entwicklungsaufwand im Vergleich zur Erstellung einer benutzerdefinierten Lösung reduziert.
- **Geringere Personalkosten** – Entfällt die Notwendigkeit für dediziertes Personal, um Dokumente manuell zusammenzuführen.
- **Pay-Per-Use** – Keine Vorab-Investition; Sie zahlen nur für die tatsächlich durchgeführten API-Aufrufe.
- **Keine Wartungskosten** – Keine zu verwaltenden Server, keine Software-Updates und keine Kompatibilitätsprobleme.
- **Beibehaltung aller Zellformatierungen, Formeln und Diagramme** – Der Vorgang bewahrt das ursprüngliche Layout und die Berechnungen der Arbeitsmappe nach dem Textersatz.

## Wie Sie die API zum Ersetzen des Inhalts in Remote-Tabellenkalkulationen mit SDKs verwenden

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie das Ersetzen von Inhalten in Tabellenkalkulationen mit minimalem Codeaufwand umsetzen können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:


---