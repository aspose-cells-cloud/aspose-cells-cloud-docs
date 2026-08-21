---
title: "Bir Excel dosyasını başka bir formata dönüştürün veya farklı bir şekilde kaydedin."
second_title: "Belge"
linktitle: "Dönüştürme ve Farklı Kaydet"
type: docs
url: /tr/conversion-and-save-as/
aliases: [  /tr/convert-excel/ , /tr/convert/ ]
keywords: "Aspose.Cells, Excel dönüştürme API'si, Excel’i PDF’e dönüştürme, Excel’i CSV’ye dönüştürme, Excel’i JSON’a dönüştürme, bulut tablolama dönüştürme"
description: "Aspose.Cells Cloud REST API kullanarak Excel çalışma kitaplarını PDF, CSV, JSON, HTML ve 15’ten fazla diğer forma dönüştürmeyi öğrenin. Endpoint ayrıntılarını, örnek cURL komutlarını ve Java, .NET, Python ve diğerleri için SDK snippet’lerini içerir."
weight: 30
ArticleTitle: "Aspose.Cells Cloud ile Excel Dosyalarını PDF, CSV, JSON ve Daha Fazlasına Dönüştürün"
---

İlk olarak bir Excel dosyasını belirli bir formatta—örneğin [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) veya [CSV](https://docs.fileformat.com/spreadsheet/csv/)—oluşturduysanız, özel özelliklerden yararlanmak amacıyla dosyayı başka bir formata dönüştürmek faydalı olabilir. Örneğin, bir Excel dosyasını [PDF](https://docs.fileformat.com/pdf/) formatına dönüştürmek, içeriğinin yetkisiz değişikliklerden korunmasını sağlar ve okunmasını/paylaşılmasını kolaylaştırır.

**Önkoşullar**  
Dönüştürme API’lerini çağırmadan önce Aspose Cloud’dan bir OAuth 2.0 erişim belirteci almanız ve çalışma kitabının Aspose Cloud depolama alanınızda (veya PUT dönüştürme endpoint’i için istek gövdesine eklenmiş olması) bulunduğundan emin olmanız gerekir.

Belge dönüştürme, karmaşık bir süreçtir. Dönüştürme işlemine katkısı olan ve dönüşüm sırasında dikkate alınması gereken birçok faktör vardır. Excel formatları arasında kesin ve profesyonel kalitede dönüştürme sağlaması, Aspose.Cells Cloud’un temel özelliklerinden biridir.

Hizmet, herhangi bir belge formatı dönüştürme işlemi için sorunsuz şekilde çalışır. Aşağıdaki formatlardaki belgeleri hem içe aktarabilir hem de dışa aktarabilirsiniz:

**Desteklenen Formatlar**  
- İçe/Dışa Aktarım: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- Yalnızca Dışa Aktarım: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### Dönüştürme API’leri

| API                         | Açıklama                                                                                      |
| :-------------------------- | :------------------------------------------------------------------------------------------- |
| `GET /cells/{name}`         | Bulut depolama alanından bir Excel çalışma kitabını alır ve istenen forma dönüştürür.        |
| `PUT /cells/convert`        | İstek gövdesinde verilen bir Excel çalışma kitabını belirtilen çıktı formatına dönüştürür.   |
| `POST /cells/{name}/saveAs` | Mevcut bir Excel çalışma kitabını doğrudan başka bir forma bulut depolama alanına kaydeder. |

**API ayrıntıları**

- **GET /cells/{name}**  
  - **Yol parametreleri:** `name` – çalışma kitabının dosya adı (zorunludur).  
  - **Sorgu parametreleri:** `format` – hedef format (örn. pdf, csv, json); `storage` – bulut depolama adı (isteğe bağlı); `folder` – depolama içindeki klasör yolu (isteğe bağlı).  
  - **Yanıt:** Dönüştürülmüş çalışma kitabının dosya akışı; `Content‑Type` hedef forma uyar.  
  - **Durum kodları:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **İstek gövdesi:** multipart/form‑data; kaynak çalışma kitabını içeren `file` alanı ve istenen çıktı formatını belirten zorunlu `format` alanı içerir.  
  - **Yanıt:** Dönüştürülmüş dosyanın ikili akışı.  
  - **Durum kodları:** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **Yol parametreleri:** `name` – mevcut çalışma kitabının adı.  
  - **Sorgu parametreleri:** `format` – hedef format; `outPath` – bulut depolama içindeki hedef yol (isteğe bağlı); `storage` – depolama adı (isteğe bağlı).  
  - **Yanıt:** İşlem sonucunu ve kaydedilen dosyanın yolunu içeren JSON nesnesi. Örnek yanıt:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "Dosya başarıyla kaydedildi.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **Durum kodları:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

**PDF’e dönüştürme için örnek cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Java SDK snippet’i (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**.NET SDK snippet’i (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Python SDK snippet’i (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

Aşağıdaki makaleler her API’yi ayrıntılı olarak açıklar ve ek cURL ile SDK örnekleri içerir:

- [Bir Excel dosyasını farklı bir forma dönüştürme](/tr/cells/convert-an-excel-file-to-different-formats)
- [Bir Excel dosyasını farklı bir forma kaydetme](/tr/cells/save-an-excel-file-as-other-formats-files)
- [Bir Excel dosyasını CSV dosyasına dönüştürme](/tr/cells/convert-excel-file-to-csv-file)
- [Bir Excel dosyasını DOCX dosyasına dönüştürme](/tr/cells/convert-excel-file-to-docx-file)
- [Bir Excel dosyasını HTML dosyasına dönüştürme](/tr/cells/convert-excel-file-to-html-file)
- [Bir Excel dosyasını JSON dosyasına dönüştürme](/tr/cells/convert-excel-file-to-json-file)
- [Bir Excel dosyasını Markdown dosyasına dönüştürme](/tr/cells/convert-excel-file-to-markdown-file)
- [Bir Excel dosyasını PDF dosyasına dönüştürme](/tr/cells/convert-excel-file-to-pdf-file)
- [Bir Excel dosyasını PNG dosyasına dönüştürme](/tr/cells/convert-excel-file-to-png-file)
- [Bir Excel dosyasını PPTX dosyasına dönüştürme](/tr/cells/convert-excel-file-to-pptx-file)
- [Bir Excel dosyasını SQL dosyasına dönüştürme](/tr/cells/convert-excel-file-to-sql-file)
- [Bir Excel dosyasını TIFF dosyasına dönüştürme](/tr/cells/convert-excel-file-to-tiff-file)
---