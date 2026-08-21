---
title: "Tabelle in PDF konvertieren"
ArticleTitle: "Tabelle in PDF konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Tabelle in PDF konvertieren"
type: docs
url: /cells/convert/table/pdf
aliases: []
keywords: "Tabelle in PDF konvertieren, Aspose.Cells, API"
description: "Konvertiert eine Tabelle einer Tabellendatei auf dem lokalen Laufwerk mithilfe von Aspose.Cells Cloud in eine PDF-Datei."
weight: 1000
---

## Die Konvertierung von Tabellen in PDF über die Webdienste von Aspose.Cells Cloud

Dieser Vorgang liest eine Tabellendatei vom lokalen Dateisystem, konvertiert die angegebene Tabelle in ein PDF-Dokument und gibt das konvertierte Ergebnis zurück. Der Vorgang erfolgt vollständig auf dem Cloud-Server, sodass kein Zwischenspeichern in den Cloud-Speicher erforderlich ist. Die API unterstützt optionale Parameter für den Ausgabeort, benutzerdefinierte Schriftarten, automatische Anpassung von Zeilen/Spalten, Regionseinstellungen und passwortgeschützte Arbeitsmappen.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                     |
|------------------|--------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Datei  | FormData                          | Hochladen der Tabellendatei.                                                                                                                                    |
| worksheet        | String | Abfrage                           | Name des Arbeitsblatts der Tabellendatei.                                                                                                                       |
| tableName        | String | Abfrage                           | Name der Tabelle.                                                                                                                                               |
| outPath          | String | Abfrage                           | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Der Standardwert ist null.                                                                  |
| outStorageName   | String | Abfrage                           | Speichername für die Ausgabedatei.                                                                                                                              |
| fontsLocation    | String | Abfrage                           | Verwendung benutzerdefinierter Schriftarten.                                                                                                                     |
| AutoRowsFit      | Boolean| Abfrage                           | (Optional) Passt automatisch alle Zeilen in Arbeitsblättern an.                                                                                                |
| AutoColumnsFit   | Boolean| Abfrage                           | (Optional) Passt automatisch alle Spalten in Arbeitsblättern an.                                                                                               |
| region           | String | Abfrage                           | Regionale Spracheinstellung der Tabellendatei (z. B. `de-DE`, `fr-FR`). Beeinflusst die Zahlenformatierung, das Parsen von Datumsangaben und länderspezifisches Verhalten. |
| password         | String | Abfrage                           | Das Passwort zum Öffnen der Tabellendatei.                                                                                                                      |

### Parameter im Anforderungstext

| Parametername | Typ | Beschreibung |
|---------------|-----|-------------|
| *Keine*       | *Keine* | *Kein JSON-Textkörper erforderlich; die Datei wird über multipart/form-data gesendet.* |

### **Antwort**

```json
{
  "file": "<binärer PDF-Inhalt>"
}
```

**Antwortstatuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|-------------|
| 200 | OK | Die Tabelle wurde erfolgreich in PDF konvertiert; der Antworttext enthält den PDF-Dateistream. |
| 400 | Bad Request | Ungültige Anforderungsparameter oder fehlerhafte URL. |
| 401 | Unauthorized | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen bereitgestellt. |
| 404 | Not Found | Quelldatei nicht zugänglich oder Arbeitsblatt/Tabelle nicht gefunden. |
| 413 | Payload Too Large | Die hochgeladene Tabellendatei überschreitet das zulässige Größenlimit. |
| 500 | Internal Server Error | Beim Konvertieren der Tabellendatei in PDF ist ein Fehler aufgetreten. |

## Verwendung der Konvertierung von Tabellen in PDF mit SDKs

### Spezifikation für die Konvertierung von Tabellen in PDF

Die [API-Spezifikation für die Konvertierung von Tabellen in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# Verwenden Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binärer PDF-Inhalt>"
}
```

{< /tab >}

{< /tabs >}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstractiert die niederleveligen Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

```csharp
// SDK-Beispielcode für C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// SDK-Beispielcode für Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# SDK-Beispielcode für Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`
---