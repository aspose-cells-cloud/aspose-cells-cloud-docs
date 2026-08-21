---
title: "Excel Çalışma Sayfasında Grafik Başlığını Güncelleme"
type: docs
url: /charts/title/update/
aliases: [/update-chart-title-in-excel-worksheet/]
weight: 160
keywords: Excel, Aspose.Cells, REST API, Grafik Başlığı, Güncelleme, Bulut SDK'sı
description: Aspose.Cells Cloud REST API, cURL ve çeşitli SDK'lar kullanarak Excel çalışma sayfasında bir grafik başlığını nasıl güncelleyeceğinizi öğrenin.
ArticleTitle: "Excel Çalışma Sayfasında Grafik Başlığını Güncelleme – Aspose.Cells Cloud Dokümantasyonu"
---

Bu REST API, grafik başlığını günceller.

**Ön Gereksinimler:** Geçerli bir Aspose Cloud hesabınız ve yetkilendirme için bir JWT jetonuna sahip olmalısınız. Tipik adımlar şunları içerir:

- Aspose Cloud hesabına kaydolun.  
- Kimlik doğrulama uç noktası aracılığıyla bir JWT jetonu oluşturun.  
- Hedef çalışma kitabının desteklenen bir bulut depolama alanına (varsayılan veya özel) kaydedildiğinden emin olun.

## PostWorksheetChartTitle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

Tüm API çağrıları, karışık içerik uyarılarını önlemek için **HTTPS** üzerinden yapılmalıdır.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür      | Konum  | Açıklama                               |
| ------------- | -------- | ------ | -------------------------------------- |
| name          | string   | path   | Çalışma kitabı adı.                    |
| sheetName     | string   | path   | Çalışma sayfası adı.                   |
| chartIndex    | integer  | path   | Grafik için sıfır tabanlı dizin.       |
| title         | string   | body   | Yeni grafik başlığı.                   |
| folder        | string   | query  | Çalışma kitabının bulunduğu klasör.    |
| storageName   | string   | query  | Depo adı.                              |

### Yanıt Durum Kodları

| Kod  | Açıklama                                           |
| ---- | -------------------------------------------------- |
| 200  | Tamam – Grafik başlığı başarıyla güncellendi.     |
| 400  | Hatalı İstek – Eksik veya geçersiz parametreler.  |
| 401  | Yetkisiz – Geçersiz veya eksik JWT jetonu.        |
| 404  | Bulunamadı – Çalışma kitabı, çalışma sayfası veya grafik bulunamadı. |
| 500  | İç Sunucu Hatası – Beklenmeyen sunucu durumu.      |

**Not:** `chartIndex` sıfır tabanlıdır; bir çalışma sayfasındaki ilk grafik `0` ile referans alınır.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Borsa"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}
---