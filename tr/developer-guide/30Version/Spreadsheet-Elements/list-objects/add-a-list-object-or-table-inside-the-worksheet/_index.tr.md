---
title: "Bir Excel Çalışma Sayfasına Bir Liste Objesi (Tablo) Ekleyin"
second_title: "Belge"
linktitle: "Ekle"
type: docs
url: /tr/list-objects/add/
aliases: [  /tr/add-a-list-object-or-table-inside-the-worksheet/ , /tr/tables/add/ ]
keywords: "Aspose.Cells Cloud, Excel API, liste objesi, tablo, REST API, çalışma sayfası"
description: "Aspose.Cells Cloud REST API kullanarak bir çalışma sayfasına bir liste objesi (Excel tablosu) nasıl ekleyeceğinizi öğrenin. Uç nokta, parametreler, kimlik doğrulama adımları, cURL örneği ve SDK kod örneklerini içerir."
weight: 10
ArticleTitle: "Bir Excel Çalışma Sayfasına Bir Liste Objesi (Tablo) Ekleyin – Aspose.Cells Cloud Dokümantasyonu"
---

Bu REST API, bir Excel çalışma sayfasına bir **liste objesini (tabloyu)** ekler.

Bu uç noktayı kullanmadan önce geçerli bir JWT jetonuna sahip olduğunuzdan, çalışma kitabının desteklenen bir bulut depolama alanında tutulduğundan ve çalışma sayfasının mevcut olduğundan emin olun.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### İstek parametreleri

| Parametre Adı   | Tür     | Konum  | Açıklama                                                             |
| ---------------- | ------- | ------ | -------------------------------------------------------------------- |
| **name**         | string  | path   | Çalışma kitabı dosya adı.                                            |
| **sheetName**    | string  | path   | Çalışma sayfası adı.                                                 |
| **startRow**     | integer | query  | Tablo aralığının ilk satırının sıfır tabanlı indeksi.               |
| **startColumn**  | integer | query  | Tablo aralığının ilk sütununun sıfır tabanlı indeksi.              |
| **endRow**       | integer | query  | Tablo aralığının son satırının sıfır tabanlı indeksi.               |
| **endColumn**    | integer | query  | Tablo aralığının son sütununun sıfır tabanlı indeksi.              |
| **hasHeaders**   | boolean | query  | İlk satırda sütun başlıkları varsa `true`, aksi halde `false`.      |
| **listObject**   | object  | body   | Liste objesinin tanımı (bkz. **İstek gövdesi şeması**).             |
| **folder**       | string  | query  | Çalışma kitabını içeren klasör.                                      |
| **storageName**  | string  | query  | Depolama adı.                                                        |

### İstek gövdesi şeması

**listObject** nesnesi, oluşturulacak tabloyu tanımlar. En yaygın özellikleri gösterilmiştir; tam liste için OpenAPI spesifikasyonuna bakın.

```json
{
  "displayName": "MyTable",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### Örnek istek (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MyTable",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### Örnek yanıt

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Hata kodları

| HTTP Durumu | Neden                 | Açıklama                                          |
| ----------- | --------------------- | ------------------------------------------------- |
| **400**     | Bad Request (Geçersiz İstek) | Geçersiz aralık parametreleri veya bozuk JSON gövdesi. |
| **401**     | Unauthorized (Yetkisiz)      | Eksik veya süresi dolmuş JWT jetonu.              |
| **404**     | Not Found (Bulunamadı)       | Belirtilen çalışma kitabını veya çalışma sayfasını bulamadı. |
| **500**     | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu tarafı hatası.             |

**Örnek 400 yanıtı**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**Örnek 401 yanıtı**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

Bu işlem için tamcontract’ı [OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) sağlar.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en hızlı şekilde artıracaktır. Bir SDK, düşük seviye detayları işler ve projenizdeki görevlere odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)na bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerine istek yapmayı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}