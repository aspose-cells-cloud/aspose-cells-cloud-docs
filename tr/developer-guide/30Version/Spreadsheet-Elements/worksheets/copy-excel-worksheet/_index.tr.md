---
title: "Bir diğer çalışma sayfasından içeriği ve formatları kopyala."
second_title: "Belge"
linktitle: "Kopyala"
type: docs
url: /tr/worksheets/copy/
aliases: [  /tr/copy-excel-worksheet/ ]
keywords: "Aspose Cells kopyalama çalışma sayfası API'si, Excel sayfa kopyalama REST API'si, Aspose Cloud SDK kopyalama, elektronik tablo kopyalama çalışma sayfası"
description: "Aspose.Cells Cloud REST API kullanarak bir çalışma sayfasını ve formatlarını yeni bir sayfaya nasıl kopyalayacağınızı öğrenin. C#, Java, Python ve diğerleri için uç nokta, parametreler, cURL ve SDK örneklerini içerir."
weight: 20
---

Bu REST API, bir çalışma sayfasını ve formatlarını aynı çalışma kitabında yeni bir sayfaya kopyalar.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı    | Tür    | Konum  | Açıklama                                                                 |
| ---------------- | ------ | ------ | ------------------------------------------------------------------------ |
| `name`           | string | path   | Çalışma kitabı dosyasının adı.                                           |
| `sheetName`      | string | path   | Hedef çalışma sayfasının (yeni sayfanın) adı.                            |
| `sourceSheet`    | string | query  | Kopyalanacak çalışma sayfasının adı.                                     |
| `options`        | object | body   | Kopyalama seçeneklerini içeren JSON nesnesi (örn., sütun genişliği, formüller). |
| `sourceWorkbook` | string | query  | Kaynak çalışma kitabının adı, mevcut çalışma kitabından farklıysa.      |
| `sourceFolder`   | string | query  | Kaynak çalışma kitabının bulunduğu klasör yolu.                          |
| `folder`         | string | query  | Hedef çalışma kitabının kaydedileceği klasör yolu.                       |
| `storageName`    | string | query  | Kullanılacak depolama hizmetinin adı.                                    |

### İstek ve Yanıt Örnekleri

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
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

### Hata Yönetimi

API, standart HTTP durum kodlarını ve JSON hata gövdesini döndürür. Typik yanıtlar şunları içerir:

| HTTP Kodu | Açıklama                                                       | Örnek JSON Hata Gövdesi                                        |
| --------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| 400       | Hatalı istek – eksik veya geçersiz parametreler.               | `{ "Code": 400, "Message": "Geçersiz istek parametreleri." }`   |
| 401       | Yetkisiz erişim – eksik veya geçersiz belirteç.                | `{ "Code": 401, "Message": "Kimlik doğrulama başarısız." }`     |
| 404       | Bulunamadı – çalışma kitabı, çalışma sayfası veya klasör mevcut değil. | `{ "Code": 404, "Message": "Kaynak bulunamadı." }`           |
| 500       | İç sunucu hatası – beklenmeyen durum.                          | `{ "Code": 500, "Message": "Beklenmeyen bir hata oluştu." }`   |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en çok artıracak en iyi yoldur. SDK, düşük seviye ayrıntıları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine çeşitli SDK'lar kullanılarak nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}