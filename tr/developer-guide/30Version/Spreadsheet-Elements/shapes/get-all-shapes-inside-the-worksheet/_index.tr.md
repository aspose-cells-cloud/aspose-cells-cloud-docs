---
title: "Bir Excel Çalışma Sayfasındaki Tüm Şekilleri Al"
second_title: "Belge"
linktitle: "Tümünü-al"
type: docs
url: /shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: "Aspose.Cells, Bulut API, Excel şekilleri, şekilleri al, REST, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir çalışma sayfasından tüm şekilleri (grafikler, resimler, metin kutuları) alma. cURL örneği, SDK kod parçacıkları, kimlik doğrulama adımları ve hata yönetimi içerir."
ArticleTitle: "Bir Excel Çalışma Sayfasındaki Tüm Şekilleri Al"
weight: 10
---

Bu REST API, bir Excel çalışma sayfasındaki tüm şekilleri alma işlemini sağlar.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### İstek Parametreleri

| Parametre Adı   | Tür     | Konum  | Açıklama                                                                                             |
| ---------------- | ------- | ------ | ---------------------------------------------------------------------------------------------------- |
| **name**         | string  | path   | Excel dosyasının adı.                                                                                |
| **sheetName**    | string  | path   | Çalışma sayfasının adı.                                                                              |
| **folder**       | string  | query  | Belgenin bulunduğu klasör.                                                                           |
| **storageName**  | string  | query  | Kullanılacak depolama hizmetinin adı.                                                               |
| **include**      | string  | query  | `details` olarak ayarlandığında tam şekil özelliklerini döndürür; aksi takdirde yalnızca `link` nesneleri döner. |

> **İsteğe Bağlı**: Dosya kök depolama alanında yer alıyorsa `folder`, `storageName` ve `include` parametreleri atlanabilir.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine erişebilirsiniz. Aşağıdaki örnek, isteğe bağlı sorgu parametrelerini içeren bir istek göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Yanıt Alanları

`Shapes` nesnesi, `Shape` ögelerinin bir listesini içerir. Her şekil, aşağıdaki özelliklere sahiptir (`include=details` bayrağı kullanıldığında); aksi takdirde yalnızca `link` nesnesi döner.

| Özellik   | Tür     | Açıklama                                                                     |
| ---------- | ------- | ---------------------------------------------------------------------------- |
| **Name**   | string  | Şekile atanan ad (örn. “Chart 1”).                                           |
| **Type**   | string  | Şekil türü (örn. `Chart`, `Picture`, `TextBox`).                            |
| **Top**    | number  | Çalışma sayfasının üst kenarından şeye kadar olan uzaklık (nokta cinsinden). |
| **Left**   | number  | Çalışma sayfasının sol kenarından şeye kadar olan uzaklık (nokta cinsinden). |
| **Width**  | number  | Şeklin genişliği (nokta cinsinden).                                          |
| **Height** | number  | Şeklin yüksekliği (nokta cinsinden).                                         |
| **Link**   | object  | Hiperbağlantı bilgisi (`Href`, `Rel`, `Type`, `Title`).                     |

## Hata Yönetimi

| HTTP Durumu | Açıklama                                              | Örnek Hata Gövdesi                                                |
| ----------- | ----------------------------------------------------- | ----------------------------------------------------------------- |
| **400**     | Geçersiz istek – hatalı parametreler.                | `{ "Code": 400, "Message": "Geçersiz parametre değeri." }`       |
| **401**     | Yetkisiz erişim – eksik veya geçersiz belirteç.      | `{ "Code": 401, "Message": "Erişim belirteci eksik veya geçersiz." }` |
| **404**     | Bulunamadı – çalışma kitapçası veya çalışma sayfası yok. | `{ "Code": 404, "Message": "Dosya veya çalışma sayfası bulunamadı." }` |
| **500**     | İç sunucu hatası – beklenmeyen durum.                | `{ "Code": 500, "Message": "Beklenmeyen bir hata oluştu." }`     |

Başarılı bir istek, yukarıdaki yanıt örneğinde gösterildiği gibi, şekillerin listesini içeren bir `Shapes` nesnesi ile **HTTP 200** durum kodu döner.

API, her JWT belirteci başına **dakikada 150 istek** sınırını uygular. Bu sınırı aşmak, yeniden deneme zamanını belirten bir `Retry-After` başlığı ile **HTTP 429** döndürür.

## Bulut SDK Grubu

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, düşük seviye ayrıntıları yönetir ve size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerine istek yapmayı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}
---