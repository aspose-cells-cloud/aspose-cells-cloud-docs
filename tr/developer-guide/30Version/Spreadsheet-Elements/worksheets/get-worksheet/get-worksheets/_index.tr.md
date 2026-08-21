---
title: "Tüm Çalışma Sayfalarını Al"
second_title: "Belge"
linktitle: "Tümü"
type: docs
url: /worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, Bulut API, Çalışma Sayfalarını Al, Excel, REST, SDK"
description: "Aspose.Cells Cloud REST API (v3.0) aracılığıyla bir Excel çalışma kitabındaki çalışma sayfalarının listesini alın. cURL örneği, SDK kod parçacıkları ve yanıt formatını içerir."
weight: 10
---

Bu REST API, bir çalışma kitabında bulunan çalışma sayfaları hakkında bilgi verir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **İstek Parametreleri**

| Parametre Adı  | Tür    | Konum | Açıklama                             |
| -------------- | ------ | ----- | ------------------------------------ |
| name           | string | path  | Excel belgesinin adı.                |
| folder         | string | query | Belgeyi içeren klasör.               |
| storageName    | string | query | Kullanılacak depo adı.               |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells Cloud hizmetlerine erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, çalışma sayfalarını almak için bir GET isteğini göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Hata Yönetimi

Bu uç noktanın döndürdüğü tipik HTTP durum kodları:

| Kod  | Anlamı               | Açıklama                                  |
| ---- | -------------------- | ----------------------------------------- |
| 400  | Hatalı İstek         | Gerekli parametre eksik (örn. `name`).    |
| 401  | Yetkisiz             | Geçersiz veya eksik JWT belirteci.        |
| 404  | Bulunamadı           | Belirtilen çalışma kitabı mevcut değil.   |
| 500  | Sunucu İç Hatası     | Beklenmeyen sunucu durumu.                |

Hata yanıtları JSON formatında döndürülür; örneğin:

```json
{
  "Code": "401",
  "Message": "Geçersiz erişim belirteci."
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}