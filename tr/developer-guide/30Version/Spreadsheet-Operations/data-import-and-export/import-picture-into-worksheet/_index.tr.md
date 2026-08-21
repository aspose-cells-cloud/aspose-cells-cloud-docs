---
title: "Resimleri Excel Çalışma Sayfasına İçe Aktar"
ArticleTitle: "Resimleri Excel Çalışma Sayfasına İçe Aktar – Aspose.Cells Cloud API Kılavuzu"
second_title: "Belge"
linktitle: "Resim içe aktar"
type: docs
url: /tr/import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "resim içe aktar, Excel, Aspose.Cells Cloud, REST API, v3.0"
description: "Aspose.Cells Cloud REST API v3.0 ile resimleri Excel çalışma sayfalarına nasıl içe aktaracağınızı öğrenin. Multipart istek örnekleri, SDK kod örnekleri ve hata işleme yönergeleri içerir. Net adımlarla hızlıca başlayın."
weight: 19
---

Bir Excel çalışma sayfasına resim eklemek, defterlerinizi logolar, grafikler veya diyagramlar gibi görsel içeriklerle zenginleştirmenizi sağlar. Bu kılavuz, Aspose.Cells Cloud **ImportPicture** işlemini, gerekli istek formatını ve yanıtları nasıl işleyeceğinizi gösterir.

**Önkoşullar:** İçe aktarma işlemini çağırmadan önce geçerli bir JWT kimlik doğrulama belirteci ve Aspose Cloud Depolama’da depolanmış mevcut bir çalışma kitabına sahip olmanız gerekir.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

İstek, HTTP **POST** türündedir ve **multipart/related** içeriğe sahiptir (bkz. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- **İlk parça**, resmin nereye ve nasıl yerleştirileceğini tanımlayan **ImportPictureOption** adlı bir JSON nesnesini içerir.
- **İkinci parça**, resim dosyasını (veya Base64 ile kodlanmış verilerini) taşır.

### ImportPictureOption – tanım

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert`, bir **boolean** değerdir – `true` yeni bir resim ekler, `false` mevcut birini değiştirir._

### Önemli parametreler

**ImportPictureOption**

| Parametre Adı        | Tür         | Açıklama                                                                                                                                                                                     |
| --------------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UpperLeftRow          | int         | Resmin yerleştirileceği üst-sol köşesinin satır indeksi.                                                                                                                                      |
| UpperLeftColumn       | int         | Resmin yerleştirileceği üst-sol köşesinin sütun indeksi.                                                                                                                                       |
| LowerRightRow         | int         | Resmin sınırlarını belirleyen alt-sağ köşesinin satır indeksi.                                                                                                                                 |
| LowerRightColumn      | int         | Resmin sınırlarını belirleyen alt-sağ köşesinin sütun indeksi.                                                                                                                                  |
| Filename              | string      | Resim dosyasının adı.                                                                                                                                                                          |
| Data                  | string      | Resmin Base64 ile kodlanmış ikili verileri (dosya ikinci parça olarak gönderilmediyse isteğe bağlıdır).                                                                                       |
| DestinationWorksheet  | string      | Resmin ekleneceği çalışma sayfasının adı.                                                                                                                                                     |
| **IsInsert**          | **boolean** | `true` yeni bir resim eklemek için; `false` mevcut birini değiştirmek için.                                                                                                                     |
| ImportDataType        | string      | İçe aktarılan veri türü (örn. `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`).     |
| Source                | FileSource  | `BatchData` parametresi null olduğunda veri dosyasının konumunu belirtir.                                                                                                                     |

### Yanıt

Başarılı bir istek, şu şekilde bir JSON içeriğiyle **HTTP 200** döndürür:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Olası durum kodları:

| Kod | Anlam                                   |
|-----|-----------------------------------------|
| 200 | İçe aktarma başarılı                      |
| 400 | Geçersiz istek – eksik veya geçersiz veri |
| 401 | Yetkisiz erişim – geçersiz veya eksik belirteç |
| 500 | Sunucu iç hatası                        |

## SDK’lar ile PostImportData API Nasıl Kullanılır?

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostImport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları işler, böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}