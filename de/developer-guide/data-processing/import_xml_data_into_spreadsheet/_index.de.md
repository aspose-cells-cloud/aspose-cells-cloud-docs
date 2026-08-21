---
title: "XML-Daten in eine Tabellenkalkulation importieren"
ArticleTitle: "XML-Daten in eine Tabellenkalkulation importieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /de/cells/import/data/xml
aliases: []
keywords: "XML importieren, Aspose.Cells, API"
description: "XML-Datendatei mit Aspose.Cells Cloud in die lokale Tabellenkalkulation importieren."
weight: 1000
---

## Das Importieren von XML-Daten in eine Tabellenkalkulation über die Aspose.Cells Cloud-Webdienste

Importieren Sie eine XML-Datendatei in die lokale Tabellenkalkulation. Die Methode analysiert die XML-Daten, ordnet die Daten der Zellstruktur der Tabellenkalkulation zu und speichert die Datei lokal. Unterstützte Tabellenkalkulationsformate sind unter anderem .xlsx und .ods.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                              |
|------------------|---------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| datafile         | Datei   | FormData                            | Datendatei hochladen.                                                                                                                     |
| Spreadsheet      | Datei   | FormData                            | Tabellenkalkulationsdatei hochladen.                                                                                                      |
| worksheet        | String  | Abfrage                             | XML-Daten müssen in dieses Arbeitsblatt importiert werden.                                                                               |
| startcell        | String  | Abfrage                             | Startposition für den Datenimport                                                                                                         |
| insert           | Boolean | Abfrage                             | Steuert das Einfügeverhalten. true: fügt Daten ein; false: überschreibt vorhandene Daten. Standardwert: **true**                        |
| outPath          | String  | Abfrage                             | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.                                           |
| outStorageName   | String  | Abfrage                             | Speichername für die Ausgabedatei.                                                                                                        |
| fontsLocation    | String  | Abfrage                             | Benutzerdefinierte Schriftarten verwenden.                                                                                                |
| region           | String  | Abfrage                             | Region/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password         | String  | Abfrage                             | Das Passwort zum Öffnen der Tabellenkalkulationsdatei.                                                                                    |

### Parameter des Anforderungstextes

| Parametername | Typ | Beschreibung |
|---------------|-----|--------------|
| *Keine*       | –   | –            |

### **Antwort**

```json
{
  "file": "<binärer Stream der aktualisierten Tabellenkalkulation>"
}
```

**Antwortstatuscodes**

| Code | Bedeutung               | Beschreibung                                                                                             |
|------|-------------------------|----------------------------------------------------------------------------------------------------------|
| 200  | OK                      | XML-Daten wurden erfolgreich importiert, und die aktualisierte Tabellenkalkulationsdatei wird zurückgegeben. |
| 400  | Ungültige Anforderung   | Ungültige Anforderungs-URL oder fehlende erforderliche Parameter.                                        |
| 401  | Nicht autorisiert       | Authentifizierung ist fehlgeschlagen oder es wurden keine Anmeldeinformationen bereitgestellt.            |
| 404  | Nicht gefunden          | Quelldatei ist nicht zugänglich.                                                                         |
| 413  | Anforderungstext zu groß | Die hochgeladene Datei überschreitet die zulässige Dateigröße.                                           |
| 500  | Interner Serverfehler   | In der Tabellenkalkulation ist beim Abrufen der Daten ein Fehler aufgetreten.                            |

## So verwenden Sie das Importieren von XML-Daten in eine Tabellenkalkulation mit SDKs

### Spezifikation: XML-Daten in eine Tabellenkalkulation importieren

Die [API-Spezifikation zum Importieren von XML-Daten in eine Tabellenkalkulation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mithilfe von cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{DataFileName}" \
  -F "Spreadsheet=@{SpreadsheetFileName}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binärer Stream der aktualisierten Tabellenkalkulation>"
}
```

{< /tab >}

{< /tabs >}

### Verwenden von Aspose Cells Cloud SDKs

Die Verwendung eines SDK ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractisiert Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---