---
title: "Aralığı CSV'ye Dönüştür"
ArticleTitle: "Aralığı CSV'ye Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "docs"
url: /cells/convert/range/csv
aliases: []
keywords: "dönüştür, csv, aralık, Aspose.Cells"
description: "Yerel bir sürücüdeki bir elektronik tablo aralığını csv dosyasına dönüştürür."
weight: 1
---

## Aspose.Cells Cloud Web Hizmetlerinin Aralığı CSV'ye Dönüştürme Özelliği

Bu işlem, yerel dosya sisteminden bir elektronik tablo dosyasını okur, belirtilen bir aralığı CSV formatına dönüştürür ve dönüştürülen sonucu doğrudan döndürür. Tamamen bulut sunucusunda çalışır, bu nedenle bulut depolama alanına ara yükleme gerekmez. API, özel yazı tipleri, satırları/sütunları otomatik sığdırma, yerel ayarlar ve şifreli çalışma kitapları gibi isteğe bağlı parametreleri destekler.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                             |
|------------------|---------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Dosya   | FormData                      | Elektronik tablo dosyasını yükleyin.                                                                                                |
| worksheet        | String  | Sorgu                         | Elektronik tablonun çalışma sayfası adı. **Zorunludur**.                                                                             |
| range            | String  | Sorgu                         | Hücre alanı. Örneğin `A1:C10`. **Zorunludur**.                                                                                        |
| outPath          | String  | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null'dır.                                                 |
| outStorageName   | String  | Sorgu                         | Çıktı dosyası için depo adı.                                                                                                         |
| fontsLocation    | String  | Sorgu                         | Özel yazı tiplerini kullanın.                                                                                                        |
| AutoRowsFit      | Boolean | Sorgu                         | (İsteğe bağlı) Çalışma sayfalarındaki tüm satırları otomatik sığdırır.                                                               |
| AutoColumnsFit   | Boolean | Sorgu                         | (İsteğe bağlı) Çalışma sayfalarındaki tüm sütunları otomatik sığdırır.                                                               |
| region           | String  | Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmasını ve yerel ayara özgü davranışı etkiler. |
| password         | String  | Sorgu                         | Elektronik tablo dosyasını açmak için şifre.                                                                                        |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | --- | -------- |
| Yok            | N/A | İstek gövdesi parametresi yoktur. |

### **Yanıt**

```json
{
  "ResponseFile": "ikili dosya akışı (CSV içeriği)"
}
```

**Yanıt Durum Kodları**

| Kod | Anlamı | Açıklama |
|-----|--------|----------|
| 200 | Tamam | Aralık başarıyla dönüştürüldü ve CSV dosyası yanıt gövdesinde döndürüldü. |
| 400 | Geçersiz İstek | Geçersiz URL veya eksik zorunlu parametreler. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgisi sağlanmadı. |
| 413 | Yük Çok Büyük | İstek gövdesi boyutu izin verilen sınıra aşkı. |
| 500 | İç Sunucu Hatası | Elektronik tablo dönüştürme verilerini alırken bir sorunla karşılaştı. |

## Aralığı CSV'ye SDK'larla Nasıl Kullanılır

### Aralığı CSV'ye Dönüştürme Özelliği

[Convert Range to CSV API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca ulaşmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "Base64EncodedCsvContent"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK'larını Kullanma

SDK kullanmak, geliştirmeyi hızlandırmak için en hızlı yoldur. SDK, düşük seviye ayrıntıları soyutlayarak projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose Cells Cloud web hizmetlerine nasıl istek atılacağını göstermektedir:
`[TBD]`
---