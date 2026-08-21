---
title: "Çalışma Kitabına Bağlantı Ekle"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, bağlantı ekle, Excel REST API, bulut SDK"
description: "Aspose.Cells Cloud v3.0 REST API kullanarak bir Excel çalışma sayfasına bağlantı nasıl ekleneceğini öğrenin. Endpoint, tüm parametre kılavuzu, cURL örneği ve C#, Java, Python ve daha fazlası için SDK kod parçacıklarını içerir."
weight: 20
---

Bu REST API, bir Excel çalışma sayfasına bir bağlantı ekler.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### İstek Parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                                                                                  |
| ------------- | ------ | ----- | ----------------------------------------------------------------------------------------- |
| name          | string | path  | Belge adı.                                                                                |
| sheetName     | string | path  | Çalışma sayfası adı.                                                                      |
| firstRow      | integer| query | Bağlantının uygulanacağı aralığın ilk satırının sıfır tabanlı indeksi.                    |
| firstColumn   | integer| query | Bağlantının uygulanacağı aralığın ilk sütununun sıfır tabanlı indeksi.                    |
| totalRows     | integer| query | Bağlantı aralığının kapsadığı satır sayısı.                                               |
| totalColumns  | integer| query | Bağlantı aralığının kapsadığı sütun sayısı.                                               |
| address       | string | query | Bağlantının işaret ettiği hedef URL (URL kodlu).                                         |
| folder        | string | query | Belge klasörü.                                                                            |
| storageName   | string | query | Depo adı.                                                                                 |

İstek, aynı alanları içeren bir JSON gövdesi de içerebilir (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). Gövdeyi sağlamanız, sorgu dizgisi parametrelerine göre bir yük tercih ettiğinizde faydalı olur.

### Hata Yanıtları

| HTTP Kodu | Neden                                              | Örnek Gövde                                                         |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Geçersiz İstek – eksik veya geçersiz parametreler. | `{ "Code":"400", "Message":"Geçersiz parametre değeri." }`         |
| **401**   | Yetkisiz – eksik veya geçersiz JWT belirteci.     | `{ "Code":"401", "Message":"Erişim belirteci eksik veya geçersiz." }` |
| **404**   | Bulunamadı – çalışma kitabısı veya çalışma sayfası mevcut değil. | `{ "Code":"404", "Message":"Dosya bulunamadı." }`                     |
| **500**   | Sunucu iç hatası – beklenmeyen sunucu hatası.     | `{ "Code":"500", "Message":"Beklenmeyen bir hata oluştu." }`        |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink), genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye istekte bulunma yöntemini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

İstek başarısız olursa, API standart HTTP hata kodlarını (örn. 400 Geçersiz İstek, 401 Yetkisiz, 404 Bulunamadı, 500 Sunucu İç Hatası) ve içinde bir hata mesajı ve kodu içeren bir JSON yükünü döndürür.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye ayrıntıları yönetir; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini çeşitli SDK’lar kullanarak çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}