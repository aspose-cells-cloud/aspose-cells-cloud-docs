---
title: "Excel Çalışma Sayfasına Çift Diziyi İçe Aktar"
second_title: "Belge"
linktitle: "Çift diziyi içe aktar"
type: docs
url: /tr/import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, çift diziyi içe aktar, Excel API, bulut SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasına çift dizi içe aktarmanın nasıl yapıldığını öğrenin. Kimlik doğrulama, istek formatı, parametreler, örnek XML/JSON ve yanıt ayrıntılarını içerir."
weight: 20
ArticleTitle: "Excel Çalışma Sayfasına Çift Diziyi İçe Aktar – Aspose.Cells Bulut Kılavuzu"
---

Bu REST API, **çift dizi verisini** bir Excel çalışma sayfasına içe aktarır.

> **Önkoşullar:** Bu API’yi çağırmadan önce geçerli bir JWT belirteciniz olmalıdır. Ayrıntılar için kimlik doğrulama kılavuzuna bakın.

HTTP isteğini **çoklu parçalı (multipart)** içeriğiyle gönderirsiniz (bkz. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Çoklu parçalı gövdenin ilk parçası **ImportDoubleArrayOption** verisini içerir, ikinci parçası ise veri dosyasını içerir.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

#### **ImportDoubleArrayOption**

| Parametre Adı        | Tür        | Açıklama                                                                                                   |
| --------------------- | ---------- | ---------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Verilerin yerleştirileceği ilk satırın sıfır tabanlı indeksi.                                              |
| FirstColumn          | int        | Verilerin yerleştirileceği ilk sütunun sıfır tabanlı indeksi.                                              |
| IsVertical           | boolean    | `true` / `false` – dizinin dikey (`true`) mi yoksa yatay (`false`) mi ekleneceğini belirler.               |
| Data                 | Double[]   | İçe aktarılacak çift (double) değer dizisi.                                                                |
| DestinationWorksheet | string     | Hedef çalışma sayfasının adı.                                                                               |
| IsInsert             | boolean    | `true` / `false` – `true` ise veriler eklenir; `false` ise mevcut hücreler üzerine yazılır.                |
| ImportDataType       | string     | İçe aktarılan veri türü (örn. `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`).           |
| Source               | FileSource | `BatchData` parametresi null olduğunda veri dosyasının konumunu belirtir.                                  |

#### Örnek (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### Örnek (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### Yanıt

Başarılı bir istek, JSON yükü içeren **HTTP 200** ile döner:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Olası durum kodları:

| Kod | Anlamı                                   |
|-----|------------------------------------------|
| 200 | İçe aktarma işlemi başarılı              |
| 400 | Geçersiz istek – eksik veya geçersiz veri|
| 401 | Yetkisiz – geçersiz veya eksik belirteç  |
| 500 | İç sunucu hatası                         |

### Hata İşleme

Bir hata oluştuğunda API, hata kodunu ve açıklayıcı bir mesajı içeren bir JSON nesnesi döner. Yetkisiz bir istek için örnek:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

İlgili içe aktarma işlemleri hakkında daha fazla bilgi için "İki Boyutlu Çift Diziyi İçe Aktar" ve "Tamsayı Dizisini İçe Aktar" belge sayfalarına bakın.

## PostImportData API’yi SDK’larla Nasıl Kullanılır

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostImport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. Bir SDK düşük seviye ayrıntıları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web servislerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}