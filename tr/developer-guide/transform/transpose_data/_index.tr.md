---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "docs"
url: /cells/transpose
aliases: ["/cells/transpose"]
keywords: "TransposeData, Aspose.Cells, Bulut API, elektronik tablo, transpoze"
description: "Elektronik tabloda satırları ve sütunları değiştirin."
weight: 1000
---

## Aspose.Cells Cloud Web Servislerinin TransposeData Özelliği

Elektronik tabloda satırları ve sütunları değiştirin.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür    | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                                                                              |
|------------------|--------|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Dosya  | FormData                     | Elektronik tablo dosyasını yükleyin.                                                                                                  |
| worksheet        | Dize   | Sorgu                        | Çalışma sayfası adı.                                                                                                                  |
| cellArea         | Dize   | Sorgu                        | Belirli bir veri aralığı.                                                                                                             |
| outPath          | Dize   | Sorgu                        | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null’dır.                                                  |
| outStorageName   | Dize   | Sorgu                        | Çıktı dosyasının depo adı.                                                                                                             |
| region           | Dize   | Sorgu                        | Elektronik tablo bölgesi/dil ayarı (örneğin, `tr-TR`, `en-US`, `fr-FR`). SayıBiçimlendirme, tarih ayrıştırma ve yerel ayara özel davranışları etkiler. |
| password         | Dize   | Sorgu                        | Elektronik tablo dosyasını açmak için şifre.                                                                                          |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| [TBD]          | [TBD]| [TBD]       |

### **Yanıt**

```json
{
  "file": "transpoze edilmiş elektronik tablonun ikili akışı"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|-------|----------|
| 200 | OK | Transpoze edilmiş elektronik tablo dosyası döndürülür. |
| 400 | Bad Request | Geçersiz girdi parametreleri veya bozuk istek. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya JWT belirteci eksik/geçersiz. |
| 413 | Payload Too Large | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | Internal Server Error | Beklenmeyen sunucu hatası. |

## SDK’lar ile TransposeData Nasıl Kullanılır?

### TransposeData Spesifikasyonu

[TransposeData API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose Cells Cloud web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye istek nasıl atlanacağını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=tr-TR&password=MyPassword" \
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
  "file": "transpoze edilmiş elektronik tablonun ikili akışı"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. SDK, düşük seviye detayları soyutlayarak projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, Aspose Cells Cloud web servislerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:
`[TBD]`
---