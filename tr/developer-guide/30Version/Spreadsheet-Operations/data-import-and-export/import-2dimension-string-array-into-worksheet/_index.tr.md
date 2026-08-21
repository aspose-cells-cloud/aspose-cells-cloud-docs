---
title: "İkili Boyutlu Diziyi Excel Çalışma Sayfasına İçe Aktar"
second_title: "Belge"
linktype: "İçerik"
url: /tr/import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-string-array-into-excel-worksheet/",
    "/import-2dimension-string-array-into-worksheet/",
    "/import-data/-2dimension-string-array/",
    "/import-data/2dimension-string-array/",
    "/import/2dimension-string-array/",
  ]
keywords: "Aspose.Cells Cloud, ikili boyutlu dizi içe aktar, Excel, REST API, SDK"
description: "Aspose.Cells Cloud REST API ile bir Excel çalışma sayfasına iki boyutlu dize dizisi nasıl içe aktarılacağını öğrenin. İsteğin formatı, parametre ayrıntıları ve C#, PHP ve Ruby için SDK kod örnekleri içerir."
weight: 20
---

Bu REST API, **iki boyutlu bir dize dizisini** bir Excel çalışma sayfasına aktarır.

İstek, çoklu içerikli HTTP isteğidir (bkz. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çoklu içeriğin ilk kısmı `Import2DimensionStringArrayOption` verilerini, ikinci kısmı ise veri dosyasını içerir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

### **Import2DimensionStringArrayOption**

| Parametre Adı        | Tür                 | Açıklama                                                                      |
| -------------------- | ------------------- | ----------------------------------------------------------------------------- |
| FirstRow             | int                 | İçe aktarmanın başlayacağı satırın sıfır tabanlı indeksi.                     |
| FirstColumn          | int                 | İçe aktarmanın başlayacağı sütunun sıfır tabanlı indeksi.                     |
| Data                 | String[,]           | İçe aktarılacak dize değerlerini içeren iki boyutlu dizi.                     |
| DestinationWorksheet | string              | İçe aktarılan verileri alacak çalışma sayfasının adı.                         |
| IsInsert             | string (true/false) | **true** ise veri eklenir ve mevcut hücreler buna göre kaydırılır.            |
| ImportDataType       | string              | Veri türünü belirtir; bu işlem için `TwoDimensionStringArray` kullanın.       |
| Source               | FileSource          | `BatchData` parametresi null olduğunda veri dosyasının konumunu belirtir.     |

### Örnek İstek Gövdesi

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
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

| Kod | Anlam                       | Açıklama                                          |
|-----|-----------------------------|---------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek                | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz İstek              | Geçersiz veya eksik JWT belirteci.               |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut sınırını aşar.             |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                        |

## SDK’lar ile PostImportData API’sini Nasıl Kullanılır

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData), bir web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmenizi sağlayan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, bu işlevselliği entegre etmenin en hızlı yoludur. SDK, düşük seviye ayrıntıları soyutlayarak size iş mantığınızla ilgilenmenizi sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}