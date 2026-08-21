---
title: "Tabloyu Böl"
ArticleTitle: "Tabloyu Böl – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Tabloyu Böl"
type: docs
url: /tr/cells/split/table
aliases: []
keywords: "Aspose.Cells, Tabloyu Böl, API"
description: "Elektronik tablo içindeki bir tabloyu sütun değerlerine göre bölmek için API."
weight: 1
---

## Aspose.Cells Cloud Web Hizmetlerinin SplitTable Yöntemi

Bu yöntem, belirtilen sütundaki benzersiz değerlere göre satırları gruplayarak kaynak tablo üzerinde bir bölme işlemi gerçekleştirir. Her veri grubu (her benzersiz bölme değeri için), ayrı bir veri birimi olarak işlenir. Dışa aktarma hedefi, iki temel boole parametresi ile kontrol edilir:
- Çalışma kitabının yapısını belirler. `true` olarak ayarlanırsa, her bölme birimi ayrı bir çalışma kitabını dosyasına kaydedilir. `false` olarak ayarlanırsa, her birim mevcut çalışma kitabında yeni bir çalışma sayfası olur.
- Çıktı paketlemeyi belirler. `true` olarak ayarlanırsa ve `toNewWorkbook` = `true` ile birlikte kullanılırsa, yöntem birden fazla ayrı dosya oluşturur ve bunları ZIP arşivi olarak döndürür. `false` olarak ayarlanırsa, tüm veriler tek bir dosyada birleştirilir (çok sayfalı bir çalışma kitabı veya diğer ayarlara göre tek bir dosya).

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı     | Tür       | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                               |
|-------------------|-----------|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet       | Dosya     | FormData                      | Elektronik tablo dosyasını yükleyin.                                                                                                                                   |
| worksheet         | Dize      | Sorgu                         | Tablonun bulunduğu çalışma sayfası.                                                                                                                                    |
| tableName         | Dize      | Sorgu                         | Bölünmesi gereken veri tablosu.                                                                                                                                        |
| splitColumnName   | Dize      | Sorgu                         | Bölüneceği sütun adı.                                                                                                                                                  |
| saveSplitColumn   | Boole     | Sorgu                         | Bölünen sütundaki verilerin tutulup tutulmayacağı.                                                                                                                     |
| splitRowNumber    | Tamsayı   | Sorgu                         | [TBD]                                                                                                                                                                   |
| toNewWorkbook     | Boole     | Sorgu                         | Dışa aktarma hedefi kontrolü: true – Bölünen verileri içeren yeni çalışma kitabını dosyalar oluşturur; false – Mevcut çalışma kitabına yeni bir çalışma sayfası ekler. |
| toMultipleFiles   | Boole     | Sorgu                         | true – Tablo verilerini **birden fazla ayrı dosya** olarak dışa aktarır (ZIP arşivi olarak döndürülür); false – Tüm verileri **tek bir dosyada** çok sayfalı olarak saklar. Varsayılan: false. |
| outPath           | Dize      | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan: null.                                                                                             |
| outStorageName    | Dize      | Sorgu                         | Çıktı dosyası için depo adı.                                                                                                                                            |
| fontsLocation     | Dize      | Sorgu                         | Özel yazı tiplerini kullanın.                                                                                                                                           |
| region            | Dize      | Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örn., `tr-TR`, `en-US`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmayı ve yerel ayara özel davranışı etkiler.                   |
| password          | Dize      | Sorgu                         | Elektronik tablo dosyasını açmak için şifre.                                                                                                                           |

### Gövde Parametresi

| Parametre Adı | Tür  | Açıklama                  |
| --------------| ---- | ------------------------- |
| Spreadsheet   | Dosya | Elektronik tablo dosyasını yükleyin. |

### **Yanıt**

```json
{
  "file": "ikili akış (parametrelere göre ZIP arşivi veya çalışma kitabını)"
}
```

**Yanıt Durum Kodları**

| Kod | Anlamı | Açıklama |
|-----|--------|----------|
| 200 | OK (Tamam) | Bölme işlemi başarıyla tamamlandı. Yanıt, oluşturulan dosyayı (ZIP arşivi veya çalışma kitabını) içerir. |
| 400 | Bad Request (Hatalı İstek) | Geçersiz URL veya istek parametreleri. |
| 401 | Unauthorized (Yetkisiz) | Kimlik doğrulama başarısız oldu veya kimlik bilgisi verilmedi. |
| 404 | Not Found (Bulunamadı) | Kaynak dosyaya erişilemedi. |
| 413 | Payload Too Large (İstek Gövdesi Çok Büyük) | İstek gövdesi izin verilen boyutu aştı. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Elektronik tablo veri alınırken bir anormallik ile karşılaştı. |

## SplitTable SDK’ları ile Nasıl Kullanılır?

### SplitTable Belirtimi

[SplitTable API Belirtimi](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenizi sağlar.

Aspose.Cells Cloud web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "file": "ikili akış (parametrelere göre ZIP arşivi veya çalışma kitabını)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirmeyi hızlandırmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web hizmetlerine nasıl istek atılacağını göstermektedir:
`[TBD]`