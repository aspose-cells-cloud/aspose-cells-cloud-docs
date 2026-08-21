---
title: "Grafik İkinci Değer Ekseni Alma"
type: docs
url: /tr/charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, grafik ikinci değer ekseni, Excel, REST API, bulut, API, Excel grafik ekseni
description: Aspose.Cells Cloud REST API kullanılarak bir Excel çalışma sayfasındaki belirli bir grafiğin ikinci değer ekseni alınır.
ArticleTitle: "Grafik İkinci Değer Ekseni Alma – Aspose.Cells Cloud API"
---

Bu REST API, bir grafiğin ikinci değer eksenini alır.

## GetChartSecondValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür      | Konum   | Açıklama                                      |
| ------------- | -------- | ------- | --------------------------------------------- |
| name          | string   | path    | Excel dosyasının adı.                         |
| sheetName     | string   | path    | Grafiğin bulunduğu çalışma sayfasının adı.    |
| chartIndex    | integer  | path    | Grafiğin sıfır tabanlı indeksi.               |
| folder        | string   | query   | Dosyanın bulunduğu klasör.                    |
| storageName   | string   | query   | Aspose Cloud depo adı.                        |

**Önkoşullar**: Her isteğin `Authorization` başlığına, Aspose Cloud OAuth2 akışı ile elde edilmiş geçerli bir JWT erişim belirteci verilmesi gerekir.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapıldığını göstermektedir. Tüm Aspose Cloud endpoint’leri HTTPS gerektirir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
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
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "İkinci Değer Ekseni"
  }
}
```

**Yanıt Alanları**

- **Code** – İşlemin HTTP durum kodu (örneğin, başarı durumunda `200`).  
- **Status** – Durumun metinsel açıklaması (başarı durumunda `"OK"`).  
- **Axis** – İkinci değer eksenine ait ayrıntıları içeren nesne:  
  - **AxisId** – Eksenin tanımlayıcısı.  
  - **IsVisible** – Eksenin gösterilip gösterilmediğini belirten boole değer.  
  - **MinimumScale** – Eksende gösterilen minimum değer.  
  - **MaximumScale** – Eksende gösterilen maksimum değer.  
  - **MajorUnit** – Ana ölçek çizgileri arasındaki aralık.  
  - **MinorUnit** – Yardımcı ölçek çizgileri arasındaki aralık.  
  - **Title** – Eksenin başlık metni.

**Hata Yanıtları** (200 dışındaki durumlar)

- `400 Bad Request` – Geçersiz parametreler veya bozuk istek.  
- `401 Unauthorized` – Eksik veya geçersiz JWT belirteci.  
- `404 Not Found` – Belirtilen dosya, çalışma sayfası veya grafik mevcut değil.  
- `500 Internal Server Error` – Beklenmeyen sunucu hatası.

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Paketi Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve size proje görevlerinize odaklanma imkânı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
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