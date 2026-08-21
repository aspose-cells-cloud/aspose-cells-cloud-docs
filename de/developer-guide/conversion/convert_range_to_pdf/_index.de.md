---
title: "ConvertRangeToPdf"
ArticleTitle: "Bereich in PDF konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, Bereich in PDF konvertieren, API"
description: "Konvertiert einen angegebenen Bereich einer Tabellendatei in PDF mithilfe von Aspose.Cells Cloud."
weight: 1
---

## ConvertRangeToPdf der Aspose.Cells Cloud-Webdienste

Konvertiert einen Bereich einer Tabellendatei auf einem lokalen Laufwerk in eine PDF-Datei.

### Web-API-Endpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername    | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                    |
|------------------|--------|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Datei  | FormData                           | Tabellendatei hochladen.                                                                                                                        |
| worksheet        | String | Abfrage                            | Name des Arbeitsblatts der Tabellendatei.                                                                                                      |
| range            | String | Abfrage                            | Zellbereich, z. B. A1:C10                                                                                                                       |
| outPath          | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. Standardwert ist null.                                                     |
| outStorageName   | String | Abfrage                            | Name des Speichers für die Ausgabedatei.                                                                                                       |
| fontsLocation    | String | Abfrage                            | Benutzerdefinierte Schriftarten verwenden.                                                                                                     |
| AutoRowsFit      | Boolean| Abfrage                            | (Optional) Alle Zeilen in den Arbeitsblättern automatisch anpassen.                                                                           |
| AutoColumnsFit   | Boolean| Abfrage                            | (Optional) Alle Spalten in den Arbeitsblättern automatisch anpassen.                                                                          |
| region           | String | Abfrage                            | Regionale-/Spracheinstellung der Tabellendatei (z. B. `de-DE`, `en-US`, `fr-FR`). Beeinflusst die Zahlenformatierung, Datumsinterpretation und länderspezifisches Verhalten. |
| password         | String | Abfrage                            | Passwort zum Öffnen der Tabellendatei.                                                                                                         |

### Anforderungstextparameter

| Parametername | Typ  | Beschreibung               |
|---------------|------|----------------------------|
| Spreadsheet   | Datei | Tabellendatei hochladen.   |

### **Antwort**

```json
{
  "file": "<binärer PDF-Inhalt>"
}
```

**Antwortstatuscodes**

| Code | Bedeutung             | Beschreibung                                                                 |
|------|-----------------------|------------------------------------------------------------------------------|
| 200  | OK                    | Erfolgreiche Konvertierung; gibt den erzeugten PDF-Dateistream zurück.      |
| 400  | Bad Request           | Ungültige URL.                                                               |
| 401  | Unauthorized          | Authentifizierung fehlgeschlagen oder keine Anmeldeinformationen angegeben. |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das zulässige Dateigrößenlimit.       |
| 500  | Internal Server Error | Bei der Tabellendatei ist beim Abrufen der Konvertierungsdaten ein Fehler aufgetreten. |

## Verwendung von ConvertRangeToPdf mit SDKs

### ConvertRangeToPdf-Spezifikation

Die [ConvertRangeToPdf-API-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose Cells Cloud-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}

{< tab tabNum="1" >}

```bash
# HTTPS für eine sichere Verbindung verwenden
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
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

### Verwendung von Aspose Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractiert die niedrigeren Detailstufen, sodass Sie sich auf die Projektaufgaben konzentrieren können. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> mit einer vollständigen Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose Cells Cloud-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

```csharp
// SDK-Beispielcode für C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// SDK-Beispielcode für Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# SDK-Beispielcode für Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// SDK-Beispielcode für JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`