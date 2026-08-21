---
---
title: "Tabelle aufteilen"
ArticleTitle: "Tabelle aufteilen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "Tabelle aufteilen"
type: docs
url: /cells/split/table
aliases: []
keywords: "Aspose.Cells, Tabelle aufteilen, API"
description: "API zum Aufteilen einer Tabelle in einer Tabellendatei nach Spaltenwerten."
weight: 1
---

## Die SplitTable-Methode von Aspose.Cells Cloud Webdiensten

Diese Methode führt eine Aufteilungsoperation an der Quelltabelle durch, indem sie die Zeilen nach den unterschiedlichen Werten in der angegebenen Spalte gruppiert. Jede Gruppe von Daten (für jeden eindeutigen Aufteilungswert) wird anschließend als eigenständige Dateneinheit verarbeitet. Das Exportziel wird durch zwei wichtige boolesche Parameter gesteuert:
- Steuert die Arbeitsmappestruktur. Wenn `true`, wird jede Aufteilungseinheit in einer separaten Arbeitsmappe gespeichert. Falls `false`, wird jede Einheit als neues Arbeitsblatt in der aktuellen Arbeitsmappe hinzugefügt.
- Steuert die Ausgabeverpackung. Bei Einstellung auf `true` und Kombination mit `toNewWorkbook` = `true` erzeugt die Methode mehrere einzelne Dateien und gibt diese als ZIP-Archiv zurück. Bei `false` werden alle Daten in einer einzigen Datei gespeichert (entweder eine mehrblättrige Arbeitsmappe oder eine einzelne Datei gemäß anderen Einstellungen).

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                              |
|-------------------|---------|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet       | Datei   | FormData                            | Hochzuladende Tabellendatei.                                                                                                                                              |
| worksheet         | String  | Abfrage                             | Arbeitsblatt, das die Tabelle enthält.                                                                                                                                    |
| tableName         | String  | Abfrage                             | Zu teilende Datentabelle.                                                                                                                                                 |
| splitColumnName   | String  | Abfrage                             | Spaltenname, nach dem aufgeteilt werden soll.                                                                                                                             |
| saveSplitColumn   | Boolean | Abfrage                             | Ob die Daten in der Aufteilungsspalte beibehalten werden sollen.                                                                                                          |
| splitRowNumber    | Integer | Abfrage                             | [VBD]                                                                                                                                                                      |
| toNewWorkbook     | Boolean | Abfrage                             | Steuerung des Exportziels: true – Erstellt neue Arbeitsmappendateien mit den aufgeteilten Daten; false – Fügt der aktuellen Arbeitsmappe ein neues Arbeitsblatt hinzu.      |
| toMultipleFiles   | Boolean | Abfrage                             | true – Exportiert Tabellendaten als **mehrere separate Dateien** (als ZIP-Archiv zurückgegeben); false – Speichert alle Daten in **einer einzigen Datei** mit mehreren Blättern. Standardwert: false. |
| outPath           | String  | Abfrage                             | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert wird. Standardwert ist null.                                                                               |
| outStorageName    | String  | Abfrage                             | Speichername für die Ausgabedatei.                                                                                                                                        |
| fontsLocation     | String  | Abfrage                             | Verwendung benutzerdefinierter Schriftarten.                                                                                                                               |
| region            | String  | Abfrage                             | Regionale/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, das Parsen von Datumsangaben und länderspezifisches Verhalten. |
| password          | String  | Abfrage                             | Das Passwort zum Öffnen der Tabellendatei.                                                                                                                                |

### Anforderungstextparameter

| Parametername | Typ  | Beschreibung            |
| ------------- | ---- | ----------------------- |
| Spreadsheet   | Datei | Hochzuladende Tabellendatei. |

### **Antwort**

```json
{
  "file": "Binärstream (ZIP-Archiv oder Arbeitsmappe, abhängig von den Parametern)"
}
```

**Antwortstatuscodes**

| Code | Bedeutung           | Beschreibung                                                                                     |
|------|---------------------|--------------------------------------------------------------------------------------------------|
| 200  | OK                  | Die Aufteilungsoperation wurde erfolgreich abgeschlossen. Die Antwort enthält die erzeugte Datei (ZIP-Archiv oder Arbeitsmappe). |
| 400  | Bad Request         | Ungültige URL oder Anforderungsparameter.                                                       |
| 401  | Unauthorized        | Authentifizierung ist fehlgeschlagen oder es wurden keine Anmeldeinformationen übermittelt.     |
| 404  | Not Found           | Quelldatei ist nicht erreichbar.                                                                 |
| 413  | Payload Too Large   | Die Anforderungsnutzlast überschreitet die zulässige Größe.                                     |
| 500  | Internal Server Error | In der Tabellendatei ist ein Fehler beim Abrufen von Daten aufgetreten.                         |

## Verwendung von SplitTable mit SDKs

### SplitTable-Spezifikation

Die [SplitTable-API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells Cloud-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL erfolgen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# HTTPS für eine sichere Verbindung verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Blatt1&tableName=MeineTabelle&splitColumnName=Kategorie&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=Ausgabe%2FOrdner&outStorageName=MeinSpeicher&fontsLocation=%2Fbenutzerdefiniert%2FSchriftarten&region=de-DE&password=GeheimesPasswort" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <JWT-Token>" \
  -F "Spreadsheet=@beispiel.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "file": "Binärstream (ZIP-Archiv oder Arbeitsmappe, abhängig von den Parametern)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre ProjektAufgaben zu konzentrieren.Bitte überprüfen Sie den <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
`[VBD]`
---