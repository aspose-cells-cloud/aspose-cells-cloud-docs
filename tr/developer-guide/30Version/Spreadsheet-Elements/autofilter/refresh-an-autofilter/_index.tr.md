---
title: "Excel Çalışma Sayfasında Otomatik Filtreyi Yenile"
second_title: "Belge"
linktitle: "Otomatik filtreyi yenile"
type: docs
url: /tr/autofilter/refresh/
aliases: [  /tr/refresh-an-autofilter/ ]
weight: 100
keywords: "Aspose.Cells, AutoFilter, yenile, Excel, API, REST"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki mevcut Otomatik Filtreyi yenileyin. C#, Java, Python ve daha fazlası için cURL ve SDK örnekleri içerir."
ArticleTitle: "Excel Çalışma Sayfasında Otomatik Filtreyi Yenile"
---

### **Yenile** işlemi ne yapar?

Uç noktayı çağırmak, çalışma sayfası verileri değiştiğinde (örneğin satır eklendiğinde veya silindiğinde) geçerli filtre kriterlerini tekrar uygular. İşlem, filtre tanımını değiştirmez; yalnızca görünümü günceller ve bir durum yanıtı döndürür.

### REST API

Bu REST API, bir Excel çalışma sayfasındaki otomatik filtreyi yeniler (API sürümü **v3.0**).

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası. |

*Örnek hata yanıtları*  

```json
// 400 Geçersiz İstek
{
    "Code": 400,
    "Message": "Geçersiz parametre: sheetName bulunamadı."
}

// 401 Yetkisiz
{
    "Code": 401,
    "Message": "Kimlik doğrulama başarısız. JWT belirteci eksik veya geçersiz."
}

// 413 Yük Çok Büyük
{
    "Code": 413,
    "Message": "Yüklenen dosya maksimum izin verilen boyutu aşıyor."
}

// 500 İç Sunucu Hatası
{
    "Code": 500,
    "Message": "Sunucuda beklenmeyen bir hata oluştu."
}
```

## SDK’lar ile PostWorksheetAutoFilterRefresh API’sini Nasıl Kullanılır

### PostWorksheetAutoFilterRefresh API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye ayrıntıları yönetir ve size proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine istek nasıl yapılacağını göstermektedir:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}
---