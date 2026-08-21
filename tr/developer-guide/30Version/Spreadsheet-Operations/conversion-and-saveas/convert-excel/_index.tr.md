---
title: "Bir Excel Dosyasını Farklı Formatlara Dönüştürme"
ArticleTitle: "Bir Excel Dosyasını Farklı Formatlara Dönüştürme"
second_title: "Belge"
linktitle: "Excel'i Dönüştür"
type: docs
url: /tr/convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud, Excel dönüşümü, dosya formatı dönüşümü, REST API, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Aspose.Cells Cloud REST API’sini kullanarak Excel çalışma kitaplarını CSV, PDF, HTML, JSON, Markdown ve diğer formatlara dönüştürün."
weight: 10
---

Bu uç noktayı çağırmadan önce geçerli bir JWT belirteci elde ettiğinizden ve kaynak çalışma kitabının desteklenen bir depolama konumunda (örneğin Aspose Cloud Storage) bulunduğundan emin olun. Belirteci `Authorization` başlığına ekleyin ve gerekirse `storageName` sorgu parametresini belirtin.

Bu REST API, bir Excel dosyasını çeşitli çıktı formatlarına dönüştürür.

## PutConvertWorkBook API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

İstek, çok parçalı içerik içeren bir HTTP **PUT** isteğidir (bkz. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Çok parçalı gövdenin ilk parçası **veri dosyasını**, ikinci parçası ise **kaydetme seçeneklerini** içerir.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### Sorgu Parametreleri

| Parametre Adı           | Tür    | Açıklama                                                                                                                   |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | Hedef dosya formatı (örneğin CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG vb.).     |
| `password`              | string | Kaynak Excel dosyasını açmak için gereken parola.                                                                          |
| `outPath`               | string | Tek bir çıktı dosyası için tam yol (dosya adı ve uzantı dahil), birden fazla dosya oluşturulduğunda ise klasör yolu.       |
| `storageName`           | string | Kaynak dosyanın bulunduğu depolama adı.                                                                                   |
| `checkExcelRestriction` | bool   | **true** olarak ayarlandığında, hücreleri veya ilgili nesneleri değiştirmeden önce Excel kısıtlamalarını doğrular.        |
| `streamFormat`          | string | Girdi akış dosyasının formatı.                                                                                             |
| `region`                | string | Çalışma kitabına uygulanacak bölgesel ayarlar.                                                                            |
| `pageWideFitOnPerSheet` | bool   | PDF’e dönüştürürken sayfa genişliğini her bir çalışma sayfasına sığacak şekilde ayarlar.                                   |
| `pageTallFitOnPerSheet` | bool   | PDF’e dönüştürürken sayfa yüksekliğini her bir çalışma sayfasına sığacak şekilde ayarlar.                                 |
| `sheetName`             | string | Dönüştürülecek çalışma sayfasının adı.                                                                                     |
| `pageIndex`             | string | Dönüştürülecek sayfanın indeksi (`sheetName` gerektirir).                                                                 |
| `onePagePerSheet`       | bool   | **true** olarak ayarlandığında, her çalışma sayfası için bir PDF sayfası oluşturur.                                       |
| `AutoRowsFit`           | bool   | Çalışma kitabındaki tüm satırları otomatik olarak sığdırır.                                                                |
| `AutoColumnsFit`        | bool   | Çalışma kitabındaki sütun genişliklerini otomatik olarak sığdırır.                                                         |

### İstek Gövdesi Parametreleri

| Parametre Adı | Tür       | Açıklama                                                       |
| ------------- | --------- | -------------------------------------------------------------- |
| `datafile`    | data file | Çok parçalı gövdenin ilk parçasına yerleştirilen Excel dosyası. |
| `SaveOptions` | object    | Çok parçalı gövdenin ikinci parçasına yerleştirilen kaydetme seçenekleri. |

### **Yanıt**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                       |
|-----|-----------------------------|----------------------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.                             |
| 413 | İstek Gövdesi Çok Büyük     | Yüklenen dosya boyut sınırını aşıyor.                          |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası.                                     |

## PutConvertWorkBook API’sini SDK’lar ile Nasıl Kullanılır?

### PutConvertWorkBook API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), web tarayıcısından doğrudan REST etkileşimlerini mümkün kılan herkese açık bir arayüz tanımlar.

### cURL Örneği

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak düşük seviye detayları işleyerek geliştirme sürecini hızlandırır ve iş mantığına odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’larla Aspose.Cells web servislerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}