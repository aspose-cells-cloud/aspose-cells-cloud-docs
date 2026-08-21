---
title: "Excel Çalışma Kitabında Metin Bulma"
second_title: "Belge"
linktitle: "Çalışma kitabında bul"
type: docs
url: /tr/workbook/find-text/
aliases: [  /tr/find-text-in-a-workbook/ ]
weight: 30
keywords: "Aspose.Cells, metin bul, Excel API, çalışma kitabında ara"
description: "Aspose.Cells Cloud API kullanarak Excel çalışma kitaplarında (XLS‑X, ODS) **metin bulmayı** öğrenin. cURL örneği, SDK kod parçaları ve yanıt şeması içerir. Hemen başlayın."
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Kitabında Metin Bulma"
---

Bu REST API, bir Excel çalışma kitabında metin arar.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/findText
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek Parametreleri

| Parametre Adı | Tür   | Konum | Açıklama                                                  |
| -------------- | ------ | -------- | ---------------------------------------------------------- |
| name           | string | path     | Excel çalışma kitabının adı.                                |
| text           | string | query    | Aranacak metin dizisi.                                 |
| folder         | string | query    | Çalışma kitabının bulunduğu klasör (isteğe bağlı).              |
| storageName    | string | query    | Çalışma kitabının bulunduğu depo adı (isteğe bağlı). |

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

| Kod | Anlam                       | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Geçersiz İstek                 | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Yetkisiz                      | Geçersiz veya eksik JWT belirteci. |
| 413  | Yük Çok Büyük                 | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | İç Sunucu Hatası              | Beklenmeyen sunucu hatası. |
## SDK’lar ile PostWorkbooksTextSearch API’yi Nasıl Kullanılır

### PostWorkbooksTextSearch API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksTextSearch" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API’yi çağırma yöntemini göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/findText?text=a" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <your_access_token>"
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

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye ayrıntıları işler böylece projenize odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub Deposu</a>’nu kontrol edin.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}
---