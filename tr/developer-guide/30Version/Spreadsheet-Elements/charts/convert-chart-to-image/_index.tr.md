---
title: "Excel Grafğini Görüntüye Dönüştür – Aspose.Cells Cloud REST API"
type: docs
url: /charts/to-image/
aliases: [/convert-charts-to-image/]
weight: 50
keywords: "Aspose.Cells Cloud, grafikten görüntüye, Excel grafik dönüştürme, REST API, görüntü formatı, PNG, JPEG, BMP, TIFF, GIF"
description: "Aspose.Cells Cloud REST API kullanarak Excel grafik nesnelerini PNG, JPEG, BMP, TIFF veya GIF Görüntü formatlarına nasıl dönüştüreceğinizi öğrenin. Uç nokta detaylarını, parametreleri, cURL örneğini, SDK kod parçacıklarını, yanıt örneğini ve hata işleme bilgilerini içerir."
ArticleTitle: "Excel Grafğini Görüntüye Dönüştür – Aspose.Cells Cloud REST API"
---

Bu REST API, bir **Excel grafiğini** bir görsel formatına dönüştürmenin nasıl yapıldığını **Aspose.Cells Cloud** kullanarak göstermektedir.

## PutWorksheetAddChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

Desteklenen görüntü formatları şunlardır: `png`, `jpeg`, `bmp`, `tiff` ve `gif`.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                   |
| ------------- | ------ | ----- | -------------------------- |
| name          | string | path  | Belge adı.                 |
| sheetName     | string | path  | Çalışma sayfası adı.       |
| chartNumber   | integer| path  | Grafik numarası.           |
| format        | string | query | Dışa aktarılan dosya formatı. |
| folder        | string | query | Belge klasörü.             |
| storageName   | string | query | Depo adı.                  |

### **Yanıt**

Uç nokta, istenen formatı ikili akış olarak (örneğin `byte[]`) döndürür. Yanıt `Content-Type` başlığı, seçilen görüntü formatına göre `image/png`, `image/jpeg` vb. değerler alır.

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK (Tamam)                  | Sü 필터 başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                   |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırlarını aşıyor.            |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                         |

## PutWorksheetAddChart API'yi SDK’larla Nasıl Kullanılır

### PutWorksheetAddChart API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek atacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoluudur. Bir SDK, düşük seviye detayları yönetir ve sizin proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

Örnek yakında gelecek.

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}
---