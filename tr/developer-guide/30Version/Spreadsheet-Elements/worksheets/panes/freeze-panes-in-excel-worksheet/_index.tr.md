---
title: "Excel Çalışma Sayfasında Bölmeleri Dondurma"
second_title: "Belge"
linktitle: "Dondur"
type: docs
url: /tr/worksheets/panes/freeze/
aliases: [  /tr/freeze-panes-in-excel-worksheet/ , /tr/worksheets/freeze-panes/ ]
keywords: "Aspose.Cells Cloud, Bölmeleri Dondurma, Excel, REST API, Çalışma Sayfası"
description: "Aspose.Cells Cloud REST API ile bir Excel çalışma sayfasında satır ve sütunları nasıl donduracağını öğrenin. Uç nokta sözdizimi, gerekli parametreler, cURL örneği, kimlik doğrulama yönlendirmesi, hata yanıt ayrıntıları ve birden fazla dil için SDK kod örneklerini içerir."
weight: 190
---

Bu REST API, bir Excel çalışma sayfasında bölmeleri **dondurur**.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

İstek parametreleri:

| Parametre Adı | Tür      | Konum  | Açıklama                                            |
| ------------- | -------- | ------ | --------------------------------------------------- |
| name          | string   | path   | Çalışma kitabının dosya adı.                        |
| sheetName     | string   | path   | Bölmelerin dondurulacağı çalışma sayfasının adı.    |
| row           | integer  | query  | İlk **dondurulmamış** satırın sıfır tabanlı indeksi. |
| column        | integer  | query  | İlk **dondurulmamış** sütunun sıfır tabanlı indeksi. |
| frozenRows    | integer  | query  | Üstten itibaren dondurulacak satır sayısı.          |
| frozenColumns | integer  | query  | Soldan itibaren dondurulacak sütun sayısı.          |
| folder        | string   | query  | Çalışma kitabının bulunduğu depolama klasör yolu.   |
| storageName   | string   | query  | Depolama hizmetinin adı.                            |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### Hata Yanıtı

| HTTP Durumu               | Kod | Mesaj                           | Örnek                                                    |
| ------------------------- | --- | ------------------------------- | -------------------------------------------------------- |
| 400 Bad Request           | 400 | Geçersiz parametreler           | `{ "Code": 400, "Message": "Geçersiz frozenRows değeri" }` |
| 401 Unauthorized          | 401 | Eksik veya geçersiz JWT jetonu  | `{ "Code": 401, "Message": "Geçersiz erişim jetonu" }`   |
| 404 Not Found             | 404 | Çalışma kitabını veya çalışma sayfasını bulamadı | `{ "Code": 404, "Message": "Dosya bulunamadı" }` |
| 500 Internal Server Error | 500 | Beklenmeyen sunucu hatası       | `{ "Code": 500, "Message": "İç sunucu hatası" }`         |

## Bulut SDK Geliştirme Seti Ailesi

Bir SDK kullanmak, geliştirme hızını en çok artıran en iyi yoldur. Bir SDK, düşük seviye ayrıntıları işler; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine farklı SDK’lar kullanarak nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}