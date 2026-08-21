---
title: "Excel Çalışma Sayfasında Bir Liste Objesini Güncelleme"
ArticleTitle: "Excel Çalışma Sayfasında Bir Liste Objesini Güncelleme – Aspose.Cells Cloud API Dokümantasyonu"
second_title: "Belge"
linktitle: "Güncelle"
type: docs
url: /list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, Tablo Güncelle, Excel API, REST, Bulut SDK, liste nesnesi güncelleme, Excel çalışma sayfası, tablo"
description: "Aspose.Cells Cloud API’sini (v3.0) kullanarak bir Excel tablosunu nasıl güncelleyeceğinizi öğrenin. Uç nokta, parametreler, örnek cURL, hata kodları ve SDK örneklerini içerir."
weight: 20
---

Bu REST API, bir Excel çalışma sayfasındaki **liste nesnesini** (tabloyu) günceller.

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) ihtiyaç duyar.

## İstek Gövdesi Şeması

`listObject` DTO’su aşağıdaki alanları içerir. İstek gövdesinde yalnızca değiştirmek istediğiniz alanların belirtilmesi gerekir.

| Alan                                           | Tür                | Gerekli | Açıklama                                                                 |
| ----------------------------------------------- | ------------------ | ------- | ------------------------------------------------------------------------ |
| **DisplayName**                                 | string             | isteğe bağlı | Tablonun görünen adı.                                                    |
| **StartRow** / **StartColumn**                  | integer            | isteğe bağlı | Tablonun ilk satırı/sütunu için sıfır tabanlı indeks.                   |
| **EndRow** / **EndColumn**                      | integer            | isteğe bağlı | Tablonun son satırı/sütunu için sıfır tabanlı indeks.                   |
| **Range**                                       | string             | isteğe bağlı | Tablo aralığını tanımlayan A‑1 tarzı adres (örneğin, `A1:D10`).         |
| **ShowHeaderRow**                               | boolean            | isteğe bağlı | Başlık satırını göstermek için `true`.                                   |
| **ShowTotals**                                  | boolean            | isteğe bağlı | Toplam satırını göstermek için `true`.                                   |
| **TableStyleName**                              | string             | isteğe bağlı | Uygulanacak yerleşik tablo stili adı.                                   |
| **TableStyleType**                              | string             | isteğe bağlı | Stil türü (`TableStyleLight`, `TableStyleMedium`, vb.).                 |
| **ListColumns**                                 | object dizisi      | isteğe bağlı | Sütun tanımlarının koleksiyonu (`Name`, `TotalsCalculation`).           |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | object             | isteğe bağlı | Gelişmiş stil ve filtreleme seçenekleri (OpenAPI spesifikasyonunda tam DTO’ya bakın). |

### Minimal Örnek Yük

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **İstek Parametreleri**

| Parametre Adı       | Tür     | Konum | Açıklama                                    |
| ------------------- | ------- | ----- | ------------------------------------------- |
| **name**            | string  | path  | Belge adı.                                  |
| **sheetName**       | string  | path  | Çalışma sayfası adı.                        |
| **listObjectIndex** | integer | path  | Güncellenecek liste nesnesinin indeksi.     |
| **listObject**      | object  | body  | İstek gövdesindeki ListObject DTO’su.      |
| **folder**          | string  | query | Belgeyi içeren klasör.                      |
| **storageName**     | string  | query | Depo adı.                                   |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

### İstek

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Yanıt

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Başarılı yanıt aşağıdaki alanları içerir:

| Alan           | Tür    | Açıklama                                         |
| -------------- | ------ | ------------------------------------------------ |
| Code           | integer| HTTP durum kodu (başarı için 200).               |
| Status         | string | Durumun metinsel açıklaması.                     |
| UpdatedObject *(isteğe bağlı)* | object | Değiştirilen özellikler içeren güncellenmiş `ListObject` temsili. |

{{< /tab >}}

{{< /tabs >}}

## Hata Yanıtları

| HTTP Kodu | Açıklama                                                                | Örnek Yük                                                |
| --------- | ----------------------------------------------------------------------- | -------------------------------------------------------- |
| **400**   | Geçersiz istek – gerekli alanlar eksik veya bozuk JSON.                | `{ "Code": 400, "Message": "Geçersiz istek gövdesi." }` |
| **401**   | Yetkisiz – JWT belirteci eksik veya geçersiz.                          | `{ "Code": 401, "Message": "Kimlik doğrulama başarısız." }` |
| **404**   | Bulunamadı – belirtilen çalışma kitapçası, çalışma sayfası veya liste nesnesi mevcut değil. | `{ "Code": 404, "Message": "Kaynak bulunamadı." }` |
| **500**   | Sunucu iç hatası – sunucu tarafında beklenmedik bir durum oluştu.      | `{ "Code": 500, "Message": "Sunucu hatası." }`          |

## SSS

<details>  
<summary>Aspose.Cells Cloud API’yi kullanarak bir liste nesnesini nasıl güncellerim?</summary>

`POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}` uç noktasını kullanın. Değiştirmek istediğiniz özellikleri içeren bir JSON gövdesi ekleyin (örneğin, `DisplayName`, `ShowHeaderRow`). `Authorization` başlığında JWT belirtecini kullanarak kimlik doğrulaması yapın.

</details>

<details>  
<summary>Başarılı bir güncelleme sonrası ne tür bir yanıt alırım?</summary>

`Code: 200` ve `Status: "OK"` içeren bir JSON nesnesi döndürülür. Hata oluşursa, yanıt uygun HTTP durum kodunu ve sorunu açıklayan bir `Error` nesnesini içerir.

</details>

<details>  
<summary>Listenin nesne özelliklerinin yalnızca bir alt kümesini güncelleyebilir miyim?</summary>

Evet. İstek gövdesine yalnızca değiştirmek istediğiniz alanları ekleyin; atlanan tüm alanlar değişmeden kalır.

</details>

## İlgili Dokümantasyon

- [Bir Liste Objesi Ekle](https://docs.aspose.cloud/cells/list-objects/add/)
- [Liste Objesini Al](https://docs.aspose.cloud/cells/list-objects/get/)
- [Liste Objesini Sil](https://docs.aspose.cloud/cells/list-objects/delete/)

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en fazla artıracak yoldur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkânı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---