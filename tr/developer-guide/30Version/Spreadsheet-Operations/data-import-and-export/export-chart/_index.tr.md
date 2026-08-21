---
title: "Excel Grafiğini Dışa Aktar"
second_title: "Belge"
linktype: "Grafik"
type: docs
url: /tr/export-excel-chart-to-different-formats/
aliases: [  /tr/export/excel-chart-to-different-formats/ ]
description: "Aspose.Cells Cloud REST API'sini veya SDK'larını kullanarak Excel grafik nesnelerini PNG, JPEG, PDF, SVG, TIFF, EMF, WMF ve daha fazlası gibi popüler formatlara dışa aktarın. Kimlik doğrulama, cURL örneği ve birden fazla dil için kod örneklerini içerir."
keywords: "Aspose.Cells, grafik dışa aktar, Excel grafik dışa aktarımı, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, grafik formatları, Aspose Cells Cloud"
weight: 20
ArticleTitle: "Excel Grafiğini Dışa Aktar – Belge"
---

Bir Excel çalışma kitabından grafik nesnelerini çeşitli görüntü ve belge formatlarına dışa aktarmak, raporlama ve yayımlama süreçleri için yaygın bir ihtiyaçtır. Aspose.Cells Cloud, grafikleri doğrudan PNG, JPEG, PDF, SVG, TIFF, EMF, WMF ve daha fazlası gibi popüler formatlara dönüştüren basit bir REST uç noktası sağlar.

Grafikleri aşağıdaki formatlara dışa aktarabilirsiniz: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), ve [PDF](https://docs.fileformat.com/pdf/).

**Ön Gereksinimler:**  
- Aktif bir aboneliğe sahip geçerli bir Aspose.Cells Cloud hesabı.  
- Kimlik doğrulama akışıyla elde edilmiş bir OAuth 2.0 Bearer token (JWT).  
- Yüklenecek çalışma kitapığı dosyası (maksimum boyut < 50 MB).  

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Zorunlu | Açıklama                                                                                                                     |
|---------------|-------|-------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------|
| file          | dosya | formData                      | Evet    | Yüklenecek dosya                                                                                                             |
| objectType    | string | sorgu                         | Evet    | Dışa aktarılacak nesne türü. Grafik dışa aktarma için `chart` kullanın. Diğer olası değerler `worksheet`, `picture` vb.     |
| format        | string | sorgu                         | Evet    | İstenen çıktı formatı. Desteklenen değerler: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.              |

### **Yanıt**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                               |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | Tamam (OK)                  | Süzgeç başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek (Bad Request)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT token.                         |
| 413 | İstem Gövdesi Çok Büyük     | Yüklenecek dosya boyutu sınırını aşıyor.               |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                             |
## SDK'lar ile PostExport API Nasıl Kullanılır

### PostExport API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport), genel erişime açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Tüm istekler, `Authorization` başlığında geçerli bir OAuth 2.0 Bearer token içermelidir. Aşağıdaki örnek, API'yi **cURL** ile nasıl çağıracağınızı ve bir çalışma kitabını multipart/form‑data kullanarak nasıl yükleyeceğinizi göstermektedir.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. Bir SDK, düşük seviye detayları kendisi yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerine çeşitli SDK'lar kullanarak nasıl istekte bulunulacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}