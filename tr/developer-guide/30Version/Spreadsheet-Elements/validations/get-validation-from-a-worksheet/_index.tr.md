---
title: "Excel çalışma sayfasından bir dizine göre çalışma sayfası doğrulaması alma"
second_title: "Belge"
linktitle: "Al"
type: docs
url: /validations/get/
aliases: [/get-validation-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, çalışma sayfası doğrulama API'si, dizine göre doğrulama alma, Excel REST API, Aspose.Cells SDK"
description: "Aspose.Cells Cloud API'sini (v3.0) kullanarak bir Excel defterinden sıfır tabanlı dizine göre bir çalışma sayfası doğrulaması alın. cURL örneği, yanıt şeması, hata kodları ve C#, Java, Python ve daha fazlası için SDK snippet'leri içerir."
weight: 10
---

Bu REST API, bir Excel çalışma sayfasında bir dizine göre çalışma sayfası doğrulamasını getirir.  
Uç noktayı çağırmadan önce `/connect/token` uç noktasından bir JWT jetonu edinin ve `Authorization` başlığına `Bearer <jwt token>` olarak ekleyin.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **İstek parametreleri**

| Parametre Adı   | Tür      | Konum | Açıklama                                            |
| --------------- | -------- | ----- | --------------------------------------------------- |
| name            | string   | path  | Defter dosyasının adı.                              |
| sheetName       | string   | path  | Çalışma sayfasının adı.                             |
| validationIndex | integer  | path  | Alınacak doğrulamanın sıfır tabanlı indeksi.        |
| folder          | string   | query | Defterin bulunduğu klasör.                          |
| storageName     | string   | query | Depolama hizmetinin adı.                            |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation), herkese açık bir erişilebilir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, API'yi cURL ile nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Yanıt şeması**

| Alan           | Tür       | Açıklama                                                            |
| -------------- | --------- | ------------------------------------------------------------------- |
| AlertStyle     | string    | Kullanıcıya gösterilen uyarı stili (Stop, Warning, Information).   |
| AreaList       | dizi      | Doğrulamanın uygulandığı hücre aralıkları koleksiyonu.             |
| IgnoreBlank    | boolean   | `true` ise, doğrulama sırasında boş hücreler göz ardı edilir.       |
| InCellDropDown | boolean   | `true` ise, hücrede bir açılır liste görüntülenir.                  |
| Operator       | string    | Doğrulama için kullanılan karşılaştırma operatörü (örn. `None`, `Between`). |
| ShowError      | boolean   | Doğrulama başarısız olduğunda bir hata mesajının gösterilip gösterilmeyeceğini belirler. |
| ShowInput      | boolean   | Hücre seçildiğinde bir giriş mesajının gösterilip gösterilmeyeceğini belirler. |
| Type           | string    | Doğrulama türü (örn. `AnyValue`, `WholeNumber`, `Decimal`, vb.).   |
| link.Href      | string    | Doğrulama kaynağının kendine referans URL'si.                       |
| link.Rel       | string    | İlişki türü (her zaman `self`).                                    |

**Olası hata kodları**

| HTTP Durumu | Anlam                                                               |
| ----------- | ------------------------------------------------------------------- |
| 200         | Doğrulama başarıyla alındı.                                         |
| 400         | Geçersiz istek – eksik veya geçersiz parametreler.                 |
| 401         | Yetkisiz istek – geçersiz veya eksik JWT jetonu.                   |
| 404         | Bulunamadı – defter, çalışma sayfası veya doğrulama indeksi yok.    |
| 500         | İç sunucu hatası – beklenmeyen durum.                               |

## Bulut SDK Ailesi

Aspose.Cells Cloud ile geliştirmenin en hızlı yolu bir SDK kullanmaktır. Bir SDK, düşük seviyeli detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK'lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}