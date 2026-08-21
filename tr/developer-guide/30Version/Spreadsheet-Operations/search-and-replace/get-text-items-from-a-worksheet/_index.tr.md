---
title: "Excel Çalışma Sayfasından Metin Öğelerini Alın"
second_title: "Belge"
linktitle: "Çalışma Sayfasında Metin Öğelerini Alın"
type: docs
url: /tr/worksheets/get-text-items/
aliases: [  /tr/get-text-items-from-a-worksheet/ ]
weight: 20
keywords: "Aspose.Cells, Bulut API, Excel, çalışma sayfası, metin öğeleri, REST"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel dosyasındaki belirli bir çalışma sayfasından tüm metin öğelerini alın. Örnek cURL, SDK kodu, kimlik doğrulama adımları ve yanıt şemasını içerir."
ArticleTitle: "Excel Çalışma Sayfasından Metin Öğelerini Alın"
---

## REST API

Bu REST API, bir Excel dosyasındaki bir çalışma sayfasının metin öğelerini okur.

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT token tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

### İstek Parametreleri


| Parametre Adı | Tür   | Konum | Gerekli | Açıklama                                      |
| -------------- | ------ | -------- | -------- | ---------------------------------------------- |
| name           | string | path     | Evet      | Çalışma kitapası dosyasının adı.                            |
| sheetName      | string | path     | Evet      | Çalışma sayfasının adı.                         |
| folder         | string | query    | Hayır       | Çalışma kitabını içeren klasörün yolu. |
| storageName    | string | query    | Hayır       | Aspose Cloud depo adı.              |

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
| 200  | Başarılı (OK)                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Geçersiz İstek (Bad Request)                 | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Yetkisiz (Unauthorized)                | Geçersiz veya eksik JWT token. |
| 413  | Yük Çok Büyük (Payload Too Large)           | Yüklenecek dosya boyut sınırını aşıyor. |
| 500  | İç Sunucu Hatası (Internal Server Error)       | Beklenmeyen sunucu hatası. |
## SDK'larla GetWorksheetTextItems API Nasıl Kullanılır

### GetWorksheetTextItems API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"}, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
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

### Aspose.Cells Cloud SDK'larını Kullanın

SDK’lar, düşük seviye detayları işleyerek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}

---