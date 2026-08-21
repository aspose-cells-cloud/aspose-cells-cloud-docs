---
title: "Çalışma Sayfasında Paste Seçenekleriyle Aralık Kopyalama"
second_title: "Belge"
linktitle: "Kopyala"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Aspose.Cells Cloud, REST API, Excel, aralık kopyalama, çalışma sayfası, paste seçenekleri"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında bir aralığı tam paste-seçeneği desteğiyle kopyalayın. Birden fazla programlama dili için SDK örneklerini içerir."
weight: 20
ArticleTitle: "Çalışma Sayfasında Paste Seçenekleriyle Aralık Kopyalama – Aspose.Cells Cloud API"
---

Bu REST API, bir Excel çalışma kitabının bir çalışma sayfasında bir aralığı kopyalar. İlgili işlemler için **Aralığı Al** ve **Aralığı Güncelle** belgelerine bakın.

**Ön Gereksinimler:** Bu uç noktayı kullanmak için geçerli bir OAuth 2.0 / JWT belirteciniz olmalı ve API sürümünüzün istek URL'siyle eşleştiğinden emin olmalısınız.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **İstek Parametreleri**

| Parametre Adı | Tür     | Konum | Açıklama                                                                     |
|---------------|---------|-------|------------------------------------------------------------------------------|
| name          | string  | path  | Çalışma kitabının adı.                                                       |
| sheetName     | string  | path  | Çalışma sayfasının adı.                                                      |
| rangeOperate  | string  | body  | Gerçekleştirilecek işlem: `copydata`, `copystyle`, `copyto` veya `copyvalue`. |
| folder        | string  | query | Çalışma kitabının bulunduğu klasör.                                          |
| storageName   | string  | query | Depolama hizmetinin adı.                                                     |

**Notlar:** `rangeOperate` alanı, neyin kopyalanacağını belirler. Yalnızca hücre değerlerini kopyalamak için `copydata`, biçimlendirmeyi kopyalamak için `copystyle`, hem veriyi hem de stili kopyalamak için `copyto` ve formüller olmadan değerleri kopyalamak için `copyvalue` kullanın. API, 1 milyon hücreye kadar olan aralıkları destekler; daha büyük aralıklar zaman aşımına neden olabilir.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopyCopy), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Başarılı yanıt, `200 OK` durum kodunu döndürür. Hata durumunda API aşağıdaki gibi yükleri döndürebilir:

```json
{
  "Code": 400,
  "Message": "Bad Request – geçersiz parametreler."
}
```

veya

```json
{
  "Code": 401,
  "Message": "Unauthorized – kimlik doğrulama belirteci eksik veya geçersiz."
}
```

Bu hata nesneleri, sorunların tanılanmasına yardımcı olacak HTTP durum kodunu ve açıklayıcı bir mesajı içerir.

{{< /tab >}}

{{< /tabs >}}

Kopyalama işlemini test etmek için bir örnek çalışma kitabını [buradan](https://example.com/sample.xlsx) indirebilirsiniz.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları işler böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}