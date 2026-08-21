---
title: "Tabloyu PDF'ye Dönüştür"
ArticleTitle: "Tabloyu PDF'ye Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "docs"
url: /tr/cells/convert/table/pdf
aliases: []
keywords: "Tabloyu PDF'ye Dönüştür, Aspose.Cells, API"
description: "Aspose.Cells Cloud kullanarak yerel bir sürücüdeki bir elektronik tablo tablosunu PDF dosyasına dönüştürür."
weight: 1000
---

## Aspose.Cells Cloud Web Hizmetlerinin Tabloyu PDF'ye Dönüştürme Özelliği

Bu işlem, yerel dosya sisteminden bir elektronik tablo dosyası okur, belirtilen tabloyu bir PDF belgesine dönüştürür ve dönüştürülmüş sonucu döndürür. İşlem tamamen bulut sunucusunda gerçekleşir; dolayısıyla ara yüzlü bir şekilde bulut depolama alanına yüklenmesine gerek yoktur. API, çıktı konumu, özel yazı tipleri, satırlar/sütunların otomatik boyutlandırma, bölgesel ayarlar ve şifreli çalışma kitapları için isteğe bağlı parametreleri destekler.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belge tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı   | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                     |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Dosya  | FormData                    | Elektronik tablo dosyasını yükleyin.                                                                                                                                         |
| worksheet        | Dize   | Sorgu                       | Elektronik tablonun çalışma sayfası adı.                                                                                                                                  |
| tableName        | Dize   | Sorgu                       | Tablo adı.                                                                                                                                                      |
| outPath          | Dize   | Sorgu                       | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null'dır.                                                                                  |
| outStorageName   | Dize   | Sorgu                       | Çıkış dosyası için Depolama Adı.                                                                                                                                       |
| fontsLocation    | Dize   | Sorgu                       | Özel yazı tiplerini kullanın.                                                                                                                                               |
| AutoRowsFit      | Boole  | Sorgu                       | (İsteğe bağlı) Çalışma sayfalarındaki tüm satırları otomatik olarak boyutlandırır.                                                                                                                    |
| AutoColumnsFit   | Boole  | Sorgu                       | (İsteğe bağlı) Çalışma sayfalarındaki tüm sütunları otomatik olarak boyutlandırır.                                                                                                                 |
| region           | Dize   | Sorgu                       | Elektronik tablo bölgesi/dil ayarı (örneğin, `tr-TR`, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih çözümleme ve yerel ayara özel davranışları etkiler.                         |
| password         | Dize   | Sorgu                       | Elektronik tablo dosyasını açmak için kullanılan şifre.                                                                                                                      |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
|----------------|------|-------------|
| *Yok* | *Yok* | *JSON gövdesi gerekmez; dosya multipart/form-data üzerinden gönderilir.* |

### **Yanıt**

```json
{
  "file": "<ikili PDF içeriği>"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|---------|-------------|
| 200 | Başarılı | Tablo başarıyla PDF'e dönüştürüldü; yanıt gövdesi PDF dosya akışını içerir. |
| 400 | Hatalı İstek | Geçersiz istek parametreleri veya hatalı biçimlendirilmiş URL. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgisi sağlanmadı. |
| 404 | Bulunamadı | Kaynak dosyaya erişilemiyor veya çalışma sayfası/tablo bulunamadı. |
| 413 | İçerik Çok Büyük | Yüklenen elektronik tablo izin verilen boyut sınırını aşıyor. |
| 500 | Sunucu İçinde Hata | Elektronik tablonun PDF'e dönüştürülmesi sırasında bir hata oluştu. |

## SDK’larla Tabloyu PDF'ye Dönüştürme Nasıl Kullanılır?

### Tabloyu PDF'ye Dönüştürme Belirtimi

[Tabloyu PDF'ye Dönüştür API Belirtimi](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells Cloud web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye istek yapma yöntemini göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt belgesi>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<ikili PDF içeriği>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK'larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose.Cells Cloud web hizmetlerinin nasıl çağrılacağını göstermektedir:
```csharp
// C# için SDK örneği kodu
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Java için SDK örneği kodu
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Python için SDK örneği kodu
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`
---