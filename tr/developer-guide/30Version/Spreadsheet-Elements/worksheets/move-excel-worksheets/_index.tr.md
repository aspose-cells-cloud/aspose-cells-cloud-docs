---
title: "Bir Excel Çalışma Sayfasını Taşı – Aspose.Cells Cloud API (v3.0)"
second_title: "Belge"
linktitle: "Taşı"
type: docs
url: /tr/worksheets/move/
aliases: [  /tr/move-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, Çalışma Sayfası Taşı, Excel, REST API, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "Aspose.Cells Cloud API’si (v3.0) ile bir Excel çalışma sayfasını yeni bir konuma taşımayı öğrenin. Uç nokta, gerekli parametreler, cURL örneği ve C#, Java, Python ve diğerleri için SDK kodlarını içerir."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API v3.0 ile Bir Excel Çalışma Sayfasını Nasıl Taşırız?"
---

Bu REST API, bir Excel çalışma kitabında bir çalışma sayfasını başka bir konuma taşır.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### İstek Parametreleri

| Parametre Adı | Tür   | Konum | Açıklama                                                                                                           |
| ------------- | ----- | ----- | ------------------------------------------------------------------------------------------------------------------ |
| name          | string | path  | Excel dosyasının adı.                                                                                              |
| sheetName     | string | path  | Taşınacak çalışma sayfasının adı.                                                                                  |
| moving        | object | body  | Hedef çalışma sayfasını (`DestinationWorksheet`) ve göreli konumu (`Position`) belirten JSON nesnesi.              |
| folder        | string | query | Çalışma kitabının depolandığı klasör yolu.                                                                         |
| storageName   | string | query | Depolama hizmetinin adı.                                                                                           |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerini çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, tek bir istek ile bir çalışma sayfasını nasıl taşıyacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                     | Açıklama                                      |
|-----|----------------------------|-----------------------------------------------|
| 200 | OK (Tamam)                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)    | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yükleme dosyası boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

**Örnek Hata Yükü**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Gerekli parametre eksik: 'moving'."
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yönetir; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}