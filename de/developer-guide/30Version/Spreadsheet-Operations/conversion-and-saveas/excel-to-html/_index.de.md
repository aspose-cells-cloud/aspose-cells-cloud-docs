---
title: Excel in HTML konvertieren  
description: Konvertieren Sie eine Excel-Arbeitsmappe mit der Aspose.Cells Cloud API v3.0 in eine HTML-Datei.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Excel in HTML konvertieren  

Aspose.Cells Cloud stellt einen leistungsstarken REST-Endpunkt bereit, der eine Excel-Arbeitsmappe (XLS, XLSX, CSV usw.) in ein HTML-Dokument konvertiert. Der Vorgang gibt ein **FileInfo**-Objekt zurück, das die generierte HTML-Datei enthält (Dateiname, Größe und Base64-kodierten Inhalt).

---

## Voraussetzungen

| Anforderung | Erfüllung |
|-------------|-----------|
| **Aspose Cloud-Konto** | Registrieren Sie sich unter [aspose.cloud](https://www.aspose.cloud). |
| **JWT-Zugriffstoken** | Holen Sie sich ein Bearer-Token über den OAuth 2.0-Endpunkt `POST /connect/token`. |
| **Speicher (optional)** | Falls die API Dateien aus einem bestimmten Speicher lesen/schreiben soll, erstellen Sie diesen zuerst (z. B. Amazon S3, Azure Blob oder Aspose Cloud-Speicher). |
| **cURL / SDK** | Jeder HTTP-Client, der multipart/form‑data unterstützt (cURL, Postman oder eines der Aspose.Cells SDKs). |

---

## Authentifizierung  

Alle Anfragen an Aspose.Cells Cloud erfordern eine **JWT-Token-basierte Authentifizierung**.

```http
Authorization: Bearer <access-token>
```

Das Token muss im `Authorization`-Header jeder Anfrage enthalten sein.

---

## Endpunkt  

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Hinweis** – Die Anfrage muss als `multipart/form-data` gesendet werden. Die Excel-Datei ist der erste Teil des multipart-Body.

---

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## Anforderungsparameter  

### Abfrageparameter  

| Name                     | Typ     | Erforderlich | Standardwert | Beschreibung |
|--------------------------|---------|--------------|--------------|--------------|
| `password`               | string  | Nein         | –            | Passwort zum Öffnen einer geschützten Arbeitsmappe. |
| `storageName`            | string  | Nein         | –            | Name des Speichers, in dem sich die Quelldatei befindet. |
| `checkExcelRestriction` | boolean | Nein         | `true`       | Wenn `true`, validiert der Dienst Excel-spezifische Einschränkungen (z. B. geschützte Tabellen). |
| `region`                 | string  | Nein         | –            | Regionale Einstellungen für die Arbeitsmappe (z. B. `de-DE`). |
| `FontsLocation`          | string  | Nein         | –            | URL oder Pfad zu einem Ordner mit benutzerdefinierten Schriftarten für die Darstellung. |

### Formular-Daten (Multipart)  

| Name | Typ | Erforderlich | Beschreibung |
|------|-----|--------------|--------------|
| **File** | Datei | **Ja** | Die zu konvertierende Excel-Arbeitsmappe. Muss als erster Teil der multipart-Anfrage übermittelt werden. |

---

## Beispielanfrage (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## Erfolgreiche Antwort  

**Statuscode:** `200 OK`

| Feld         | Typ    | Beschreibung |
|--------------|--------|--------------|
| `Filename`   | string | Name der generierten HTML-Datei (z. B. `beispiel.html`). |
| `FileSize`   | int    | Größe der HTML-Datei in Bytes. |
| `FileContent`| string | Base64-kodierter HTML-Inhalt. |

```json
{
  "Filename": "beispiel.html",
  "FileSize": 12345,
  "FileContent": "base64_encodierter_string"
}
```

Das Antwortschema wird durch das Modell **FileInfo** definiert: [/cells/file-info](/cells/file-info/).

---

## Fehlerantworten  

| Code | Bedeutung | Beispiel-Payload |
|------|-----------|------------------|
| `400` | Ungültige Anfrage – fehlende/ungültige Parameter | ```json { "Code": "BadRequest", "Message": "Der 'File'-Teil ist erforderlich." } ``` |
| `401` | Nicht autorisiert – ungültiges oder fehlendes JWT-Token | ```json { "Code": "InvalidToken", "Message": "Zugriffstoken fehlt oder ist abgelaufen." } ``` |
| `404` | Nicht gefunden – Quelldatei nicht im angegebenen Speicher | ```json { "Code": "FileNotFound", "Message": "Datei 'my.xlsx' existiert nicht im Speicher 'MyStorage'." } ``` |
| `413` | Anforderungstext zu groß – hochgeladene Datei überschreitet die erlaubte Größe | ```json { "Code": "RequestEntityTooLarge", "Message": "Hochgeladene Datei überschreitet das Limit von 100 MB." } ``` |
| `429` | Zu viele Anfragen – Ratenlimit überschritten | ```json { "Code": "TooManyRequests", "Message": "Ratenlimit von 60 Aufrufen pro Minute überschritten." } ``` |
| `500` | Interner Serverfehler – unerwarteter Serverzustand | ```json { "Code": "InternalError", "Message": "Ein unerwarteter Fehler ist aufgetreten. Bitte versuchen Sie es später erneut." } ``` |

---

## Ratenlimits  

| Limit | Beschreibung |
|-------|-------------|
| **60 Anfragen pro Minute** pro Konto (Standard) | Überschreiten Sie dieses Limit, um `429 Too Many Requests` zu erhalten. Passen Sie Ihre Client-Logik an oder beantragen Sie über das Aspose Cloud-Portal ein höheres Kontingent. |

---

## SDK-Unterstützung  

Aspose bietet erstklassige SDKs an, die diesen Endpunkt für mehrere Sprachen umschließen. Die folgenden Beispiele zeigen dieselbe Konvertierung mit den offiziellen SDKs.

| Sprache | Beispiel |
|---------|----------|
| C#      | <details><summary>Beispiel anzeigen</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java    | <details><summary>Beispiel anzeigen</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python  | <details><summary>Beispiel anzeigen</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js | <details><summary>Beispiel anzeigen</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go      | <details><summary>Beispiel anzeigen</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP     | <details><summary>Beispiel anzeigen</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby    | <details><summary>Beispiel anzeigen</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl    | <details><summary>Beispiel anzeigen</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

Für die vollständige Liste der unterstützten SDKs und Installationsanweisungen siehe das Repository **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud>.

---

## Verwandte Endpunkte  

| Endpunkt | Beschreibung |
|----------|--------------|
| `POST /cells/{name}/saveAs` | Speichern Sie eine bestehende Excel-Datei direkt als HTML (oder andere Formate) im Speicher. |
| `PUT /cells/convert` | Konvertieren Sie eine Arbeitsmappe in HTML mit erweiterten Konvertierungsoptionen; das Ergebnis wird im Antworttext zurückgegeben. |
| `GET /cells/{name}` | Rufen Sie eine bereits als HTML (oder andere Formate) gespeicherte Arbeitsmappe ab, optional mit Abfrageparametern. |

---

## Häufig gestellte Fragen  

**Q:** *Wie authentifiziere ich mich beim Aufruf der Excel-zu-HTML-Konvertierungs-API?*  
**A:** Fügen Sie einen Header `Authorization: Bearer <access-token>` hinzu, den Sie vom OAuth 2.0-Endpunkt `/connect/token` erhalten haben.

**Q:** *Was enthält die `FileInfo`-Antwort?*  
**A:** Drei Felder – `Filename` (Zeichenkette), `FileSize` (Ganzzahl, Bytes) und `FileContent` (Base64-kodierter HTML-Inhalt).

**Q:** *Welche Fehlercodes kann ich erwarten?*  
**A:** `400` (Ungültige Anfrage), `401` (Nicht autorisiert), `404` (Datei nicht gefunden), `413` (Anforderungstext zu groß), `429` (Zu viele Anfragen), `500` (Interner Serverfehler). Jeder gibt eine JSON-Payload mit `Code` und `Message` zurück.

**Q:** *Kann ich einen benutzerdefinierten Schriftartenpfad angeben?*  
**A:** Ja. Verwenden Sie den Abfrageparameter `FontsLocation`, um auf einen Ordner oder eine URL mit den erforderlichen Schriftarten zu verweisen.

**Q:** *Gibt es ein Ratenlimit für diesen Vorgang?*  
**A:** Das Standardlimit beträgt **60 Aufrufe pro Minute** pro Konto. Überschreiten Sie es, erhalten Sie `429 Too Many Requests`.

---

## JSON‑LD-Brotkrümel (Strukturierte Daten)

Das Hinzufügen dieses Blocks verbessert das SEO, indem erreichende Snippet-Brotkrümel in Suchergebnissen ermöglicht werden.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Startseite", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Entwickler-Center", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Konvertierung", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel in HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## Änderungsprotokoll  

| Version | Datum | Änderungen |
|---------|-------|------------|
| **v3.0** | 2024‑10‑01 | Erstveröffentlichung von `PostConvertWorkbookToHtml`. |
| **v3.1** | 2025‑04‑15 | Hinzugefügt: Abfrageparameter `region` und `FontsLocation`; aktualisiertes Format der Fehler-Payload. |
| **v3.2** | 2026‑03‑20 | Dokumentation zu Ratenlimits und Beispiel-Fehlerantworten eingeführt. |

--- 

*Für weitere Unterstützung wenden Sie sich bitte an den Aspose-Support oder besuchen Sie die offizielle API-Referenz:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---