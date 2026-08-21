---
title: "CSV Verisini Elektronik Tabloya İçe Aktar"
ArticleTitle: "CSV Verisini Elektronik Tabloya İçe Aktar – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "CSV Verisini Elektronik Tabloya İçe Aktar"
type: docs
url: /tr/cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, CSV içe aktarma, elektronik tablo, API"
description: "Aspose.Cells Cloud API kullanarak CSV veri dosyasını yerel elektronik tabloya içe aktarın."
weight: 100
---

## Aspose.Cells Cloud Web Servislerinin CSV Verisini Elektronik Tabloya İçe Aktarma Özelliği

CSV veri dosyasını yerel elektronik tabloya içe aktarın. Bu yöntem, CSV dosyasını ayrıştırır, verileri elektronik tablonun hücre yapısına eşler ve dosyayı yerel olarak kaydeder. Desteklenen elektronik tablo formatları şunları içerir: .xlsx ve .ods.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı         | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                          |
|-----------------------|---------|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| datafile              | Dosya   | FormData                      | Veri dosyasını yükleyin.                                                                                                          |
| Spreadsheet           | Dosya   | FormData                      | Elektronik tablo dosyasını yükleyin.                                                                                              |
| worksheet             | Dize    | Sorgu                         | CSV verisinin aktarılacağı çalışma sayfası. (zorunlu)                                                                             |
| startcell             | Dize    | Sorgu                         | Veri aktarımı için başlangıç konumu. (zorunlu)                                                                                   |
| insert                | Boolean | Sorgu                         | Ekleme davranışını kontrol eder. true: verileri ekler; false: mevcut verilerin üzerine yazar. Varsayılan: true (isteğe bağlı)    |
| convertNumericData    | Boolean | Sorgu                         | Metin dosyasındaki dizenin sayısal verilere dönüştürüp dönüştürülmeyeceği. Varsayılan: true (isteğe bağlı)                        |
| splitter              | Dize    | Sorgu                         | CSV alanlarını ayırmak için kullanılan ayraç. Varsayılan: "," (isteğe bağlı)                                                      |
| outPath               | Dize    | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan: null (isteğe bağlı)                                         |
| outStorageName        | Dize    | Sorgu                         | Çıktı dosyası için depo adı. (isteğe bağlı)                                                                                       |
| fontsLocation         | Dize    | Sorgu                         | Özel yazı tiplerini kullanın. (isteğe bağlı)                                                                                      |
| region                | Dize    | Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmasını ve yerel ayara özgü davranışı etkiler. (isteğe bağlı) |
| password              | Dize    | Sorgu                         | Elektronik tablo dosyasını açmak için şifre. (isteğe bağlı)                                                                       |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | --- | -------- |
| [TBD] | [TBD] | [TBD] |

### **Yanıt**

```json
{
  "file": "<oluşan elektronik tablonun ikili akışı>"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | Başarılı | CSV verisi başarıyla içe aktarıldı ve oluşan elektronik tablo dosyası döndürüldü. |
| 400 | Hatalı İstek | Geçersiz istek parametreleri veya bozuk URL. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgisi sağlanmadı. |
| 404 | Bulunamadı | Kaynak dosyaya erişilemedi. |
| 413 | Yük Çok Büyük | Yüklenen dosyalar izin verilen boyut sınırını aştı. |
| 500 | İç Sunucu Hatası | Elektronik tablo, veri alırken bir sorunla karşılaştı. |

## CSV Verisini Elektronik Tabloya İçe Aktarmayı SDK’lar ile Nasıl Kullanılır

### CSV Verisini Elektronik Tabloya İçe Aktarma Belirtimi

[CSV Verisini Elektronik Tabloya İçe Aktarma API Belirtimi](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sayfa1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=çıktıKlasörü&outStorageName=MyStorage&fontsLocation=/özel/yazıtipleri&region=tr-TR&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt belirteci>" \
  -F "datafile=@sample.csv" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<oluşan elektronik tablonun ikili akışı>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye ayrıntıları soyutlayarak size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, Aspose Cells Cloud web servislerini farklı SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:
 `[TBD]`
---