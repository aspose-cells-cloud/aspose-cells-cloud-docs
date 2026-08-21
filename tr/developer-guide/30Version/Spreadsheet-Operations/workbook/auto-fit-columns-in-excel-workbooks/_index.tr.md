---
title: "Excel dosyasında sütunları otomatik boyutlandırma"
second_title: "Belge"
linktitle: "Sütunlar"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "Sütunları otomatik boyutlandırma, Excel, Aspose.Cells Cloud, REST API, SDK, cURL, API"
description: "Aspose.Cells Cloud REST API’sini kullanarak bir Excel çalışma kitabında sütunları otomatik boyutlandırmanın nasıl yapılacağını öğrenin. İstek detaylarını, bir cURL örneğini ve birden fazla dil için SDK kod örneklerini içerir."
weight: 90
---

Bu REST API, bir Excel çalışma kitabında sütunları otomatik boyutlandırmayı destekler.

## PostAutofitWorkbookColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

İstek parametreleri:

| Parametre Adı         | Tür     | Konum  | Açıklama                                            |
| --------------------- | ------- | ------ | --------------------------------------------------- |
| **name**              | string  | path   | Çalışma kitabının dosya adı.                         |
| **autoFitterOptions** | object  | body   | Otomatik boyutlandırma davranışını denetleyen seçenekler. |
| **startColumn**       | integer | query  | Otomatik boyutlandırılacak ilk sütunun sıfır tabanlı indeksi. |
| **endColumn**         | integer | query  | Otomatik boyutlandırılacak son sütunun sıfır tabanlı indeksi. |
| **folder**            | string  | query  | Çalışma kitabını içeren klasör.                      |
| **storageName**       | string  | query  | Depolama hizmetinin adı.                            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} ortak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **Not:** Production ortamında her zaman HTTPS uç noktasını kullanın ve JWT belirtecinizi gizli tutun.

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

### Gereksinimler
Bu işlemi çağırmadan önce geçerli bir Aspose Cloud API anahtarına, oluşturulmuş bir JWT belirteçine ve hedef çalışma kitabının belirtilen depolama konumunda zaten mevcut olduğundan emin olun.

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK (Başarılı)               | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                 |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.         |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                 |

API aşağıdaki HTTP durum kodlarını döndürebilir:

| Kod | Açıklama                                      |
|-----|-----------------------------------------------|
| 200 | Başarılı – sütunlar otomatik boyutlandırıldı  |
| 400 | Bad request – eksik veya geçersiz parametreler |
| 401 | Unauthorized – geçersiz veya süresi dolmuş JWT |
| 500 | Server error – iç işlem başarısızlığı         |

## Bulut SDK Ailesi

Bir SDK kullanmak, geliştirmeyi hızlandırmanın en verimli yoludur. Bir SDK düşük seviyeli ayrıntıları işler, böylece proje mantığına odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerinin çeşitli SDK’lar kullanılarak nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}