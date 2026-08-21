---
title: "Bereich in CSV konvertieren"
ArticleTitle: "Bereich in CSV konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Bereich in CSV konvertieren"
type: docs
url: /de/cells/convert/range/csv
aliases: []
keywords: "konvertieren, csv, bereich, Aspose.Cells"
description: "Konvertiert einen Bereich eines Tabellendokuments auf einer lokalen Festplatte in eine CSV-Datei."
weight: 1
---

## Konvertieren eines Bereichs in CSV mit Aspose.Cells Cloud-Webdiensten

Dieser Vorgang liest eine Tabellendatei vom lokalen Dateisystem, konvertiert einen angegebenen Bereich in das CSV-Format und gibt das konvertierte Ergebnis direkt zurück. Der Vorgang erfolgt vollständig auf dem Cloud-Server, sodass kein Zwischenspeichern oder Hochladen in den Cloud-Speicher erforderlich ist. Die API unterstützt optionale Parameter wie benutzerdefinierte Schriftarten, automatische Anpassung von Zeilen/Spalten, Locale-Einstellungen und passwortgeschützte Arbeitsmappen.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                             |
|-------------------|---------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet       | Datei   | FormData                           | Hochladen der Tabellendatei.                                                                                                             |
| worksheet         | String  | Abfrage                            | Name des Arbeitsblatts der Tabellendatei. **Erforderlich**.                                                                             |
| range             | String  | Abfrage                            | Zellbereich, z. B. `A1:C10`. **Erforderlich**.                                                                                           |
| outPath           | String  | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.                                           |
| outStorageName    | String  | Abfrage                            | Name des Speichers für die Ausgabedatei.                                                                                                |
| fontsLocation     | String  | Abfrage                            | Verwendung benutzerdefinierter Schriftarten.                                                                                             |
| AutoRowsFit       | Boolean | Abfrage                            | (Optional) Passt alle Zeilen in den Arbeitsblättern automatisch an.                                                                     |
| AutoColumnsFit    | Boolean | Abfrage                            | (Optional) Passt alle Spalten in den Arbeitsblättern automatisch an.                                                                    |
| region            | String  | Abfrage                            | Regionale/Ländereinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password          | String  | Abfrage                            | Das Passwort zum Öffnen der Tabellendatei.                                                                                              |

### Parameter im Anforderungstext

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| Keine         | N/A | Keine Parameter im Anforderungstext erforderlich. |

### **Antwort**

```json
{
  "ResponseFile": "Binärer Dateistream (CSV-Inhalt)"
}
```

**HTTP-Antwortstatuscodes**

| Code | Bedeutung              | Beschreibung                                                                 |
|------|------------------------|------------------------------------------------------------------------------|
| 200  | OK                     | Der Bereich wurde erfolgreich konvertiert, und die CSV-Datei wird im Antworttext zurückgegeben. |
| 400  | Bad Request            | Ungültige URL oder fehlende erforderliche Parameter.                        |
| 401  | Unauthorized           | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen übergeben. |
| 413  | Payload Too Large      | Die Anforderung übersteigt die zulässige Größe.                             |
| 500  | Internal Server Error  | Bei der Tabellendatei trat beim Abrufen der Konvertierungsdaten ein Fehler auf. |

## Verwenden der Bereich-in-CSV-Konvertierung mit SDKs

### Spezifikation der Bereich-in-CSV-Konvertierung

Die [API-Spezifikation für die Bereich-in-CSV-Konvertierung](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&AutoRowsFit=true&AutoColumnsFit=true&region=de-DE&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "Base64-kodierter_CSV_Inhalt"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractiert die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webdienste mit verschiedenen SDKs aufgerufen werden:
`[TBD]`
---