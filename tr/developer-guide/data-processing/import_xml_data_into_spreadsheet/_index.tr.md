---
title: "XML Verisini Elektronik Tabloya İçe Aktar"
ArticleTitle: "XML Verisini Elektronik Tabloya İçe Aktar – Aspose.Cells Cloud API"
second_title: "Doküman"
linktype: "docs"
url: /tr/cells/import/data/xml
aliases: []
keywords: "XML İçe Aktar, Aspose.Cells, API"
description: "Aspose.Cells Cloud kullanarak XML veri dosyasını yerel elektronik tabloya içe aktarın."
weight: 1000
---

## Aspose.Cells Cloud Web Hizmetlerinin XML Verisini Elektronik Tabloya İçe Aktarma Özelliği

Yerel elektronik tabloya XML veri dosyası içe aktarın. Bu yöntem XML dosyasını ayrıştırır, verileri elektronik tablonun hücre yapısına eşler ve dosyayı yerel olarak kaydeder. Desteklenen elektronik tablo formatları: .xlsx ve .ods.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı   | Tür     | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                                                                            |
|------------------|---------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile         | Dosya   | FormData                      | Veri dosyasını yükleyin.                                                                                                                      |
| Spreadsheet      | Dosya   | FormData                      | Elektronik tablo dosyasını yükleyin.                                                                                                               |
| worksheet        | Metin   | Sorgu                         | XML verisinin içe aktarılacağı çalışma sayfası.                                                                                            |
| startcell        | Metin   | Sorgu                         | Veri içe aktarma için başlangıç konumu                                                                                                      |
| insert           | Boolean | Sorgu                         | Ekleme davranışını kontrol eder. true: verileri ekler; false: mevcut verilerin üzerine yazar. Varsayılan: **true**                               |
| outPath          | Metin   | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan: null.                                                         |
| outStorageName   | Metin   | Sorgu                         | Çıktı dosyası için depo adı.                                                                                                              |
| fontsLocation    | Metin   | Sorgu                         | Özel yazı tiplerini kullanın.                                                                                                                      |
| region           | Metin   | Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler. |
| password         | Metin   | Sorgu                         | Elektronik tablo dosyasını açmak için parola.                                                                                             |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
|----------------|-----|-------------|
| *Yok*          | -   | -           |

### **Yanıt**

```json
{
  "file": "<güncellenmiş elektronik tablonun ikili akışı>"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam                   | Açıklama                                                                                           |
|-----|-------------------------|-------------------------------------------------------------------------------------------------------|
| 200 | Tamam                   | XML verisi başarıyla içe aktarıldı ve güncellenmiş elektronik tablo dosyası döndürüldü.                        |
| 400 | Geçersiz İstek          | Geçersiz istek URL’si veya eksik gerekli parametreler.                                                   |
| 401 | Yetkisiz                | Kimlik doğrulama başarısız oldu veya kimlik bilgileri sağlanmadı.                                          |
| 404 | Bulunamadı              | Kaynak dosyaya erişilemiyor.                                                                           |
| 413 | Yük Çok Büyük           | Yüklenen dosya izin verilen boyut sınırını aşıyor.                                                          |
| 500 | Sunucu İç Hatası        | Elektronik tablo veri alırken bir anomaliyle karşılaştı.                                         |

## SDK’larla XML Verisini Elektronik Tabloya İçe Aktar Nasıl Kullanılır?

### XML Verisini Elektronik Tabloya İçe Aktarma Özelliği Spesifikasyonu

[XML Verisini Elektronik Tabloya İçe Aktar API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells Cloud web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapılacağını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{DataFileName}" \
  -F "Spreadsheet=@{SpreadsheetFileName}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<güncellenmiş elektronik tablonun ikili akışı>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, Aspose Cells Cloud web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:
`[TBD]`
---