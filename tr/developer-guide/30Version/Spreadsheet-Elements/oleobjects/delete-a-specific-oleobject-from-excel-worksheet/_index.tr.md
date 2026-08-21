---
title: "Bir Excel çalışma sayfasından bir OLE nesnesini silin"
second_title: "Belge"
linktitle: "Sil"
type: docs
url: /tr/oleobjects/delete/
aliases: [/tr/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells, Bulut, Sil, OLE, Nesne, Excel, çalışma sayfası, REST, API, SDK"
description: "Aspose.Cells Cloud REST API'sini (v4.0) kullanarak bir Excel çalışma sayfasından bir OLE nesnesini nasıl sileceğinizi öğrenin. HTTPS uç noktası, kimlik doğrulama adımları, cURL örneği, SDK kod parçacıkları, hata işleme yönergeleri ve sonraki adımlar için bağlantıları içerir."
weight: 50
ArticleTitle: "Aspose.Cells Cloud API kullanılarak Excel Çalışma Sayfasından OLE Nesnesi Silme"
---

Bu sayfa, bir Excel defterindeki bir çalışma sayfasından belirli bir OLE nesnesini **Aspose.Cells Cloud** kullanarak nasıl sileceğinizi açıklar. Bir OLE nesnesi, Excel'in ayrı bir varlık olarak depoladığı bağlı bir resim, grafik veya gömülü herhangi bir nesne olabilir.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### İstek Parametreleri

| Parametre adı | Tür      | Konum | Açıklama                                            |
| ------------- | -------- | ----- | --------------------------------------------------- |
| name          | string   | path  | Defter adı.                                         |
| sheetName     | string   | path  | Çalışma sayfası adı.                                |
| oleObjectIndex| integer  | path  | Silinecek OLE nesnesinin dizini.                    |
| folder        | string   | query | Defteri içeren klasör. (isteğe bağlı)              |
| storageName   | string   | query | Depolama hizmetinin adı. (isteğe bağlı)            |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject), herkese açık erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL komut satırı aracını** kullanabilirsiniz. Aşağıdaki örnek, cURL ile bu isteği nasıl yapacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Yanıt ayrıntıları

| HTTP durumu          | Açıklama                                                          | Örnek JSON                                                         |
| -------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| **200 OK**           | OLE nesnesi başarıyla silindi.                                    | `{ "Code": 200, "Status": "OK" }`                                 |
| **401 Unauthorized** | Eksik veya geçersiz JWT belirteci.                                | `{ "Code": 401, "Message": "Erişim belirteci eksik veya geçersiz." }` |
| **404 Not Found**    | Belirtilen defter, çalışma sayfası veya OLE nesnesi dizini yok.   | `{ "Code": 404, "Message": "OLE nesnesi dizini aralık dışında." }` |
| **400 Bad Request**  | Gerekli parametreler eksik veya hatalı.                           | `{ "Code": 400, "Message": "Geçersiz istek parametreleri." }`    |

Uygulamanızda bu yanıtları, durum kodunu kontrol ederek ve eşlik eden mesajı göstererek ele alın.

## Bulut SDK Ailesi
SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları işler böylece projenizdeki görevlere odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}