---
title: "JSON-Daten in eine Tabellenkalkulation importieren"
ArticleTitle: "JSON-Daten in eine Tabellenkalkulation importieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "JSON-Daten in eine Tabellenkalkulation importieren"
type: docs
url: /cells/import/data/json
aliases: []
keywords: "JSON importieren, Aspose.Cells, Tabellenkalkulation, API"
description: "JSON-Datendatei in die lokale Tabellenkalkulation importieren."
weight: 1
---

## Importieren von JSON-Daten in eine Tabellenkalkulation über die Aspose.Cells Cloud-Webdienste

Importieren Sie eine JSON-Datendatei in die lokale Tabellenkalkulation. Die Methode analysiert das JSON, ordnet die Daten der Zellstruktur der Tabellenkalkulation zu und speichert die Datei lokal. Unterstützte Tabellenkalkulationsformate sind .xlsx und .ods.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|-----------------|--------|------------------------------------|--------------|
| datafile        | Datei  | FormData                           | Datendatei hochladen. |
| Spreadsheet     | Datei  | FormData                           | Tabellenkalkulationsdatei hochladen. |
| worksheet       | string | Abfrage                            | JSON-Daten sollen in dieses Arbeitsblatt importiert werden. |
| startcell       | string | Abfrage                            | Startposition für den Datenimport |
| insert          | boolean| Abfrage                            | Steuert das Einfügeverhalten. true: Daten einfügen; false: vorhandene Daten überschreiben. (Standard: true) |
| outPath         | string | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. |
| outStorageName  | string | Abfrage                            | Name des Speichers für die Ausgabedatei. |
| fontsLocation   | string | Abfrage                            | Benutzerdefinierte Schriftarten verwenden. |
| region          | string | Abfrage                            | Region-/Spracheinstellung der Tabellenkalkulation (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password        | string | Abfrage                            | Das Passwort zum Öffnen der Tabellenkalkulationsdatei. |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| [TBD] | [TBD] | [TBD] |

### **Antwort**

```json
{
  "file": "Binärstream"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200  | OK        | Datei erfolgreich generiert und zurückgegeben. |
| 400  | Bad Request | Ungültige URL. |
| 401  | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 404  | Not Found | Quelldatei nicht erreichbar. |
| 413  | Payload Too Large | [TBD] |
| 500  | Internal Server Error | In der Tabellenkalkulation ist ein Fehler beim Abrufen der Daten aufgetreten. |

## So verwenden Sie den JSON-Datenimport in eine Tabellenkalkulation mit SDKs

### Spezifikation: JSON-Daten in eine Tabellenkalkulation importieren

Die [Spezifikation der API zum Importieren von JSON-Daten in eine Tabellenkalkulation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}
{< tab tabNum="1" >}
```bash
# HTTPS für eine sichere Verbindung verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Blatt1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MeinSpeicher&fontsLocation=%2Ffonts&region=de-DE&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@daten.json" \
  -F "Spreadsheet=@arbeitsmappe.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "Binärstream"
}
```
{< /tab >}
{< /tabs >}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstractiert die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> mit einer vollständigen Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
 `[TBD]`
---