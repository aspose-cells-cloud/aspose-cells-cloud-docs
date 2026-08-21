---
title: "Bir Excel çalışma kitabından metin öğelerini alın"
ArticleTitle: "Aspose.Cells Cloud API kullanarak bir Excel Çalışma Kitabından Metin Öğelerini Alın"
second_title: "Belge"
linktitle: "Çalışma kitabından metin öğelerini al"
type: docs
url: /workbook/get-text-items/
aliases: [/get-text-items-from-a-workbook/]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, Elektronik Tablo, Metin Öğelerini Al, Çalışma Kitabı"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabından metin öğelerini alın. C#, Java, Python, PHP, Ruby, Go, Node.js, Perl ve Swift için SDK’lar aracılığıyla kullanılabilir."
---


## REST API

Bu REST API, bir Excel dosyasındaki bir çalışma kitabının **metin öğelerini** okur.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek parametreleri

| Parametre Adı  | Tür    | Konum | Açıklama                                            |
| -------------- | ------ | ----- | ---------------------------------------------------- |
| name           | string | path  | Çalışma kitabının dosya adı.                         |
| folder         | string | query | Çalışma kitabının bulunduğu depolama dizin yolu.     |
| storageName    | string | query | Depolama hizmetinin adı.                            |

### **Yanıt**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |
## SDK’lar ile GetWorkbookTextItems API’sini Nasıl Kullanılır

### GetWorkbookTextItems API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye bir çağrı nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

Tipik HTTP yanıt kodları:

| Kod | Açıklama                                     |
|-----|----------------------------------------------|
| 200 | İstek başarılı; metin öğeleri döndürülür.    |
| 401 | Unauthorized – eksik veya geçersiz belirteç. |
| 403 | Forbidden – yetersiz izinler.                |
| 404 | Not Found – çalışma kitabı veya kaynak bulunamadı. |
| 500 | Internal Server Error – beklenmeyen hata.    |

### Aspose.Cells Cloud SDK’larını Kullanma

Bu örnek **v3.0** API sürümünü kullanır; yeni sürümler için değişiklik notlarına bakın. SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}
---