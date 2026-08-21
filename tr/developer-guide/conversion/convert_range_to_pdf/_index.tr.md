---
title: "ConvertRangeToPdf"
ArticleTitle: "Aralığı PDF'ye Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "docs"
url: /tr/cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, Aralığı PDF'ye Dönüştür, API"
description: "Aspose.Cells Cloud kullanarak bir elektronik tablo belirli bir aralığını PDF'ye dönüştürür."
weight: 1
---

## Aspose.Cells Cloud Web Servislerinin ConvertRangeToPdf Özelliği

Yerel bir sürücüdeki bir elektronik tablonun belirli bir aralığını PDF dosyasına dönüştürür.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Güvenlik ve Yetkilendirme**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı   | Tür   | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                                                                                    |
|------------------|--------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Dosya  | FormData                    | Elektronik tablo dosyasını yükleyin.                                                                                                                       |
| worksheet        | Dize   | Sorgu                       | Elektronik tablonun çalışma sayfası adı.                                                                                                                |
| range            | Dize   | Sorgu                       | Hücre alanı. Örneğin: A1:C10                                                                                                                         |
| outPath          | Dize   | Sorgu                       | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null'dır.                                                                 |
| outStorageName   | Dize   | Sorgu                       | Çıktı dosyası için depo adı.                                                                                                                      |
| fontsLocation    | Dize   | Sorgu                       | Özel yazı tiplerini kullanın.                                                                                                                              |
| AutoRowsFit      | Boole  | Sorgu                       | (İsteğe bağlı) Çalışma sayfalarındaki tüm satırları otomatik olarak sığdırır.                                                                                                   |
| AutoColumnsFit   | Boole  | Sorgu                       | (İsteğe bağlı) Çalışma sayfalarındaki tüm sütunları otomatik olarak sığdırır.                                                                                                |
| region           | Dize   | Sorgu                       | Elektronik tablonun bölge/dil ayarı (örneğin, `tr-TR`, `fr-FR`). Sayı biçimlendirmesini, tarih ayrıştırmasını ve yerel ayara özel davranışı etkiler.       |
| password         | Dize   | Sorgu                       | Elektronik tablo dosyasını açmak için şifre.                                                                                                     |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
|----------------|------|-------------|
| Spreadsheet    | Dosya | Elektronik tablo dosyasını yükleyin. |

### **Yanıt**

```json
{
  "file": "<ikili PDF içeriği>"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|---------|-------------|
| 200 | Tamam | Başarılı dönüştürme; oluşturulmuş PDF dosya akışını döndürür. |
| 400 | Geçersiz İstek | Geçersiz URL. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgileri sağlanmadı. |
| 413 | Yük Çok Büyük | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası | Elektronik tablo, dönüştürme verilerini alırken bir sorunla karşılaştı. |

## ConvertRangeToPdf SDK’lar ile Nasıl Kullanılır

### ConvertRangeToPdf Spesifikasyonu

[ConvertRangeToPdf API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose Cells Cloud web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapılır gösterir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt belirteci>" \
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

### Aspose Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub Deposu</a>’na bakın.

Aşağıdaki kod örnekleri, Aspose Cells Cloud web servislerini çeşitli SDK’lar kullanarak nasıl çağıracağını göstermektedir:

```csharp
// C# için SDK örnek kodu
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// Java için SDK örnek kodu
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Python için SDK örnek kodu
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// JavaScript/Node.js için SDK örnek kodu
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---