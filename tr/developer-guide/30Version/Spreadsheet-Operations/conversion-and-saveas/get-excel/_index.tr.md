---
title: "Aspose.Cells Cloud – Excel Çalışma Kitabını PDF, CSV, HTML ve Daha Fazlasına Dönüştürün (GET /cells/{name})"
second_title: "Belge"
linktitle: "Excel Dönüştür"
type: docs
url: /get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel dönüştürme, Excel dönüştür, PDF, CSV, HTML, ODS, JSON, görüntü formatları, elektronik tablo dışa aktarma, API, REST"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabını herhangi bir formatta (PDF, CSV, HTML, PNG vb.) nasıl alacağınızı öğrenin. cURL, SDK örnekleri, kimlik doğrulama ve yanıt ayrıntılarını içerir."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – Excel Çalışma Kitabını PDF, CSV, HTML ve Daha Fazlasına Dönüştürün (GET /cells/{name})"
---

Bu REST API, bir Excel çalışma kitabını farklı bir formatta getirir.

## GetWorkBook API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **Sorgu Parametreleri**

| Parametre Adı        | Tür    | Açıklama                                                                                                                                                                          | Varsayılan |
| --------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| format                | string | Hedef dosya formatı (örn. CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG vb.).                 | –         |
| password              | string | Excel dosyasını açmak için gereken şifre.                                                                                                                                        | –         |
| isAutoFit             | bool   | Satır ve sütun genişliklerini otomatik olarak ayarlar.                                                                                                                           | false     |
| onlySaveTable         | bool   | **true** olarak ayarlandığında sadece tablo verileri kaydedilir. `true` veya `false` değerlerini kabul eder.                                                                      | false     |
| outPath               | string | Sonucun kaydedileceği yol. Tek bir dosya için dosya adı ve uzantı; birden fazla dosya için sadece klasör belirtilir.                                                               | –         |
| outStorageName        | string | Çıktı dosyasının kaydedileceği depo adı.                                                                                                                                         | –         |
| checkExcelRestriction | bool   | Hücreleri veya ilgili nesneleri değiştirirken Excel kısıtlamalarını denetler.                                                                                                     | false     |
| region                | string | Çalışma kitabına uygulanacak bölgesel ayarlar.                                                                                                                                   | –         |
| pageWideFitOnPerSheet | bool   | PDF'e dönüştürürken sayfa genişliğini her bir çalışma sayfasına sığdırır.                                                                                                         | false     |
| pageTallFitOnPerSheet | bool   | PDF'e dönüştürürken sayfa yüksekliğini her bir çalışma sayfasına sığdırır.                                                                                                       | false     |
| onePagePerSheet       | bool   | Her çalışma sayfası için bir PDF sayfası oluşturur.                                                                                                                               | false     |
| folder                | string | Orijinal çalışma kitabının bulunduğu klasör yolu.                                                                                                                                | –         |
| storageName           | string | Kaynak dosyanın bulunduğu depo adı.                                                                                                                                              | –         |

### Yanıt

**Başarılı (200)** 

- `format` sorgu parametresi atlandığında API, çalışma yapısı bilgilerini içeren bir **[Workbook](/cells/workbook/)** nesnesi döndürür.

- `format` sorgu parametresi bir dosya türünü belirttiğinde API, istenen formatta dönüştürülmüş dosyayı döndürür.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(binary PDF data)
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                     |
|-----|-----------------------------|--------------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                           |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.                         |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                   |

> **Notlar:**  
> - Büyük çalışma kitaplarının dönüştürülmesi daha uzun sürebilir; istek zaman aşımını artırmayı düşünün.  
> - Bazı formatlar (örn. `ODS`), makrolar gibi belirli Excel özellikler için desteklenmez.

## SDK’lar ile GetWorkBook API Nasıl Kullanılır

> **Önkoşullar:**  
> - Aspose.Cells kimlik doğrulama akışı aracılığıyla alınmış geçerli bir **JWT erişim belirteci**.  
> - Kaynak çalışma kitabı, desteklenen bir Aspose deposunda depolanmış olmalı veya doğrudan isteğe dahil edilmeli.  
> - API sürümünün (`v3.0`) en son yayınlanan sürümle eşleştiğinden emin olun.

### GetWorkBook API Belirtimi

<a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">OpenAPI Belirtimi</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Örnek İstek

Aspose.Cells web hizmetlerine erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, gerekli yetkilendirme başlığı ile doğru bir GET isteğini göstermektedir.

{{< tabs tabTotal="1" tabID="11" tabName11="İstek" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye ayrıntıları soyutlayarak projenizin görevlerine odaklanabilmenizi sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca Bakınız**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Çalışma Kitabını Dönüştür (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Farklı Kaydet (GET)</a>

---

_Son Güncelleme: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Excel Çalışma Kitabını PDF, CSV, HTML ve Daha Fazlasına Dönüştürün (GET /cells/{name})",
  "description": "Excel çalışma kitaplarını PDF, CSV, HTML ve daha fazlası gibi çeşitli formatlara dönüştüren Aspose.Cells Cloud GET /cells/{name} uç noktası için belge.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, Excel dönüştürme, PDF, CSV, HTML, API, REST, bulut",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---