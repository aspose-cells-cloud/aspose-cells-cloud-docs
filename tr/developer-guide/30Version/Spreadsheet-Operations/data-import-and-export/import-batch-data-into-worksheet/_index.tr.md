---
title: "Toplu Verileri Excel Çalışma Sayfasına İçe Aktar"
second_title: "Belge"
linktype: "toplu-verileri-ice-aktar"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, Bulut API, toplu veri içe aktarma, Excel, CSV, JSON, XML, diziler"
description: "Aspose.Cells Cloud REST API kullanarak Excel çalışma sayfasına toplu verileri (CSV, JSON, XML, diziler) nasıl içe aktaracağınızı öğrenin. Kimlik doğrulama, istek/yanıt örnekleri, SDK kod parçacıkları ve hata yönetimi içerir."
weight: 19
ArticleTitle: "Toplu Verileri Excel Çalışma Sayfasına İçe Aktar – Aspose.Cells Cloud Dokümantasyonu"
---

Bu REST API, Excel çalışma sayfasına **toplu veri içe aktarır**. İsteğin ilk parçası **ImportBatchDataOption** nesnesini, ikinci parçası ise gerçek veri dosyasını (CSV, JSON, XML vb.) içerir.

İşlem, çok parçalı içerikli bir HTTP isteği kullanır (bkz. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### ImportBatchDataOption

| Parametre Adı           | Tür               | Açıklama                                                                                                                                                                                   |
| ------------------------ | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**            | `List<CellValue>` | Doğrudan yazılacak hücre değerlerinden oluşan koleksiyon.                                                                                                                                             |
| **DestinationWorksheet** | `string`          | Verilerin içe aktarılacağı çalışma sayfasının adı.                                                                                                                                        |
| **IsInsert**             | `bool`            | `true` ise veriler eklenir ve mevcut hücreler kaydırılır; `false` ise veriler mevcut hücreleri üzerine yazar.                                                                           |
| **ImportDataType**       | `string`          | İçe aktarılacak verilerin biçimi. İzin verilen değerler: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | `FileSource`      | **BatchData** `null` olduğunda veri dosyasının konumunu belirtir.                                                                                                                         |

### CellValue

| Parametre Adı   | Tür      | Açıklama                                                 |
| --------------- | -------- | --------------------------------------------------------- |
| **rowIndex**    | `int`    | Hedef hücrenin sıfırdan başlayarak satır indeksi.                  |
| **columnIndex** | `int`    | Hedef hücrenin sıfırdan başlayarak sütun indeksi.               |
| **type**        | `string` | Değerin veri türü (örn. `int`, `double`, `string`). |
| **value**       | `string` | Hücreye yazılacak gerçek değer.                  |
| **style**       | `Style`  | Hücre için isteğe bağlı stil bilgileri.                |

### FileSource

| Parametre Adı      | Tür      | Açıklama                                                                |
| ------------------ | -------- | -------------------------------------------------------------------------- |
| **FileSourceType** | `string` | Dosyanın kaynağı: `InMemoryFiles`, `CloudFileSystem` veya `RequestFiles`. |
| **FilePath**       | `string` | Seçilen kaynak içindeki dosyanın yolu veya tanımlayıcısı.                   |

### Örnek (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam                       | Filtre başarıyla uygulandı; yanıt, işlem ayrıntılarını içerir. |
| 400  | Geçersiz İstek              | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401  | Yetkisiz                    | Geçersiz veya eksik JWT jetonu. |
| 413  | Yük Çok Büyük               | Yüklenecek dosya boyut sınırını aşıyor. |
| 500  | İç Sunucu Hatası            | Beklenmeyen sunucu hatası. |

## SDK’larla PostImportData API Nasıl Kullanılır

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData), bir web tarayıcısından doğrudan REST etkileşimlerinde bulunmanıza olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, bu işlevselliği entegre etmenin en hızlı yoludur. SDK’lar, iş mantığınıza odaklanabilmeniz için düşük seviye detayları yönetir. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’larla Aspose.Cells web hizmetlerinin nasıl çağrılacağını gösterir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}