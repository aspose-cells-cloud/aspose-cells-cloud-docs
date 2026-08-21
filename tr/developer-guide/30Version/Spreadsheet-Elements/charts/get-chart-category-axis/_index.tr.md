---
title: "Grafik Kategori Ekseni Al"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, Grafik Kategori Ekseni, Excel, REST API, Bulut Depolama, OAuth2, API Dokümantasyonu"
description: "Aspose.Cells Cloud REST API kullanılarak bir Excel çalışma sayfasındaki bir grafikin kategori eksenini getirir."
ArticleTitle: "Grafik Kategori Ekseni Al – Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, bir grafikteki **Kategori Ekseni**'ni getirir.  
Bu uç noktayı çağırmak için geçerli bir OAuth 2.0 erişim belirteci sağlamalı ve çalışma kitabının Aspose Bulut depolamasında saklanmış olması gerekir.

**Ön Gereksinimler**  
Bu uç noktayı kullanmadan önce şunlardan emin olun:  

- OAuth 2.0 belirteci alınmış ve Aspose Bulut hizmetleri için geçerli olmalı.  
- Çalışma kitapğı dosyası Aspose Bulut depolamasına yüklenmiş olmalı (varsayılan veya belirtilen klasörde).  
- İstek URL'sinde gösterildiği gibi API sürümü **v3.0** kullanılıyor olmalı.  
- Çağrılan uygulamanın çalışma kitabını okuma ve çalışma sayfalarına erişme izni olmalı.

## GetChartCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**Arka Plan** – Bir çalışma sayfasından tüm grafikleri kaldırmak, bir sayfanın görsel düzenini sıfırlamanız, eski görselleştirmeleri değiştirmeniz veya önceki grafik verilerini korumadan bir çalışma kitabını yeniden kullanmaya hazırlamanız gerektiğinde faydalıdır.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                                               |
|---------------|--------|-------|--------------------------------------------------------|
| name          | string | path  | Çalışma kitapığı dosyasının adı.                       |
| sheetName     | string | path  | Grafik içeren çalışma sayfasının adı.                  |
| chartIndex    | integer| path  | Ekseni istenen grafik için sıfır tabanlı dizin.        |
| folder        | string | query | Çalışma kitabının bulunduğu depolamadaki klasör yolu.  |
| storageName   | string | query| Depolama hizmetinin adı (varsayılan değilse).          |

### **Yanıt**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                               |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |

## GetChartCategoryAxis API Nasıl SDK’larla Kullanılır?

### GetChartCategoryAxis API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK düşük seviye detayları yönetir ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# örneği yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java örneği yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP örneği yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby örneği yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python örneği yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android örneği yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift örneği yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl örneği yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go örneği yer tutucusu -->

{{< /tab >}}

{{< /tabs >}}