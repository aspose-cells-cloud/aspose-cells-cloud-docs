---
title: "Uzak Çalışma Kitabındaki Bozuk Bağlantıları ara"
ArticleTitle: "Uzak Çalışma Kitabındaki Bozuk Bağlantıları ara – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "docs"
url: /cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, Bozuk Bağlantıları ara, Uzak Çalışma Kitabı"
description: "Uzak bir bulut deposunda depolanan bir çalışma kitabının çalışma sayfasındaki bozuk bağlantıları ara."
weight: 100
---

## Aspose.Cells Cloud Web Servislerinin Uzak Çalışma Kitabındaki Bozuk Bağlantıları Arama İşlevi

Bu yöntem, uzak bir bulut deposunda depolanan bir hesaplama dosyasının çalışma sayfasında bozuk bağlantıları arar. Geçersiz hale gelen URL’ler veya eksik harici referanslar gibi, artık geçerli bir hedefe işaret etmeyen tüm sayfa ve hücreleri tarayarak bağlantıları inceler. İşlem, dosyanın yerel makineye indirilmesine gerek kalmadan bulut ortamında uzaktan gerçekleştirilir.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|----------------|------|-----------------------------|-------------|
| name | string | Yol | Arama yapılacak çalışma kitabının dosya adı. |
| worksheet | string | Yol | Arama için belirli bir çalışma sayfasını belirtin. |
| folder | string | Sorgu | Çalışma kitabının bulunduğu klasör yolu. (isteğe bağlı) |
| storageName | string | Sorgu | (İsteğe bağlı) Özel bulut deposu kullanılıyorsa deponun adı. Atlanırsa varsayılan depo kullanılır. |
| region | string | Sorgu | Hesaplama dosyasının bölge/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih ayrıştırma ve yerel ayara özel davranışları etkiler. |
| password | string | Sorgu | Hesaplama dosyasını açmak için gerekli şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| — | — | Bu işlem için istek gövdesine gerek yoktur. |

### **Yanıt**

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|---------|-------------|
| 200 | OK | Bozuk bağlantı listesi başarıyla alındı. |
| 400 | Bad Request | Geçersiz istek parametreleri veya bozuk URL. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya kimlik bilgisi sağlanmadı. |
| 404 | Not Found | Kaynak dosyaya erişilemedi. |
| 413 | Payload Too Large | İstek içeriği çok büyük. |
| 500 | Internal Server Error | Hesaplama dosyası veri alırken bir sorunla karşılaştı. |

## Uzak Çalışma Kitabındaki Bozuk Bağlantıları SDK’lar ile Nasıl Kullanılır

### Uzak Çalışma Kitabındaki Bozuk Bağlantıları Arama Özellikleri

[Uzak Çalışma Kitabındaki Bozuk Bağlantıları Arama API Belirtimi](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl atlanacağını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini en hızlı şekilde hızlandırmak için en iyi yoldur. SDK, düşük seviye detayları soyutlayarak projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web servislerine nasıl istek atlandığını göstermektedir:
`[TBD]`
---