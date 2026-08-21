---
title: "Çalışma Sayfasını Dışa Aktar – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "Çalışma Sayfası"
type: docs
url: /export-excel-worksheet-to-different-formats/
aliases: [/export/excel-worksheet-to-different-formats/]
keywords: "Aspose.Cells, çalışma sayfasını dışa aktar, Excel API’si, PDF, CSV, TIFF, ODS, resim formatları"
description: "Aspose.Cells Cloud REST API’sini kullanarak bir Excel çalışma sayfasını PDF, CSV, TIFF ve diğer formatlara nasıl dışa aktaracağınızı öğrenin. cURL örneği, gerekli kimlik doğrulama, parametre detayları ve yanıt işleme içerir."
weight: 20
ArticleTitle: "Excel Çalışma Sayfasını Çeşitli Formatlara Dışa Aktar – Aspose.Cells Cloud"
---

Bir çalışma sayfasını aşağıdaki formatlara dışa aktarabilirsiniz:

- **XLS** – [XLS formatı detayları](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [XLSX formatı detayları](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [XLSB formatı detayları](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [CSV formatı detayları](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [TSV formatı detayları](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [XLSM formatı detayları](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [ODS formatı detayları](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [TXT formatı detayları](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [PDF formatı detayları](https://docs.fileformat.com/pdf/)
- **OTS** – [OTS formatı detayları](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [XPS formatı detayları](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [DIF formatı detayları](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [PNG formatı detayları](https://docs.fileformat.com/Image/png/)
- **JPEG** – [JPEG formatı detayları](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [BMP formatı detayları](https://docs.fileformat.com/image/bmp/)
- **SVG** – [SVG formatı detayları](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [TIFF formatı detayları](https://docs.fileformat.com/image/tiff/)
- **EMF** – [EMF formatı detayları](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Numbers formatı detayları](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [FODS formatı detayları](https://docs.fileformat.com/spreadsheet/fods/)

[Çalışma kitabının tamamını veya bir grafiği dışa aktarma gibi ilgili dışa aktarma işlemlerini keşfedin.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## PostExport API’si

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür    | Yol/Sorgu Dizisi/HTTP Gövdesi | Gerekli | Açıklama                                                                 |
|---------------|--------|-------------------------------|---------|--------------------------------------------------------------------------|
| file          | dosya  | formData                      | Evet    | Yüklenecek dosya                                                         |
| objectType    | string | sorgu                         | Evet    | Dışa aktarılacak nesne türü. Grafik dışa aktarımı için `chart` kullanın. Diğer olası değerler: `worksheet`, `picture` vb. |
| format        | string | sorgu                         | Evet    | İstenen çıktı formatı. Desteklenen değerler: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### Yanıt

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **Hata işleme**

İstek başarısız olursa API, `Code` ve `Message` gibi alanları içeren bir JSON hata nesnesi döndürür. Tipik HTTP durum kodları arasında **401 Unauthorized** (eksik veya geçersiz belirteç) ve **400 Bad Request** (geçersiz parametreler) bulunur.

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyutu sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |

**Notlar**

- Yükleme için maksimum dosya boyutu 50 MB’dir.  
- API, tek bir istekte birden fazla çalışma sayfasını dışa aktarmayı destekler; her çalışma sayfası `Files` dizisi içinde ayrı bir dosya olarak döndürülür.  
- Büyük çalışma kitapları için asenkron işlem mevcuttur; işlem durumunu kontrol etmek için `202 Accepted` yanıtını kullanın.

## PostExport API’sini SDK’lar ile Nasıl Kullanılır

### Önkoşullar

API’yi çağırmadan önce, Aspose.Cells Cloud kimlik doğrulama akışını kullanarak geçerli bir JWT erişim belirteci edinin. Belirtecin her isteğin `Authorization` başlığında yer al.ensure SDK’lar, istemci kimlik bilgileriyle yapılandırıldığında belirteç edinmeyi otomatik olarak yönetir.

### PostExport API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir.

```bash
# Bir çalışma sayfasını TIFF formatına dışa aktarın
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, Aspose.Cells Cloud ile geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Desteklenen SDK’ların tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) ziyaret edin.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---