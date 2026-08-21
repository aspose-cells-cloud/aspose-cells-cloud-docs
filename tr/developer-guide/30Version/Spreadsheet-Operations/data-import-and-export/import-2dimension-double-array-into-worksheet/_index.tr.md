---
title: "İkili Boyutlu Çift Diziyi Excel Çalışma Sayfasına İçe Aktar"
second_title: "Belge"
linktype: "İçerik"
type: docs
url: /tr/import-a-2d-double-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-double-array-into-excel-worksheet/,
    /import-2dimension-double-array-into-worksheet/,
    /import-data/2dimension-double-array/,
    /import/2dimension-double-array/,
  ]
keywords: "İkili Boyutlu Çift Dizi İçe Aktar, Excel, Aspose Cells Cloud, REST API, Elektronik Tablo, Veri İçe Aktarma"
description: "Aspose.Cells Cloud REST API kullanarak iki boyutlu bir çift diziyi Excel çalışma sayfasına nasıl içe aktaracağınızı öğrenin. İstek formatı, parametreler ve SDK kod örneklerini içerir."
weight: 20
---

Bu REST API, **iki boyutlu bir çift diziyi** Excel çalışma sayfasına **içe aktarır**.

İsteğin içeriği HTTP `POST` ve çok parçalı (multipart) içerikten oluşur (bkz. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı gövdenin ilk parçası **Import2DimensionDoubleArrayOption** verisini, ikinci parçası ise kaynak veri dosyasını içerir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

### Import2DimensionDoubleArrayOption

| Parametre Adı          | Tür         | Açıklama                                                                                                            |
| ---------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**           | `int`       | İçe aktarmanın başlayacağı satır indeksi (1‑tabanlı).                                                               |
| **FirstColumn**        | `int`       | İçe aktarmanın başlayacağı sütun indeksi (1‑tabanlı).                                                               |
| **Data**               | `Double[,]` | İçe aktarılacak çift değerlerden oluşan iki boyutlu dizi.                                                          |
| **DestinationWorksheet**| `string`   | Verinin aktarılacağı çalışma sayfasının adı.                                                                        |
| **IsInsert**           | `string`    | Satırların eklenmesi için `"true"`, mevcut hücrelerin üzerine yazılması için `"false"`.                             |
| **ImportDataType**     | `string`    | İçe aktarılan veri türü (örn. `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData`, vb.). |
| **Source**             | `FileSource`| `BatchData` parametresi null olduğunda veri dosyasının konumunu belirtir.                                          |

**Örnek**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
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

| Kod | Anlamı                      | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (Tamam)                  | Sü bộ filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.              |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırnı aşıyor.        |
| 500 | Internal Server Error (Sunucu İç Hatası) | Beklenmeyen sunucu hatası.                 |

## SDK’larla PostImportData API’sini Nasıl Kullanırız?

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData), web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanıza olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, bu işlevselliği entegre etmenin en hızlı yoludur. SDK’lar düşük seviye detayları ele alır, böylece iş mantığınıza odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}