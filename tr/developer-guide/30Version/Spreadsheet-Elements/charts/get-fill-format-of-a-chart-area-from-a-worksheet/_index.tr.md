---
title: "Chart Alanı Doldurma Biçimini Al – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /tr/charts/chart-area/fill-format/get/
aliases: [/tr/charts/chart-area/fill-format/get/]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Chart Alanı"
  - "Doldurma Biçimi"
  - "REST API"
  - "Excel"
description: "Aspose.Cells Cloud API aracılığıyla bir Excel çalışma sayfasındaki bir grafik alanının doldurma biçimini (renk, desen, gradyan) alın. cURL örneği, SDK kod parçacıkları, kimlik doğrulama adımları ve yanıt detaylarını içerir."
ArticleTitle: "Chart Alanı Doldurma Biçimini Al – Aspose.Cells Cloud API v3.0"
---

Bu REST API, bir **Chart Alanı**'nın doldurma biçimi bilgilerini getirir.

**Ön Koşullar**  
Bu uç noktayı çağırmak için geçerli bir OAuth/JWT erişim belirteciniz olmalıdır. Belirteci, Aspose.Cells Cloud kimlik doğrulama akışını kullanarak edinin ve `Authorization` başlığına `Bearer <jwt token>` olarak ekleyin. SDK’lardan birini kullanıyorsanız, yöntemi çağırmadan önce SDK’nızın `client_id` ve `client_secret` ile yapılandırıldığını kontrol edin.

## GetChartAreaFillFormat API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                              |
| ------------- | ------ | ----- | ------------------------------------- |
| name          | string | path  | Çalışma kitabının adı.                |
| sheetName     | string | path  | Çalışma sayfasının adı.               |
| chartIndex    | integer| path  | Grafin indeksi.                       |
| folder        | string | query | Çalışma kitabını içeren klasör.       |
| storageName   | string | query | Depo adı.                             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, API’yi cURL ile nasıl çağıracağınızı gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**Notlar**  
- Başarılı bir çağrı, HTTP 200 durum koduyla doldurma biçimi detaylarını döndürür.  
- HTTP 401, kimlik doğrulama hatasını (geçersiz veya eksik belirteç) gösterir.  
- HTTP 404, belirtilen çalışma kitabı, çalışma sayfası veya grafik indeksi bulunamadığında döner.  
- HTTP 500, sunucu tarafında bir hata olduğunu belirtir; sorun devam ederse isteği yeniden deneyin veya destek ile iletişime geçin.

| Kod | Anlam                                               |
|-----|-----------------------------------------------------|
| 200 | Başarılı – doldurma biçimi döndürüldü               |
| 401 | Yetkisiz – geçersiz veya eksik belirteç             |
| 404 | Bulunamadı – çalışma kitabı, çalışma sayfası veya grafik bulunamadı |
| 500 | İç Sunucu Hatası                                    |

İlgili işlemler için **Get Chart Area Border** ve **Get Chart Title** uç noktalarına bakın.

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en iyi şekilde artırmak için en iyi yoldur. SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini çeşitli SDK’larla nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}