---
title: "Tabelle in CSV konvertieren"
ArticleTitle: "Tabelle in CSV konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Tabelle in CSV konvertieren"
type: docs
url: /de/cells/convert/table/csv
aliases: []
keywords: "Tabelle in CSV konvertieren, Aspose.Cells, Cloud API"
description: "Konvertiert eine Tabelle eines Tabellendokuments auf einem lokalen Laufwerk in eine CSV-Datei."
weight: 1
---

## Die Konvertierung von Tabellen in CSV mit Aspose.Cells Cloud-Webdiensten

Diese Methode liest eine Tabellendatei aus dem lokalen Dateisystem, konvertiert die angegebene Tabelle in eine CSV-Datei und gibt das konvertierte Ergebnis zurück. Sie erfolgt vollständig auf dem Cloud-Server, sodass kein Zwischenspeichern in den Cloud-Speicher erforderlich ist. Der Quelldateipfad und das Zielformat müssen korrekt angegeben werden, und es sind entsprechende Berechtigungen erforderlich, um die Quelldatei zu lesen. Fehler wie fehlende Dateien, nicht erreichbare Pfade oder Konvertierungsfehler führen zu entsprechenden Ausnahmen.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung |
|-------------------|--------|------------------------------------|--------------|
| Spreadsheet       | Datei  | FormData                           | Hochladen der Tabellendatei. |
| worksheet         | String | Abfrage                            | Name des Arbeitsblatts der Tabellendatei. |
| tableName         | String | Abfrage                            | Name der Tabelle |
| outPath           | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null. |
| outStorageName    | String | Abfrage                            | Name des Speichers für die Ausgabedatei. |
| fontsLocation     | String | Abfrage                            | Verwenden benutzerdefinierter Schriftarten. |
| AutoRowsFit       | Boolean| Abfrage                            | (Optional) Automatische Anpassung aller Zeilen in Arbeitsblättern. |
| AutoColumnsFit    | Boolean| Abfrage                            | (Optional) Automatische Anpassung aller Spalten in Arbeitsblättern. |
| region            | String | Abfrage                            | Regionale Spracheinstellung der Tabellendatei (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password          | String | Abfrage                            | Das Passwort zum Öffnen der Tabellendatei. |

### Parameter für den Anforderungstext

| Parametername | Typ  | Beschreibung |
| ------------- | ---- | ------------ |
| *Keine*       | *Keine* | *Kein Anforderungstext erforderlich; die Datei wird als multipart/form-data gesendet.* |

### **Antwort**

```json
{
  "file": "Binärstrom der generierten CSV-Datei"
}
```

**Antwort-Statuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Die Tabelle wurde erfolgreich konvertiert, und die CSV-Datei wird zurückgegeben. |
| 400 | Ungültige Anforderung | Ungültige Anforderungsparameter oder falsch formatierte URL. |
| 401 | Nicht autorisiert | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 404 | Nicht gefunden | Quelldatei ist nicht zugänglich oder existiert nicht. |
| 413 | Anforderungstext zu groß | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Interner Serverfehler | Während der Konvertierung ist ein Problem mit der Tabellendatei aufgetreten. |

## Verwenden der Konvertierung von Tabellen in CSV mit SDKs

### Spezifikation der Konvertierung von Tabellen in CSV

Die [API-Spezifikation für die Konvertierung von Tabellen in CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "Binärstrom der generierten CSV-Datei"
}
```

{< /tab >}

{< /tabs >}

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstractiert niedrigere Detailebenen und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
`[TBD]`
---