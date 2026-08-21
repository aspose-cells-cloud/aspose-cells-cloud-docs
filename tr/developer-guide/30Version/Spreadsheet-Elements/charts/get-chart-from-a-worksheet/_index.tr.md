---
title: "Çalışma Sayfasından Grafik Al"
type: docs
url: /tr/charts/get/
aliases: [  /tr/get-chart-from-a-worksheet/ ]
weight: 10
keywords: "Aspose.Cells Cloud, Grafik Al, Çalışma Sayfası, REST API, Excel, Grafik API, grafik alma, Excel grafik"
description: "Aspose.Cells Cloud REST API kullanarak bir çalışma sayfasından grafik bilgilerini, meta verileri ve dışa aktarma formatını alın."
ArticleTitle: "Çalışma Sayfasından Grafik Al – Aspose.Cells Cloud API"
---

Bu REST API, grafik bilgilerini alır.

**Ön Gereksinimler** – Bu uç noktayı çağırmak için geçerli bir Aspose.Cells Cloud hesabınız, aktif bir depolama konumunuz ve JWT erişim belirteciniz olmalıdır. Herhangi bir API isteğinde bulunmadan önce, kimlik doğrulama kılavuzundaki talimatları takip ederek belirteci edinin.

## GetWorksheetChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı  | Tür     | Konum | Açıklama                                       |
| -------------- | ------- | ----- | ---------------------------------------------- |
| name           | string  | path  | Excel dosyasının adı.                          |
| sheetName      | string  | path  | Grafiği içeren çalışma sayfasının adı.         |
| chartNumber    | integer | path  | Alınacak grafiğin sıfır tabanlı indeksi.       |
| format         | string  | query | İstenen dışa aktarma formatı (örn. png, jpeg). |
| folder         | string  | query | Belgenin depolandığı klasör yolu.              |
| storageName    | string  | query | Depolama hizmetinin adı.                       |


### **Yanıt**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Grafik 1",
    "Type": "Çubuk",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                   |
|-----|-----------------------------|------------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                         |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırlarını aşıyor.                  |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                              |

## GetWorksheetChart API'sini SDK'larla Nasıl Kullanılır

### GetWorksheetChart API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Grafik 1",
    "Type": "Çubuk",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanın

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine istek yapmayı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}