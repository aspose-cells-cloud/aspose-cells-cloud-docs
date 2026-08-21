---
title: "Excel Çalışma Sayfasına Dize Dizisi İçe Aktar – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "Dize dizisi içe aktar"
type: docs
url: /tr/import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, dize dizisi içe aktar, Excel REST API, çok parçalı yükleme, çalışma sayfası verisi içe aktarma, bulut SDK'sı"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir dize dizisini Excel çalışma sayfasına nasıl içe aktaracağınızı öğrenin. İstek formatını, parametreleri ve SDK örneklerini içerir."
weight: 40
ArticleTitle: "Excel Çalışma Sayfasına Dize Dizisi İçe Aktar – Aspose.Cells Cloud"
---

Bir dize dizisini Excel çalışma sayfasına içe aktarmak, lisel verilerle spreadsheets doldururken yaygın bir görevdir. Bu işlem, yapılandırma değerlerini yükleme, harici kaynaklardan veri aktarma veya çalışma sayfalarını önceden tanımlanmış dize koleksiyonlarıyla başlatma gibi senaryolar için kullanışlıdır.

**Önkoşullar:**  
- Aspose.Cells Cloud kimlik doğrulama akışı aracılığıyla elde edilen geçerli bir JWT jetonu.  
- Aspose Cloud depolarınızda mevcut bir çalışma kitapçığı (veya yeni oluşturabilme yeteneği).  
- `ImportStringArrayOption` modelini destekleyen uygun SDK sürümü.

Bu REST API, dize dizisi verilerini bir Excel çalışma sayfasına içe aktarır.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

İstek, çok parçalı HTTP içeriği kullanır (bkz. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Çok parçalı gövdenin ilk parçası bir **ImportStringArrayOption** yükünü içerir; ikinci parça kaynak veri dosyasını içerir.

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

<caption>ImportStringArrayOption parametreleri</caption>
### **ImportStringArrayOption**

| Parametre Adı        | Tür        | Açıklama                                                                                                                                                                            |
| --------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Verilerin yerleştirileceği başlangıç satır indeksi (1‑tabanlı).                                                                                                                     |
| FirstColumn          | int        | Verilerin yerleştirileceği başlangıç sütun indeksi (1‑tabanlı).                                                                                                                     |
| IsVertical           | boolean    | Verileri dikey eklemek için `true`; yatay eklemek için `false`.                                                                                                                    |
| Data                 | String[]   | İçe aktarılacak dize dizisi.                                                                                                                                                        |
| DestinationWorksheet | string     | Verilerin gönderileceği çalışma sayfasının adı.                                                                                                                                    |
| IsInsert             | boolean    | Satırları/sütunları eklemek için (`true`, mevcut hücreleri kaydırarak); mevcut hücreleri üzerine yazmak için (`false`).                                                             |
| ImportDataType       | string     | İçe aktarılan veri türü (örn. `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`).     |
| Source               | FileSource | **BatchData** null olduğunda veri dosyasının bulunduğu yeri tanımlar (örn. `CloudFileSystem`, `LocalFile`). `BatchData` sağlanmadıysa gereklidir.                                   |

### Örnek

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### Yanıt

Başarılı bir istek, JSON yükü içeren **HTTP 200** döndürür:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Olası durum kodları:

| Kod | Anlam                                   |
| --- | --------------------------------------- |
| 200 | İçe aktarma başarılı                    |
| 400 | Geçersiz istek – eksik veya geçersiz veri |
| 401 | Yetkisiz – geçersiz veya eksik jeton    |
| 500 | Sunucu iç hatası                        |


## SDK ile PostImportData API Nasıl Kullanılır

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostImport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

### Aspose.Cells Cloud SDK Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub deposunu](https://github.com/aspose-cells-cloud) inceleyin.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}