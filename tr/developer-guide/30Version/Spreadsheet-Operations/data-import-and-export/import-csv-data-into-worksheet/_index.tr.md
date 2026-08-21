---
title: "CSV Verisini Excel Çalışma Sayfasına İçe Aktar"
second_title: "Belge"
linktype: "İçe Aktar CSV verisi"
type: docs
url: /import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "CSV verisi içe aktar, Excel, Aspose.Cells Cloud, REST API, Elektronik tablo, CSV içe aktarma"
description: "Aspose.Cells Cloud REST API, CSV verilerini Excel çalışma sayfalarına içe aktarmayı sağlar. Desteklenen SDK’lar arasında Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift yer alır."
weight: 19
---

Bu REST API, **CSV verilerini** bir Excel çalışma sayfasına içe aktarır.

İstek, çok parçalı içerikli (bkz. [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) veya [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)) bir HTTP isteğidir. Çok parçalı içeriğin ilk parçası `ImportCSVDataOption` verisini, ikinci parçası ise CSV dosyasını içerir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

Önemli parametreler aşağıdaki tablolarda açıklanmıştır.

### ImportCSVDataOption

| Parametre Adı      | Tür                        | Açıklama                                                                  |
| ------------------ | -------------------------- | ------------------------------------------------------------------------ |
| SeparatorString    | string                     | CSV dosyasındaki alanları ayırmak için kullanılan karakter (örn., `,` veya `;`). |
| ConvertNumericData | string (`true`/`false`)    | Sayısal dizgelerin sayısal değerlere dönüştürüp dönüştürülmeyeceği.       |
| FirstRow           | int                        | Verilerin yerleştirileceği ilk satırın 1‑tabanlı indeksi.                |
| FirstColumn        | int                        | Verilerin yerleştirileceği ilk sütunun 1‑tabanlı indeksi.                |
| SourceFile         | string                     | İçe aktarılacak kaynak CSV dosyasının adı.                                |
| CustomParsers      | List\<CustomParserConfig\> | Belirli sütunlar için özel yorumlayıcı yapılandırmalarının koleksiyonu.   |

### CustomParserConfig

| Parametre Adı  | Tür    | Açıklama                                                                |
| -------------- | ------ | ----------------------------------------------------------------------- |
| ColumnIndex    | int    | Özel yorumlayıcının uygulanacağı sütunun 0‑tabanlı indeksi.             |
| ParseMethod    | string | Sütun için kullanılan yorumlama yöntemi (örn., `ToString`, `ToDate`, `ToNumber`). |
| CustomStyle    | string | Yorumlanmış hücrelere uygulanan özel stil (örn., sayı biçimi).          |

**Örnek**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413  | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırını aşıyor. |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

## SDK’larla PostImportData API Nasıl Kullanılır?

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData), web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme hızını en çok artıracak en iyi yoldur. SDK, düşük seviye ayrıntıları soyutlayarak size iş mantığınız üzerinde odaklanma imkânı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örneği, PHP SDK kullanılarak Aspose.Cells web hizmetinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}