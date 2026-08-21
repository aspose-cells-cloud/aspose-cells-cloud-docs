---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "SearchAllTextItemsInRemoteSpreadsheet"
type: docs
url: /tr/cells/{name}/search/content/all-textitems
aliases: []
keywords: "arama, metin öğeleri, Aspose.Cells"
description: "Aspose.Cells Cloud kullanarak uzak bir elektronik tabloda tüm metin öğelerini arayın."
weight: 100
---

## Aspose.Cells Cloud Web Servislerinin SearchAllTextItemsInRemoteSpreadsheet Yöntemi

Bu yöntem, uzak bir elektronik tablo dosyası içindeki tüm metin öğelerini arar. Çalışma kitabının tüm sayfalarını ve hücrelerini tarayarak arama teriminin oluşumlarını belirler. İşlem bulutta gerçekleştirilir ve yerel depolama gerektirmez. Kaynak dosyayı okumak için gerekli izinlere sahip olduğunuzdan emin olun. Kaynak dosyaya erişilemiyorsa veya arama işlemi sırasında (desteklenmeyen bir dosya formatı gibi) bir hata oluşursa uygun bir istisna fırlatılır. Yöntem, uygulama ayrıntılarına bağlı olarak eşleşmelerin konumlarını (örneğin, sayfa adı, hücre koordinatları) döndürebilir.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|---------------|--------|-------------------------------|----------|
| name          | string | Yol                           | Çalışma kitabının dosya adı. |
| folder        | string | Sorgu                         | Çalışma kitabının bulunduğu klasör yolu. |
| storageName   | string | Sorgu                         | (İsteğe bağlı) Özel bulut depolama kullanıyorsanız depolama adı. Atlanırsa varsayılan depolama kullanılır. |
| region        | string | Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örneğin, `tr-TR`, `en-US`, `fr-FR`). Sayı Biçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler. |
| password      | string | Sorgu                         | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | --- | -------- |
| [TBD]          |     | [TBD]    |

### **Yanıt**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | OK | İstek başarılı oldu ve yanıt, elektronik tabloda bulunan tüm metin öğelerini içerir. |
| 400 | Bad Request | Geçersiz URL veya istek parametreleri. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya kimlik bilgileri sağlanmadı. |
| 404 | Not Found | Kaynak dosyaya erişilemedi. |
| 413 | Payload Too Large | İstek yükü izin verilen boyutu aştı. |
| 500 | Internal Server Error | Elektronik tablo, veri alma sırasında bir anomaliyle karşılaştı. |

## SearchAllTextItemsInRemoteSpreadsheet SDK’ları ile Nasıl Kullanılır

### SearchAllTextItemsInRemoteSpreadsheet Spesifikasyonu

[SearchAllTextItemsInRemoteSpreadsheet API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek yapmayı göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bir bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Sheet1",
      "CellAddress": "A1",
      "Text": "Örnek metin"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose Cells Cloud web servislerini nasıl çağıracağınızı göstermektedir:
`[TBD]`
---