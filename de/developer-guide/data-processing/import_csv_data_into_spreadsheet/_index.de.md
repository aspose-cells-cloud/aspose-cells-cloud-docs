---
title: "CSV-Daten in eine Tabellenkalkulation importieren"
ArticleTitle: "CSV-Daten in eine Tabellenkalkulation importieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, CSV-Import, Tabellenkalkulation, API"
description: "CSV-Datendatei mithilfe der Aspose.Cells Cloud API in die lokale Tabellenkalkulation importieren."
weight: 100
---

## Importieren von CSV-Daten in eine Tabellenkalkulation über die Aspose.Cells Cloud-Webdienste

Importieren Sie eine CSV-Datendatei in die lokale Tabellenkalkulation. Die Methode analysiert die CSV-Datei, ordnet die Daten der Zellstruktur der Tabellenkalkulation zu und speichert die Datei lokal. Unterstützte Tabellenkalkulationsformate sind .xlsx und .ods.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername         | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                         |
|-----------------------|---------|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| datafile              | Datei   | FormData                           | Datendatei hochladen.                                                                                                                |
| Spreadsheet           | Datei   | FormData                           | Tabellenkalkulationsdatei hochladen.                                                                                                 |
| worksheet             | String  | Abfrage                            | CSV-Daten müssen in dieses Arbeitsblatt importiert werden. (erforderlich)                                                           |
| startcell             | String  | Abfrage                            | Startposition für den Datenimport. (erforderlich)                                                                                    |
| insert                | Boolean | Abfrage                            | Steuert das Einfügeverhalten. true: fügt Daten ein; false: überschreibt vorhandene Daten. Standard: true (optional)                |
| convertNumericData    | Boolean | Abfrage                            | Gibt an, ob Zeichenfolgen in Textdateien in numerische Daten konvertiert werden. Standard: true (optional)                          |
| splitter              | String  | Abfrage                            | Trennzeichen zur Aufteilung von CSV-Feldern. Standard: "," (optional)                                                               |
| outPath               | String  | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert: null (optional).                                  |
| outStorageName        | String  | Abfrage                            | Speichername für die Ausgabedatei. (optional)                                                                                       |
| fontsLocation         | String  | Abfrage                            | Benutzerdefinierte Schriftarten verwenden. (optional)                                                                               |
| region                | String  | Abfrage                            | Region/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, das Datumsparsing und länderspezifisches Verhalten. (optional) |
| password              | String  | Abfrage                            | Das Passwort zum Öffnen der Tabellenkalkulationsdatei. (optional)                                                                   |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Antwort**

```json
{
  "file": "<Binärstream der resultierenden Tabellenkalkulation>"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | CSV-Daten erfolgreich importiert; die resultierende Tabellenkalkulationsdatei wird zurückgegeben. |
| 400 | Bad Request | Ungültige Anforderungsparameter oder fehlerhafte URL. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 404 | Not Found | Quelldatei nicht zugänglich. |
| 413 | Payload Too Large | Die hochgeladenen Dateien überschreiten das zulässige Größenlimit. |
| 500 | Internal Server Error | Die Tabellenkalkulation hat beim Abrufen der Daten einen Fehler festgestellt. |

## Verwendung des CSV-Datenimports in eine Tabellenkalkulation mit SDKs

### Spezifikation für den CSV-Datenimport in eine Tabellenkalkulation

Die [API-Spezifikation für den CSV-Datenimport in eine Tabellenkalkulation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Sichere Verbindung über HTTPS verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Blatt1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=ausgabeordner&outStorageName=MeinSpeicher&fontsLocation=/benutzerdefinierte/schriftarten&region=de-DE&password=MeinPasswort" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@beispiel.csv" \
  -F "Spreadsheet=@arbeitsmappe.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<Binärstream der resultierenden Tabellenkalkulation>"
}
```

{< /tab >}

{< /tabs >}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert die niederwertigen Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
 `[TBD]`
---