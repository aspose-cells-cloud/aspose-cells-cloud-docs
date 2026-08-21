---
title: "Grafiğin İkinci Kategori Ekseni Güncelleme"
type: docs
url: /tr/charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart, Second Category Axis, REST API, Update Chart, Excel, Cloud API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki bir grafiğin ikinci kategori eksenini nasıl güncelleyeceğinizi öğrenin."
ArticleTitle: "Grafiğin İkinci Kategori Ekseni Güncelleme – Aspose.Cells Cloud API"
---

Bu REST API, bir grafiğin ikinci kategori eksenini günceller.

## PostChartSecondCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür     | Konum | Açıklama                                               |
| ------------- | ------- | ----- | ------------------------------------------------------ |
| name          | string  | path  | Excel dosyasının adı.                                 |
| sheetName     | string  | path  | Grafiği içeren çalışma sayfasının adı.                |
| chartIndex    | integer | path  | Güncellenecek grafiğin sıfır tabanlı dizini.          |
| axis          | object  | body  | Yeni ayarları içeren ikinci kategori eksenine ait nesne. |
| folder        | string  | query | Dosyanın depolandığı klasör yolu.                     |
| storageName   | string  | query | Depolama hizmetinin adı.                              |

**Kimlik Doğrulama** – API, geçerli bir OAuth 2.0 erişim belirtecini gerektirir. JWT belirtecini oluşturmak için [Kimlik Doğrulama Kılavuzu](https://docs.aspose.cloud/cells/authentication/)’nu izleyin. Belirteci aşağıdaki cURL örneğinde gösterildiği gibi `Authorization` başlığında dahil edin.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* axis ayarları, örneğin "Title": "Yeni Eksen Başlığı", "IsVisible": true */
        }
      }'
```

*`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}` ve `{storageName}` değerlerini gerçek değerlerinizle değiştirin. İstek gövdesi, istenen ayarları içeren `axis` nesnesini içermelidir.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Başarılı yanıt (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "Yeni Eksen Başlığı",
      "IsVisible": true,
      /* ek eksen özellikleri */
    }
  }
}
```

**Hata yanıtları**  

| Durum Kodu | Açıklama                                        |
|------------|-------------------------------------------------|
| 400        | Geçersiz istek – eksik veya geçersiz parametreler. |
| 401        | Yetkisiz erişim – geçersiz veya eksik JWT belirteci. |
| 404        | Bulunamadı – belirtilen dosya, çalışma sayfası veya grafik mevcut değil. |
| 500        | Sunucu iç hatası – sunucuda beklenmeyen bir koşul oluştu. |

```json
{
  "Code": 400,
  "Message": "Geçersiz istek yükü."
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

SDK’lar düşük seviye detayları işleyerek geliştirme sürecini kolaylaştırır ve iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerine istek nasıl yapılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# örnek yer tutucu -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java örnek yer tutucu -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP örnek yer tutucu -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby örnek yer tutucu -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python örnek yer tutucu -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android örnek yer tutucu -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift örnek yer tutucu -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl örnek yer tutucu -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go örnek yer tutucu -->

{{< /tab >}}

{{< /tabs >}}

**Notlar ve En İyi Uygulamalar**

* `chartIndex` parametresi sıfır tabanlıdır; bir çalışma sayfasındaki ilk grafik dizini 0’dır.  
* API, hem `.xlsx` hem de `.xls` çalışma kitap formatlarını destekler.  
* `axis` nesnesine yalnızca ihtiyaç duyduğunuz özellikleri ekleyin; belirtilmeyen özellikler mevcut değerlerini korur.  
* Hız sınırlamasından kaçınmak için hız sınırlama yönergelerine (genellikle hesap başına dakikada 100 istek) uyun.