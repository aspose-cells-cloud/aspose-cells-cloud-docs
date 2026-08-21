---
title: "Birden Fazla Excel Çalışma Sayfasını Silme"
second_title: "Belge"
linktitle: "Birden fazla çalışma sayfası"
type: docs
url: /tr/worksheets/delete-multiple/
aliases: [  /tr/delete-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, birden fazla çalışma sayfasını silme, Excel API, REST API, v3.0, çalışma sayfalarını silme"
description: "Aspose.Cells Cloud REST API (v3.0) kullanarak bir Excel çalışma kitabından birden fazla çalışma sayfasını nasıl sileceğinizi öğrenin. Güvenli HTTPS uç noktası, gerekli parametreler, düzeltildi cURL örneği ve birden fazla programlama dili için SDK parçacıkları içerir."
weight: 20
ArticleTitle: "Aspose.Cells Cloud REST API Kullanılarak Birden Fazla Excel Çalışma Sayfasını Silme"
---

Bu REST API, bir çalışma kitabından birden fazla çalışma sayfasını siler.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **İstek parametreleri**

| Parametre Adı   | Tür     | Konum | Açıklama                                                           |
| --------------- | ------- | ----- | ------------------------------------------------------------------ |
| name            | string  | path  | Excel dosyasının adı.                                              |
| matchCondition  | object  | body  | Hangi çalışma sayfalarının silineceğini belirleyen bir `MatchConditionRequest` nesnesi. |
| folder          | string  | query | Dosyanın bulunduğu depoda klasör yolu.                             |
| storageName     | string  | query | Depolama hizmetinin adı.                                           |

**MatchConditionRequest Özellikleri**

| Ad                  | Tür       | Açıklama                                 | Notlar     |
| ------------------- | --------- | ---------------------------------------- | ---------- |
| RegexPattern        | string    | Çalışma sayfası adlarını eşleştirmek için normal ifade. | isteğe bağlı |
| FullMatchConditions | string[]  | Silinecek tam çalışma sayfası adları.    | isteğe bağlı |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets), genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir. **`Authorization` başlığında geçerli bir JWT belirteci gerekir.**

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

İstek, aşağıdaki gibi yaygın hata yanıtları da döndürebilir:

| HTTP Durumu | Anlam                                        | Örnek Yük                                                  |
| ----------- | -------------------------------------------- | ---------------------------------------------------------- |
| 400         | Geçersiz istek – geçersiz JSON veya parametreler | `{"Code":400,"Message":"Invalid request payload."}`        |
| 401         | Yetkisiz erişim – eksik veya geçersiz JWT belirteci | `{"Code":401,"Message":"Authentication failed."}`          |
| 403         | Yetki reddedildi – yetersiz izinler          | `{"Code":403,"Message":"Access denied."}`                  |
| 404         | Bulunamadı – dosya veya çalışma sayfası yok  | `{"Code":404,"Message":"Resource not found."}`             |
| 500         | Sunucu iç hatası                             | `{"Code":500,"Message":"An unexpected error occurred."}`   |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Grubu

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bakınız:**  
- [Tek Bir Çalışma Sayfasını Silme](https://docs.aspose.cloud/cells/worksheets/delete/)  
- [Çalışma Sayfasını Kopyalama](https://docs.aspose.cloud/cells/worksheets/copy/)  
- [Çalışma Sayfasını Taşıma](https://docs.aspose.cloud/cells/worksheets/move/)  
---