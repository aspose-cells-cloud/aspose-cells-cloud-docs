---
title: "ConvertWorksheetToPdf"
ArticleTitle: " Arbeitsblatt in PDF konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "ConvertWorksheetToPdf"
type: docs
url: /cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, Arbeitsblatt in PDF konvertieren, API"
description: "Konvertiert ein Arbeitsblatt einer Spreadsheet-Datei mithilfe von Aspose.Cells Cloud in PDF."
weight: 10
---

## ConvertWorksheetToPdf von Aspose.Cells Cloud-Webdiensten

Diese Methode liest eine Spreadsheet-Datei vom lokalen Dateisystem, konvertiert ihr Arbeitsblatt in eine PDF-Datei und gibt das konvertierte Ergebnis zurück. Der Quellpfad und das Zielformat müssen korrekt angegeben werden. Stellen Sie sicher, dass die erforderlichen Berechtigungen zum Lesen der Quelldatei und zum Schreiben der konvertierten Datei (falls zutreffend) vorliegen. Der Konvertierungsvorgang erfolgt vollständig auf dem Cloud-Server, wodurch kein Cloud-Speicher oder externe Downloads erforderlich sind.

Zu den Hauptfunktionen zählen cloud-nativer Konvertierungsvorgang, reduzierter Cloud-Ressourcenverbrauch und vereinfachter Arbeitsablauf.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                             |
|------------------|---------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Datei   | FormData                           | Hochladen der Spreadsheet-Datei.                                                                                                        |
| worksheet        | String  | Abfrage                            | Name des Arbeitsblatts der Spreadsheet-Datei.                                                                                          |
| outPath          | String  | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.                                         |
| outStorageName   | String  | Abfrage                            | Name des Speichers für die Ausgabedatei.                                                                                               |
| fontsLocation    | String  | Abfrage                            | Verwenden Sie benutzerdefinierte Schriftarten.                                                                                          |
| AutoRowsFit      | Boolean | Abfrage                            | (Optional) Passt alle Zeilen in den Arbeitsblättern automatisch an.                                                                    |
| AutoColumnsFit   | Boolean | Abfrage                            | (Optional) Passt alle Spalten in den Arbeitsblättern automatisch an.                                                                   |
| region           | String  | Abfrage                            | Region-/Spracheinstellung der Spreadsheet-Datei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsanalyse und länderspezifisches Verhalten. |
| password         | String  | Abfrage                            | Das Passwort zum Öffnen der Spreadsheet-Datei.                                                                                         |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung |
| ------------- | --- | ------------ |
| [TBD]         |     |              |

### **Antwort**

```json
{
  "file": "<Binärstream der generierten PDF-Datei>"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200 | OK | Das Arbeitsblatt wurde erfolgreich in PDF konvertiert und als Dateistream zurückgegeben. |
| 400 | Bad Request | Ungültige Anforderungsparameter oder falsch formatierte URL. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldedaten bereitgestellt. |
| 404 | Not Found | Quelldatei nicht zugänglich. |
| 413 | Payload Too Large | Die hochgeladene Datei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Während der Konvertierung ist ein Fehler in der Spreadsheet-Datei aufgetreten. |

## Verwenden von ConvertWorksheetToPdf mit SDKs

### ConvertWorksheetToPdf-Spezifikation

Die [ConvertWorksheetToPdf-API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Blatt1&outPath=Ausgabe%2FOrdner&outStorageName=MeinSpeicher&fontsLocation=%2Fbenutzerdefiniert%2FSchriftarten&AutoRowsFit=true&AutoColumnsFit=true&region=de-DE&password=SecretPwd" \
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
  "file": "<Binärstream der generierten PDF-Datei>"
}
```

{< /tab >}

{< /tabs >}

### Verwenden von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractiert Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Schauen Sie sich die <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
`[TBD]`
---