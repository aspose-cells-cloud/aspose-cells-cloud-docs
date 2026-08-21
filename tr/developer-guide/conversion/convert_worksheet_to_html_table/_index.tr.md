---
title: "Çalışma Sayfasını HTML Tablosuna Dönüştür"
ArticleTitle: "Çalışma Sayfasını HTML Tablosuna Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "ConvertWorksheetToHtmlTable"
type: docs
url: /cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, HTML Tablosu, API"
description: "Aspose.Cells Cloud kullanarak yerel bir sürücüdeki bir elektronik tablo dosyasının belirli bir çalışma sayfasını HTML tablosu dosyasına dönüştürür."
weight: 100
---

## Aspose.Cells Cloud Web Servislerinin Çalışma Sayfasını HTML Tablosuna Dönüştürme Özelliği

Bu işlem, yerel dosya sistemindeki bir elektronik tablo dosyasını okur, belirtilen çalışma sayfasını HTML tablosuna dönüştürür ve dönüştürülen sonucu bir dosya akışı olarak döndürür. Dönüştürme işlemi tamamen bulut sunucusunda gerçekleştirilir, bu nedenle ara sunucuya yükleme gerektirmez. İsteğe bağlı yerel ayarlar ve şifreli çalışma kitaplarını destekler.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama |
|----------------|--------|-----------------------------|----------|
| Spreadsheet    | Dosya  | FormData                    | Elektronik tablo dosyasını yükleyin. |
| worksheet      | Dize   | Sorgu                       | Elektronik tablonun çalışma sayfası adı. (zorunludur) |
| region         | Dize   | Sorgu                       | Elektronik tablonun bölge/dil ayarı (örneğin `en-US`, `fr-FR`). Sayı formatlama, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler. |
| password       | Dize   | Sorgu                       | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| *Yok* | *Yok* | *JSON gövdesi gerekmez; dosya multipart/form-data olarak gönderilir.* |

### **Yanıt**

```json
{
  "File": "oluşturulan HTML tablosunun ikili akışı"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | Tamam | Çalışma sayfası başarıyla HTML tablosuna dönüştürüldü ve bir dosya akışı olarak döndürüldü. |
| 400 | Geçersiz İstek | Geçersiz istek URL'si veya eksik zorunlu parametreler. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgileri sağlanmadı. |
| 404 | Bulunamadı | Kaynak dosyaya erişilemedi. |
| 500 | İç Sunucu Hatası | Elektronik tablo dönüştürme verilerini alırken bir sorunla karşılaştı. |
| 413 | Yük Çok Büyük | Yüklenecek dosya izin verilen boyut sınırını aşıyor. |

## Çalışma Sayfasını SDK’larla HTML Tablosuna Dönüştürme Nasıl Yapılır

### Çalışma Sayfasını HTML Tablosuna Dönüştürme Spesifikasyonu

[Çalışma Sayfasını HTML Tablosuna Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'ye istek yapma yöntemini göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt belirteci>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "oluşturulan HTML tablosunun ikili akışı"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini en hızlı şekilde hızlandıran yoldur. SDK, düşük seviye detayları soyutlayarak proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells Cloud web servislerini çağırma yöntemlerini göstermektedir:
`[TBD]`
---