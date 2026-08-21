---
title: "Grafik Değer Ekseni'ni Al"
type: docs
url: /tr/charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, Grafik Değer Ekseni, REST API, Excel, Bulut SDK, Grafik Değer Ekseni'ni Al
description: "Aspose.Cells Cloud REST API - Excel çalışma sayfasındaki bir grafiğin değer eksenini alma."
ArticleTitle: "Grafik Değer Ekseni'ni Al - Aspose.Cells Cloud REST API"
---

Bu REST API, bir grafiğin değer eksenini alır. **Aspose.Cells Cloud REST API**'nin bir parçasıdır ve bulutta depolanan Excel çalışma sayfalarıyla çalışır.

İlgili işlemler için **[Grafik Kategori Ekseni'ni Al](/charts/category-axis/get/)** uç noktasına bakın.

## GetChartValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                                                  |
|---------------|--------|-------|-----------------------------------------------------------|
| name          | string | path  | Excel dosyasının adı (uzantı dahil).                     |
| sheetName     | string | path  | Grafiğin bulunduğu çalışma sayfasının adı.               |
| chartIndex    | integer| path  | Çalışma sayfasındaki grafiğin sıfır tabanlı dizini.      |
| folder        | string | query | Dosyanın bulunduğu bulut depolama klasörü.               |
| storageName   | string | query | Depolama hizmetinin adı (örn. Aspose Cloud).             |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek yapmayı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
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
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Değerler",
    "Format": {
      "NumberFormat": "General",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**Mümkün HTTP durum kodları**

| Kod | Açıklama                                                      |
|-----|---------------------------------------------------------------|
| 200 | Başarılı – değer eksenine ait bilgiler döndürülür.            |
| 400 | Hatalı İstek – gerekli parametreler eksik veya geçersiz.     |
| 401 | Yetkisiz – kimlik doğrulama belirteci eksik veya geçersiz.   |
| 404 | Bulunamadı – belirtilen çalışma kitapçası, çalışma sayfası veya grafik mevcut değil. |
| 500 | İç Sunucu Hatası – sunucuda beklenmeyen bir hata oluştu.      |

Yanıt, `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title` ve `Format` gibi özelliklere sahip ayrıntılı bir `ValueAxis` nesnesi içerir. Tam bir uygulamada ek biçimlendirme detayları da sağlanabilir.

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, düşük seviye ayrıntıları işler; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine çeşitli SDK’larla nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# örnek yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java örnek yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP örnek yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby örnek yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python örnek yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android örnek yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift örnek yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl örnek yer tutucusu -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go örnek yer tutucusu -->

{{< /tab >}}

{{< /tabs >}}