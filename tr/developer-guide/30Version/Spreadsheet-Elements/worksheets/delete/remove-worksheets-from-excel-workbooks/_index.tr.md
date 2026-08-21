---
title: "Çalışma Sayfasını Sil"
second_title: "Belge"
linktitle: "Tek bir çalışma sayfası"
type: docs
url: /tr/worksheets/delete-worksheet/
aliases: [  /tr/remove-worksheets-from-excel-workbooks/ ]
keywords: "Aspose.Cells Cloud, Çalışma Sayfası Sil, Excel, Elektronik Tablo, REST API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabından bir çalışma sayfasını silin. C#, Java, PHP, Ruby, Node.js, Python, Perl, Go ve cURL için SDK'ları destekler."
weight: 20
ArticleTitle: "Çalışma Sayfasını Sil – Aspose.Cells Cloud API"
---

Bu REST API, bir çalışma sayfasını siler.  
Önkoşullar: Bu API’yi çağırmak için **Authorization** başlığında geçerli bir JWT kimlik doğrulama belirteci sağlamalı ve çalışma kitabının bulunduğu depolama konumuna erişim izniniz olmalıdır.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*Not: API, şu anda kararlı sürüm olan **v3.0** sürümünü kullanır. Gelecek sürüm değişiklikleri, sürüm notlarında duyurulacaktır.*

### **İstek Parametreleri**

| Parametre Adı | Tür   | Konum | Açıklama             |
| ------------- | ----- | ----- | -------------------- |
| name          | string | path  | Belge adı.           |
| sheetName     | string | path  | Çalışma sayfası adı. |
| folder        | string | query | Belgenin klasörü.    |
| storageName   | string | query | Depo adı.            |

Olası HTTP yanıtları:

| Durum Kodu | Açıklama                                      |
| ---------- | --------------------------------------------- |
| 200 OK     | Çalışma sayfası başarıyla silindi.            |
| 400 Bad Request | Geçersiz istek parametreleri.            |
| 401 Unauthorized | Kimlik doğrulama başarısız oldu veya belirteç eksik. |
| 404 Not Found | Belirtilen çalışma kitabı veya çalışma sayfası mevcut değil. |
| 500 Internal Server Error | Beklenmeyen sunucu hatası. |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapılır gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Tüm istekler HTTPS üzerinden yapılmalıdır; API, TLS olmayan bağlantıları desteklemez.*

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

## Bulut SDK Geliştirme Kiti

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları işler; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}