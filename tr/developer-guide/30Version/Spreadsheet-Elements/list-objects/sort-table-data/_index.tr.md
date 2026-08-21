---
title: "Excel Çalışma Sayfasındaki ListObject Verilerini Sırala"
second_title: "Belge"
linktitle: "Sırala"
type: docs
url: /list-objects/sort-data/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/, /tables/sort-data/]
keywords: "Aspose.Cells Cloud, Excel, ListObject, Veri Sıralama, REST API, Çalışma Sayfası"
description: "Aspose.Cells Cloud REST API (v3.0) kullanarak Excel çalışma sayfasındaki ListObject (tablo) verilerini nasıl sıralayacağınızı öğrenin. Uç nokta, parametreler, örnek cURL isteği ve SDK örneklerini içerir."
weight: 40
ArticleTitle: "Excel Çalışma Sayfasındaki ListObject Verilerini Sırala – Aspose.Cells Cloud API"
---

**Ön Gereksinimler**  
Bu API’yi çağırmak için geçerli bir Aspose Cloud JWT erişim belirteciniz olmalı ve çalışma kitabının Aspose Cloud deposuna yüklenmiş olması gerekir. Her istekte `Authorization: Bearer <jwt token>` başlığını ekleyin.

Bu REST API, Excel çalışma sayfasındaki bir tablonun verilerini sıralar.  
Bu işlemi kullanmak için çalışma kitabının adını, çalışma sayfasının adını ve hedef ListObject’in indeksini sağlayın. Ayrıca sıralama kriterlerini tanımlayan bir `dataSorter` JSON gövdesi de ekleyin.

## PostWorksheetListObjectSortTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı   | Tür      | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                       |
|-----------------|----------|------------------------------|----------------------------------------------------------------------------------------------------------------|
| name            | string   | path                         | Aspose Cloud deposunda saklanan Excel dosyasının adı.                                                         |
| sheetName       | string   | path                         | ListObject’i içeren çalışma sayfasının adı.                                                                    |
| listObjectIndex | integer  | path                         | Çalışma sayfasındaki ListObject’in (tablonun) sıfır tabanlı indeksi.                                          |
| dataSorter      | object   | body                         | Sıralama seçeneklerini belirten JSON nesnesi (örn. `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`). |
| folder          | string   | query                        | Excel dosyasının bulunduğu depodaki klasör yolu.                                                               |
| storageName     | string   | query                        | Aspose Cloud deposunun adı.                                                                                    |

**Notlar**  
İstek gövdesi, `dataSorter` şemasıyla eşleşen geçerli bir JSON nesnesi olmalıdır. Sıralama işlemini çağırmadan önce çalışma kitabının, çalışma sayfasının ve ListObject’in mevcut olduğundan emin olun.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
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

**HTTP Durum Kodları**

| Durum Kodu | Açıklama                                        |
|------------|-------------------------------------------------|
| 200        | OK – sıralama işlemi başarıyla tamamlandı.     |
| 400        | Bad Request – geçersiz parametreler.           |
| 401        | Unauthorized – kimlik doğrulama başarısız oldu.|
| 404        | Not Found – çalışma kitabını, çalışma sayfasını veya ListObject’i bulamadı. |
| 500        | Internal Server Error – sunucu tarafında sorun.|

**Yanıt Parametreleri**

| Parametre | Tür     | Açıklama                                   |
|-----------|---------|---------------------------------------------|
| Code      | integer | API tarafından döndürülen HTTP durum kodu.  |
| Status    | string  | Sonucun metinsel açıklaması (örn. "OK").    |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[ListObjects Genel Bakış’a Geri Dön](/list-objects/)
---