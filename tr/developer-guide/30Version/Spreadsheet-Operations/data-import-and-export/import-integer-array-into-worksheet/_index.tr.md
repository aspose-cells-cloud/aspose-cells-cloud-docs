---
title: "Tamsayı Dizisini Excel Çalışma Sayfasına İçe Aktar"
linktitle: "Tamsayı dizisini içe aktar"
type: docs
url: /tr/import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, tamsayı dizisini içe aktar, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "Aspose.Cells Cloud REST API kullanarak bir tamsayı dizisini Excel çalışma sayfasına nasıl içe aktaracağınızı öğrenin. İstek sözdizimi, parametreler, birden fazla SDK için örnek kod ve yanıt detaylarını içerir."
weight: 30
ArticleTitle: "Tamsayı Dizisini Excel Çalışma Sayfasına İçe Aktar – Aspose.Cells Cloud API"
---

Bu REST API, bir tamsayı dizisini Excel çalışma sayfasına içe aktarır.

İstek, çok parçalı içerik içeren bir HTTP **POST** olmalıdır (bkz. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı gövdenin ilk parçası, **ImportIntegerArrayOption** JSON yükünü içerir; ikinci parça ise kaynak veri dosyasını (örneğin bir CSV veya ikili Excel dosyası) içerir.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

Her iki uç nokta da aynı çok parçalı yükü kabul eder. Birinci uç nokta genel bir içe aktarma işlemi gerçekleştirirken, ikinci uç nokta `{name}` ile belirtilen belirli bir çalışma kitabını hedef alır.

### **Güvenlik ve Yetkilendirme**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

### ImportIntegerArrayOption

| Parametre Adı          | Tür        | Açıklama                                                                                                                                                               |
| ---------------------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**           | int        | Verilerin yerleştirileceği ilk satırın sıfır tabanlı indeksi.                                                                                                         |
| **FirstColumn**        | int        | Verilerin yerleştirileceği ilk sütunun sıfır tabanlı indeksi.                                                                                                         |
| **IsVertical**         | boolean    | Diziyi dikey (bir sütunda aşağı) eklemek için `true`; yatay (bir satırda boyunca) eklemek için `false`.                                                               |
| **Data**               | Integer[]  | İçe aktarılacak tamsayı dizisi.                                                                                                                                       |
| **DestinationWorksheet**| string     | Verilerin gönderileceği çalışma sayfasının adı.                                                                                                                       |
| **IsInsert**           | boolean    | Veri yazmadan önce satırlar/sütunlar eklemek için `true`; mevcut hücrelerin üzerine yazmak için `false`.                                                              |
| **ImportDataType**     | string     | İçe aktarılan verilerin türü. Geçerli değerler: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**             | FileSource | **BatchData** parametresi `null` olduğunda veri dosyasının konumunu belirtir.                                                                                        |

#### Örnek İstek Gövdesi

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### Yanıt

Başarılı bir istek, aşağıdaki gibi bir JSON yüküyle **HTTP 200** döndürür:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Olası durum kodları:

| Kod | Anlam                                   |
| --- | --------------------------------------- |
| 200 | İçe aktarma başarıyla tamamlandı        |
| 400 | Hatalı istek – eksik veya geçersiz veri |
| 401 | Yetkisiz erişim – geçersiz veya eksik belirteç |
| 500 | Sunucu iç hatası                        |

## PostImportData API’sini SDK’lar ile Nasıl Kullanılır

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostImport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, bu işlevselliği entegre etmenin en hızlı yoludur. SDK’lar düşük seviye ayrıntıları soyutlar ve iş mantığınıza odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}