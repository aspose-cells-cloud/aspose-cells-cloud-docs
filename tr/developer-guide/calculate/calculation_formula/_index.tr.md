---
title: "Formül Hesapla"
ArticleTitle: "Formül Hesapla – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Formül Hesapla"
type: docs
url: /tr/cells/calculate/formula
aliases: []
keywords: "Aspose Cells, formül hesapla, elektronik tablo, API"
description: "Aspose.Cells Cloud API kullanarak bir elektronik tabloda formülü hesaplayın."
weight: 100
---

## Aspose.Cells Cloud Web Hizmetlerinin Formül Hesaplama Özelliği

Yüklenen bir elektronik tablo dosyasının belirtilen bir çalışma sayfasında belirli bir formülü hesaplayıp sonuçtabloyu bir dosya akışı olarak döndürür. Bu işlem, **region** parametresi aracılığıyla yerel ayara özel işlemeyi destekler ve şifreli dosyaları açabilir.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvendir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama |
|---------------|--------|-------------------------------|----------|
| Spreadsheet   | Dosya  | FormData                      | Yüklenen elektronik tablo dosyası. |
| worksheet     | Dize   | Sorgu                         | Formülü içeren çalışma sayfasının adı. |
| formula       | Dize   | Sorgu                         | Hesaplanacak formül (örn. `=SUM(A1:B2)`). |
| region        | Dize   | Sorgu                         | Elektronik tablonun bölge/dil ayarı (örn. `tr-TR`, `fr-FR`). Sayı biçimlendirme, tarih çözümlemesi ve yerel ayara özgü davranışları etkiler. |
| password      | Dize   | Sorgu                         | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| ------------- | --- | -------- |
| [TBD] | [TBD] | [TBD] |

### **Yanıt**

```json
{
  "File": "<sonuçtablonun ikili akışı>"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | OK | Hesaplama başarılı; sonuçtablo dosyası döndürüldü. |
| 400 | Bad Request | Bir veya daha fazla istek parametresi eksik veya geçersiz. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya JWT belirteci eksik/geçersiz. |
| 413 | Payload Too Large | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | Internal Server Error | Sunucuda beklenmeyen bir hata oluştu. |

## SDK’lar ile Formül Hesaplama Nasıl Kullanılır

### Formül Hesaplama Özellikleri

[Formül Hesaplama API Özellikleri](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose Cells Cloud web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapıldığını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=tr-TR&password=MyPassword" \
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
  "File": "<sonuçtablonun ikili akışı>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. SDK, düşük seviye ayrıntıları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose Cells Cloud web hizmetlerine nasıl istek gönderileceğini göstermektedir:
 `[TBD]`
---