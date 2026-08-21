---
title: "Tüm Değişiklikleri Kabul Et"
ArticleTitle: "Tüm Değişiklikleri Kabul Et – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "Tüm Değişiklikleri Kabul Et"
type: docs
url: /cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, elektronik tablo, değişiklikler"
description: "Aspose.Cells Cloud API kullanarak bir elektronik tablo dosyasındaki tüm değişiklikleri kabul et."
weight: 100
---

## Aspose.Cells Cloud Web Servislerinin AcceptAllRevisions Özelliği

Yüklenen elektronik tablo dosyasındaki tüm değişiklikleri kabul eder ve işlenmiş çalışma kitabını döndürür.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı   | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|-----------------|--------|-------------------------------|----------|
| Spreadsheet     | Dosya  | FormData (HTTP Gövdesi)       | Elektronik tablo dosyasını yükle. |
| outPath         | string | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null’dır. |
| outStorageName  | string | Sorgu                         | Çıktı dosyası için depo adı. |
| fontsLocation   | string | Sorgu                         | Özel yazı tiplerini kullan. |
| region          | string | Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örn., `tr-TR`, `en-US`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmasını ve yerel ayara özgü davranışı etkiler. |
| password        | string | Sorgu                         | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür  | Açıklama                 |
|---------------|------|--------------------------|
| Spreadsheet   | Dosya | Elektronik tablo dosyasını yükle. |

### **Yanıt**

```json
{
  "File": "İşlenmiş elektronik tablonun ikili akışı"
}
```

**Yanıt Durum Kodları**

| Kod | Anlamı | Açıklama |
|-----|--------|----------|
| 200 | Tamam | Değişiklikler başarıyla kabul edildi ve işlenmiş dosya döndürüldü. |
| 400 | Geçersiz İstek | İstek geçersizdir (örn., gerekli dosya eksik veya parametreler hatalı). |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya JWT belirteci eksik/geçersiz. |
| 413 | Yük Çok Büyük | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | Sunucu İç Hatası | Sunucuda beklenmeyen bir hata oluştu. |

## SDK’larla AcceptAllRevisions Nasıl Kullanılır

### AcceptAllRevisions Spesifikasyonu

[AcceptAllRevisions API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca ulaşabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek yapmayı göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=tr-TR&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "İşlenmiş elektronik tablonun ikili akışı"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye ayrıntıları soyutlayarak projenizdeki görevlere odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="[TBD]" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose Cells Cloud web servislerini nasıl çağıracağınızı göstermektedir:
 `[TBD]`
---