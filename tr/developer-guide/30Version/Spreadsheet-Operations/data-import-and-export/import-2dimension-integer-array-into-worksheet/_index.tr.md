---
title: "2 Boyutlu Tamsayı Dizisini Excel Çalışma Sayfasına İçe Aktar"
second_title: "Belge"
linktitle: "2 boyutlu tamsayı dizisini içe aktar"
type: docs
url: /tr/import-a-2d-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, 2D tamsayı dizisi içe aktar, Excel çalışma sayfası, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API, iki boyutlu tamsayı dizilerini Excel çalışma sayfalarına içe aktarmayı sağlar. SDK’lar Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift için mevcuttur."
weight: 20
---

Bu REST API, **iki boyutlu bir tamsayı dizisini** Excel çalışma sayfasına içe aktarır.

İstek, çok parçalı içerik içeren bir HTTP isteğidir (bkz. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk bölümü `Import2DimensionIntegerArrayOption` verilerini, ikinci bölümü ise veri dosyasını içerir.

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **Import2DimensionIntegerArrayOption**

| Parametre Adı        | Tür        | Açıklama                                                                                                                                                                                     |
| --------------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Verilerin yerleştirileceği ilk satırın 1‑tabanlı indeksi.                                                                                                                                      |
| FirstColumn          | int        | Verilerin yerleştirileceği ilk sütunun 1‑tabanlı indeksi.                                                                                                                                       |
| Data                 | Integer[,] | İçe aktarılacak değerleri içeren iki boyutlu tamsayı dizisi.                                                                                                                                    |
| DestinationWorksheet | string     | Hedef çalışma sayfasının adı.                                                                                                                                                                   |
| IsInsert             | string     | Verileri eklemek için `"true"`, mevcut hücreleri üzerine yazmak için `"false"`.                                                                                                                |
| ImportDataType       | string     | Veri formatını belirtir. Desteklenen değerler: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| Source               | FileSource | `BatchData` parametresi `null` olduğunda veri dosyasının konumunu belirtir.                                                                                                                    |

### **Örnek**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
}
```

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK                          | Süフィltre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırlarını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |

## SDK’lar ile PostImportData API Nasıl Kullanılır?

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData), web tarayıcısından doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}