---
title: Konvertera Excel till HTML  
description: Konvertera en Excel-arbetsbok till en HTML-fil med Aspose.Cells Cloud API v3.0.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Konvertera Excel till HTML  

Aspose.Cells Cloud tillhandahåller en robust REST-slutpunkt som konverterar en Excel-arbetsbok (XLS, XLSX, CSV m.fl.) till ett HTML-dokument. Åtgärden returnerar ett **FileInfo**-objekt som innehåller den genererade HTML-filen (namn, storlek och Base64-kodat innehåll).

---

## Förutsättningar

| Krav | Hur du tillfredställer det |
|------|----------------------------|
| **Aspose Cloud-konto** | Registrera dig på [aspose.cloud](https://www.aspose.cloud). |
| **JWT-åtkomsttoken** | Skaffa en bearer-token via OAuth 2.0-slutpunkten `POST /connect/token`. |
| **Lagring (valfritt)** | Om du vill att API:t ska läsa/skriva filer från en specifik lagring skapar du den först (t.ex. Amazon S3, Azure Blob eller Aspose Cloud-lagring). |
| **cURL / SDK** | En valfri HTTP-klient som stöder multipart/form-data (cURL, Postman eller ett av Aspose.Cells SDK:n). |

---

## Autentisering

Alla Aspose.Cells Cloud-förfrågningar kräver **JWT-tokenbaserad autentisering**.

```http
Authorization: Bearer <access-token>
```

Token måste inkluderas i `Authorization`-headern i varje förfrågan.

---

## Slutpunkt

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Obs** – Förfrågan måste skickas som `multipart/form-data`. Excel-filen är den första delen i multipart-kroppen.

---

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## Förfrågningsparametrar  

### URL-parametrar  

| Namn                     | Typ     | Obligatoriskt | Standardvärde | Beskrivning |
|--------------------------|---------|---------------|---------------|-------------|
| `password`               | string  | Nej           | –             | Lösenord för att öppna en skyddad arbetsbok. |
| `storageName`            | string  | Nej           | –             | Namn på lagringen där källfilen finns. |
| `checkExcelRestriction` | boolean | Nej           | `true`        | När `true` validerar tjänsten Excel-specifika begränsningar (t.ex. skyddade kalkylblad). |
| `region`                 | string  | Nej           | –             | Regionala inställningar för arbetsboken (t.ex. `sv-SE`). |
| `FontsLocation`          | string  | Nej           | –             | URL eller sökväg till en mapp som innehåller anpassade typsnitt som krävs för rendering. |

### Formdata (multipart)  

| Namn | Typ | Obligatoriskt | Beskrivning |
|------|-----|---------------|-------------|
| **File** | fil | **Ja** | Den Excel-arbetsbok som ska konverteras. Måste levereras som den första delen i multipart-förfrågan. |

---

## Exempel på förfrågan (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## Lyckad svar  

**Statuskod:** `200 OK`

| Fält         | Typ    | Beskrivning |
|--------------|--------|-------------|
| `Filename`   | string | Namn på den genererade HTML-filen (t.ex. `exempel.html`). |
| `FileSize`   | int    | Storlek på HTML-filen i byte. |
| `FileContent`| string | Base64-kodat HTML-innehåll. |

```json
{
  "Filename": "exempel.html",
  "FileSize": 12345,
  "FileContent": "base64_kodad_sträng"
}
```

Svarschemat definieras av modellen **FileInfo**: [/cells/file-info](/cells/file-info/).

---

## Felresponser  

| Kod | Betydelse | Exempelpayload |
|-----|-----------|----------------|
| `400` | Felaktig förfrågan – saknade eller ogiltiga parametrar | ```json { "Code": "BadRequest", "Message": "Delen 'File' krävs." } ``` |
| `401` | Obehörig – ogiltig eller saknad JWT-token | ```json { "Code": "InvalidToken", "Message": "Åtkomsttoken saknas eller har gått ut." } ``` |
| `404` | Ej hittad – källfilen finns inte i den angivna lagringen | ```json { "Code": "FileNotFound", "Message": "Filen 'min.xlsx' finns inte i lagringen 'MinLagring'." } ``` |
| `413` | För stor payload – den uppladdade filen överskrider den tillåtna storleken | ```json { "Code": "RequestEntityTooLarge", "Message": "Den uppladdade filen överskrider gränsen på 100 MB." } ``` |
| `429` | För många förfrågningar – hastighetsbegränsningen överskriden | ```json { "Code": "TooManyRequests", "Message": "Hastighetsbegränsningen på 60 anrop per minut överskriden." } ``` |
| `500` | Internt serverfel – oväntat serverfel | ```json { "Code": "InternalError", "Message": "Ett oväntat fel uppstod. Försök igen senare." } ``` |

---

## Hastighetsbegränsningar  

| Begränsning | Beskrivning |
|-------------|-------------|
| **60 förfrågningar per minut** per konto (standard) | Överskridning av denna gräns returnerar `429 Too Many Requests`. Justera din klientlogik eller begär en högre kvot via Aspose Clouds portal. |

---

## SDK-stöd  

Aspose tillhandahåller SDK:er för flera språk som omsluter denna slutpunkt. Exemplen nedan visar samma konvertering med officiella SDK:er.

| Språk | Exempel |
|-------|---------|
| C#    | <details><summary>Visa exempel</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java  | <details><summary>Visa exempel</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python| <details><summary>Visa exempel</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js| <details><summary>Visa exempel</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go    | <details><summary>Visa exempel</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP   | <details><summary>Visa exempel</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby  | <details><summary>Visa exempel</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl  | <details><summary>Visa exempel</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

Hela listan över stödda SDK:er och installationsinstruktioner finns i Aspose.Cells Cloud SDKs-repositoriet: <https://github.com/aspose-cells-cloud>.

---

## Relaterade slutpunkter  

| Slutpunkt | Beskrivning |
|-----------|-------------|
| `POST /cells/{name}/saveAs` | Spara en befintlig Excel-fil som HTML (eller andra format) direkt till lagring. |
| `PUT /cells/convert` | Konvertera en arbetsbok till HTML med ytterligare konverteringsalternativ; resultatet returneras i svarskroppen. |
| `GET /cells/{name}` | Hämta en arbetsbok som redan är lagrad som HTML (eller andra format) med valfria URL-parametrar. |

---

## Vanliga frågor  

**Fråga:** *Hur autentiserar jag vid anrop av API:et för Excel-till-HTML-konvertering?*  
**Svar:** Inkludera headern `Authorization: Bearer <access-token>` som du får från OAuth 2.0-slutpunkten `/connect/token`.

**Fråga:** *Vad innehåller svaret från `FileInfo`?*  
**Svar:** Tre fält – `Filename` (sträng), `FileSize` (heltal, byte) och `FileContent` (Base64-kodat HTML-innehåll).

**Fråga:** *Vilka felkoder kan jag stöta på?*  
**Svar:** `400` (Felaktig förfrågan), `401` (Obehörig), `404` (Filen hittades inte), `413` (För stor payload), `429` (För många förfrågningar), `500` (Internt serverfel). Varje fel returnerar en JSON-payload med `Code` och `Message`.

**Fråga:** *Kan jag ange en anpassad plats för typsnitt?*  
**Svar:** Ja. Använd URL-parametern `FontsLocation` för att peka på en mapp eller URL som innehåller de krävda typsnitten.

**Fråga:** *Finns det en hastighetsbegränsning för denna åtgärd?*  
**Svar:** Standardgränsen är **60 anrop per minut** per konto. Överskridning returnerar `429 Too Many Requests`.

---

## JSON-LD-brödsmulor (strukturerade data)

Lägg till detta block för att förbättra SEO genom att möjliggöra rika fragmentbrödsmulor i sökresultat.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Hem", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Utvecklarcenter", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Konvertering", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel till HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## Ändringslog  

| Version | Datum | Ändringar |
|---------|-------|-----------|
| **v3.0** | 2024‑10‑01 | Första offentliga utgåva av `PostConvertWorkbookToHtml`. |
| **v3.1** | 2025‑04‑15 | Lade till URL-parametrarna `region` och `FontsLocation`; uppdaterade format på fel-payload. |
| **v3.2** | 2026‑03‑20 | Lade till dokumentation om hastighetsbegränsningar och exempel på felresponser. |

--- 

*För ytterligare hjälp, vänligen kontakta Aspose-stöd eller besök den officiella API-referensen:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---