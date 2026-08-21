---
title: "Tabloyu CSV'ye Dönüştür"
ArticleTitle: "Tabloyu CSV'ye Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "doc"
url: /cells/convert/table/csv
aliases: []
keywords: "Tabloyu CSV'ye Dönüştür, Aspose.Cells, Bulut API"
description: "Yerel bir sürücüdeki elektronik tablo tablosunu CSV dosyasına dönüştürür."
weight: 1
---

## Aspose.Cells Cloud Web Hizmetlerinin Tabloyu CSV'ye Dönüştürme Özelliği

Bu yöntem, yerel dosya sisteminden bir elektronik tablo dosyası okur, belirtilen tabloyu bir CSV dosyasına dönüştürür ve dönüştürülen sonucu döndürür. Tamamen bulut sunucusunda çalışır, bu nedenle ara olarak bulut depolama alanına yükleme gerektirmez. Kaynak dosya yolu ve hedef format doğru şekilde belirtilmelidir; ayrıca kaynak dosyayı okumak için uygun izinlere sahip olunmalıdır. Eksik dosyalar, erişilemez yollar veya dönüştürme hataları gibi sorunlar uygun istisnalara neden olur.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|------------------|---------|-------------------------------|----------|
| Spreadsheet      | Dosya   | FormData                      | Elektronik tablo dosyasını yükleyin. |
| worksheet        | Dize    | Sorgu                         | Elektronik tablonun çalışma sayfası adı. |
| tableName        | Dize    | Sorgu                         | Tablo adı |
| outPath          | Dize    | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null'dır. |
| outStorageName   | Dize    | Sorgu                         | Çıktı dosyasının Depo Adı. |
| fontsLocation    | Dize    | Sorgu                         | Özel yazı tiplerini kullanın. |
| AutoRowsFit      | Boolean | Sorgu                         | (İsteğe bağlı) Çalışma sayfalarındaki tüm satırları otomatik olarak sığdırır. |
| AutoColumnsFit   | Boolean | Sorgu                         | (İsteğe bağlı) Çalışma sayfalarındaki tüm sütunları otomatik olarak sığdırır. |
| region           | Dize    | Sorgu                         | Elektronik tablonun bölge/dil ayarı (örneğin, `en-US`, `fr-FR`). Sayı Biçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler. |
| password         | Dize    | Sorgu                         | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| *Yok* | *Yok* | *İstek gövdesine gerek yoktur; dosya multipart/form-data olarak gönderilir.* |

### **Yanıt**

```json
{
  "file": "oluşturulan CSV dosyasının ikili akışı"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | Başarılı | Tablo başarıyla dönüştürüldü ve CSV dosyası döndürüldü. |
| 400 | Hatalı İstek | Geçersiz istek parametreleri veya hatalı biçimlendirilmiş URL. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgileri sağlanmadı. |
| 404 | Bulunamadı | Kaynak dosyaya erişilemiyor veya dosya mevcut değil. |
| 413 | Yük Çok Büyük | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası | Dönüştürme sırasında elektronik tabloda bir sorun oluştu. |

## SDK’ları Kullanarak Tabloyu CSV'ye Dönüştürme Nasıl Yapılır

### Tabloyu CSV'ye Dönüştürme Özelliği

[Tabloyu CSV'ye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek yapılacağını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "oluşturulan CSV dosyasının ikili akışı"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. SDK, düşük seviyeli detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells Cloud web hizmetlerinin nasıl çağrılacağını göstermektedir:
`[TBD]`
---