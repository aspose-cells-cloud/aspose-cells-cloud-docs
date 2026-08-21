---
title: "Excel Çalışma Sayfasında Bir Şekli Güncelleme"
second_title: "Belge"
linktitle: "Güncelle"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "Excel API’de şekil güncelleme, Aspose.Cells Cloud, Excel şekil güncelleme, REST API, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında bir şekli nasıl güncelleyeceğinizi öğrenin. HTTPS uç noktası, kimlik doğrulama ayrıntıları, DTO şeması, adım adım kullanım, cURL örneği ve birden fazla dil için SDK kod örneklerini içerir."
ArticleTitle: "Excel Çalışma Sayfasında Bir Şekli Güncelleme - Aspose.Cells Cloud API"
weight: 31
---

Bu REST API, bir Excel çalışma sayfasındaki bir şekli günceller.

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### İstek Parametreleri

| Parametre Adı   | Tür      | Konum  | Açıklama                                                                                   |
| ---------------- | -------- | ------ | ------------------------------------------------------------------------------------------- |
| **name**         | string   | path   | Çalışma kitabının dosya adı.                                                                |
| **sheetName**    | string   | path   | Şekli içeren çalışma sayfasının adı.                                                        |
| **shapeindex**   | integer  | path   | Çalışma sayfasındaki şeklin sıfır tabanlı dizini.                                          |
| **dto**          | object   | body   | Güncellenmiş özellikleri içeren şekil veri aktarım nesnesi (aşağıda _DTO Şeması_’na bakın). |
| **folder**       | string   | query  | Çalışma kitabının bulunduğu klasör.                                                         |
| **storageName**  | string   | query  | Aspose Cloud depo adı.                                                                      |

### DTO Şeması

`dto` nesnesi güncellenebilecek özellikleri içerir. Aksi belirtilmedikçe tüm alanlar isteğe bağlıdır.

| Alan                | Tür      | Gerekli | Açıklama                                                                          |
| ------------------- | -------- | ------- | --------------------------------------------------------------------------------- |
| **Name**            | string   | Hayır   | Şeklin yeni adı.                                                                  |
| **UpperLeftRow**    | integer  | Hayır   | Şeklin sol üst köşesinin satır dizini.                                            |
| **UpperLeftColumn** | integer  | Hayır   | Şeklin sol üst köşesinin sütun dizini.                                             |
| **Width**           | integer  | Hayır   | Şeklin genişliği (nokta cinsinden).                                               |
| **Height**          | integer  | Hayır   | Şeklin yüksekliği (nokta cinsinden).                                              |
| **RotationAngle**   | integer  | Hayır   | Derece cinsinden dönüş açısı.                                                     |
| **IsHidden**        | boolean  | Hayır   | Şekli gizlemek için `true`.                                                        |
| **IsLocked**        | boolean  | Hayır   | Şekli kilitlemek için `true`.                                                      |
| **Font**            | object   | Hayır   | Yazı tipi ayarları (alt özellikler için OpenAPI spesifikasyonuna bakın).          |
| **...**             | …        | Hayır   | `HtmlText`, `AlternativeText`, `ZOrderPosition` vb. gibi ek özellikler.          |

> Tam liste için lütfen resmi OpenAPI spesifikasyonuna bakınız: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### İstek Başlıkları

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` (_Kimlik Doğrulama_ adımından elde edilen JWT belirteci)

### İstek Gövdesi (Örnek)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## cURL ile Örnek (Komut Satırı Aracı)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### Yanıt

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Hata Yönetimi** – API aşağıdaki durum kodlarını döndürebilir:

| Kod | Anlamı                | Tipik neden                                          |
| --- | --------------------- | ---------------------------------------------------- |
| 400 | Geçersiz İstek        | Geçersiz JSON veya gerekli alanların eksikliği.     |
| 401 | Yetkisiz İstek        | Eksik veya geçersiz JWT belirteci.                  |
| 404 | Bulunamadı            | Çalışma kitabı, çalışma sayfası veya şekil dizini yok. |
| 500 | Sunucu İç Hatası      | Beklenmeyen sunucu tarafı sorunu.                   |

**Hata Yanıt Örnekleri**

*400 – Geçersiz İstek*

```json
{
  "Code": 400,
  "Message": "Geçersiz istek yükü. 'Name' alanı maksimum uzunluğu aşıyor."
}
```

*401 – Yetkisiz İstek*

```json
{
  "Code": 401,
  "Message": "Kimlik doğrulama başarısız. Geçersiz veya süresi dolmuş JWT belirteci."
}
```

*404 – Bulunamadı*

```json
{
  "Code": 404,
  "Message": "Belirtilen çalışma kitabı, çalışma sayfası veya şekil dizini bulunamadı."
}
```

*500 – Sunucu İç Hatası*

```json
{
  "Code": 500,
  "Message": "Sunucuda beklenmeyen bir hata oluştu."
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızlandırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yöneterek projenizdeki görevlere odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}