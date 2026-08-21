---
title: "Çalışma Sayfasından Tüm Grafikleri Sil"
type: docs
url: /charts/clear/tr/
aliases: [/delete-all-charts-from-a-worksheet/tr/]
weight: 30
keywords: "Aspose.Cells, Bulut, sil, tüm grafikler, çalışma sayfası, REST API, DELETE, SDK"
description: "Aspose.Cells Cloud REST API (v3.0) kullanarak bir çalışma sayfasındaki tüm grafikleri nasıl sileceğinizi öğrenin. Uç nokta, parametreler, cURL örneği, SDK kod parçacıkları, kimlik doğrulama adımları ve hata işleme içerir."
ArticleTitle: "Aspose.Cells Cloud API ile Çalışma Sayfasından Tüm Grafikleri Sil"
---

Bu REST API, belirtilen çalışma sayfasından tüm grafikleri siler.

**Arka Plan** – Bir çalışma sayfasından tüm grafikleri silmek, bir sayfanın görsel düzenini sıfırlamanız, güncel olmayan görselleştirmeleri değiştirmeniz veya önceki grafik verilerini korumadan bir defteri yeniden kullanmaya hazırlamanız gerektiğinde faydalıdır.

API’yi çağırmadan önce aşağıdaki önkoşulların karşılandığından emin olun:

- Kimlik doğrulama için geçerli bir JWT jetonuna sahip olunuz.  
- Defter dosyası, belirtilen depolama konumunda ve klasörde mevcuttur.  
- **v3.0** API sürümünü kullanıyorsunuz.

## DeleteWorksheetClearCharts API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür     | Konum  | Açıklama                              |
|---------------|---------|--------|---------------------------------------|
| name          | string  | path   | Defter dosyasının adı.                |
| sheetName     | string  | path   | Çalışma sayfasının adı.               |
| folder        | string  | query  | Defterin depolandığı klasör.          |
| storageName   | string  | query  | Depolamanın adı.                      |

**İstek Başlıkları**

| Başlık          | Açıklama                         |
|-----------------|----------------------------------|
| Authorization   | Bearer `<jwt token>`             |
| Accept          | `application/json`               |
| Content-Type    | `application/json` (gövde yok)  |

**İstek Gövdesi**

DELETE işlemi bir **istek gövdesi gerektirmez**.

**Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT jetonu.                           |
| 413 | Payload Too Large (Yük Çok Büyük) | Yüklenen dosya boyut sınırını aşıyor.                  |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                           |

*Örnek hata yanıtları*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Geçersiz parametre: 'sheetName' gerekli."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Kimlik doğrulama başarısız oldu. Geçersiz JWT jetonu."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "İstek yükü maksimum izin verilen boyutu aşıyor."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "Sunucuda beklenmeyen bir hata oluştu."
}
```

## SDK’lar ile DeleteWorksheetClearCharts API’yi Nasıl Kullanılır

### DeleteWorksheetClearCharts API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```


{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Aspose.Cells Cloud SDK’larını Kullanma

Bir çalışma sayfasından **tüm grafikleri silmeniz** gerektiğinde SDK’ları kullanmak geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine istek nasıl yapılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---