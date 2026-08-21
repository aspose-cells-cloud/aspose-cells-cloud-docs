---
title: "Excel Çalışma Sayfasında Sütunları Kopyalama"
second_title: "Belge"
linktitle: "Kopyala"
type: docs
url: /tr/columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, sütunları kopyalama, Excel API, REST, Bulut SDK’sı, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Aspose.Cells Cloud REST API’sini (v3.0) kullanarak bir Excel çalışma sayfasında bir veya daha fazla sütunu nasıl kopyalayacağınızı öğrenin. İsteğin sözdizimi, gerekli parametreler, kimlik doğrulama ayrıntıları, hata işleme ve C#, Java, Python, Ruby, Node.js, Go, Perl ve daha fazlası dillerinde SDK örneklerini içerir."
articleTitle: "Aspose.Cells Cloud API Kullanılarak Excel Çalışma Sayfasında Sütunların Kopyalanması"
weight: 30
---

Bu REST API, bir Excel çalışma sayfasında **sütunları** kopyalar. **Sütunları Kopyala** işlemi, tek bir sütunu veya bir sütun aralığını kopyalamanıza ve kopyalanan sütunları aynı çalışma sayfası içinde belirli bir konuma eklemenize olanak tanır. Büyük elektronik tablolarda çalışırken sütunları verimli bir şekilde kopyalamak için bu uç noktayı kullanın ve ek sütun yönetim görevleri için [Sütun Ekle](/columns/add/) ve [Sütunu Gizle](/columns/hide/) gibi ilgili işlemlere bakın.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### İstek Parametreleri

| Parametre Adı            | Tür      | Konum  | Açıklama                                                                              |
| ------------------------- | -------- | ------ | ------------------------------------------------------------------------------------- |
| **name**                  | string   | path   | Çalışma kitabının adı.                                                                |
| **sheetName**             | string   | path   | Çalışma sayfasının adı.                                                               |
| **sourceColumnIndex**     | integer  | query  | Kopyalanacak sütunun 0‑tabanlı indeksi.                                              |
| **destinationColumnIndex**| integer  | query  | Kopyalanan sütun(lar)ın ekleneceği 0‑tabanlı indeks.                                 |
| **columnNumber**          | integer  | query  | Kopyalanacak ardışık sütun sayısı.                                                    |
| **worksheet**             | string   | query  | _(İsteğe bağlı)_ Çalışma sayfası adı yoldan farklıysa kullanılan çalışma sayfası tanımlayıcısı. |
| **folder**                | string   | query  | Çalışma kitabının bulunduğu klasörün Aspose Cloud deposundaki yolu.                  |

Bu işlem için tam sözleşmeyi [OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) belgeleri sağlar.

### cURL Örneği

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### Yanıt

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Hata İşleme

API, hatayı açıklayan bir JSON yüküyle standart HTTP durum kodlarını döndürür.

| Durum Kodu | Anlam                                           | Örnek JSON Gövdesi                                                  |
| ---------- | ----------------------------------------------- | ------------------------------------------------------------------- |
| **400**    | Geçersiz istek – geçersiz parametreler          | `{ "Code": 400, "Message": "Geçersiz sütun indeksi." }`             |
| **401**    | Yetkisiz erişim – eksik veya geçersiz belirteç  | `{ "Code": 401, "Message": "Erişim belirteci geçersiz veya süresi dolmuş." }` |
| **404**    | Bulunamadı – çalışma kitabı veya çalışma sayfası yok | `{ "Code": 404, "Message": "Çalışma kitabı bulunamadı." }`          |
| **500**    | Sunucu iç hatası – beklenmedik durum            | `{ "Code": 500, "Message": "Beklenmeyen bir hata oluştu." }`       |

> **Nasıl Sorun Giderilir:** Erişim belirtecinin güncel olduğundan, çalışma kitabı ve çalışma sayfası adlarının doğru olduğundan ve `sourceColumnIndex`, `destinationColumnIndex` ile `columnNumber` değerlerinin çalışma sayfasının sütun aralığı içinde olduğundan emin olun.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, alt seviye ayrıntıları işler ve sizin projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Sütunları Kopyala API’sini çağırırken nasıl kimlik doğrulaması yaparım?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "OAuth2 erişim belirtecini, istemci kimliğinizi ve sırrınızı kullanarak Aspose Cloud’dan edinin ve istek başlığına `Authorization: Bearer <access_token>` olarak ekleyin."
      }
    },
    {
      "@type": "Question",
      "name": "`sourceColumnIndex` ile `destinationColumnIndex` arasındaki fark nedir?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex`, kopyalamak istediğiniz sütunun 0‑tabanlı indeksidir. `destinationColumnIndex`, kopyalanan sütun(lar)ın ekleneceği 0‑tabanlı indekstir."
      }
    },
    {
      "@type": "Question",
      "name": "Kopyalama işlemi başarısız olursa hangi yanıt alırım?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "API, 200 olmayan bir durum kodu (örneğin, 400 geçersiz istek, 401 yetkisiz erişim) döndürür. Yanıt gövdesi, hatayı açıklayan `Code` ve `Message` alanlarını içeren bir JSON nesnesi içerir."
      }
    }
  ]
}
</script>
---