---
title: "Tüm Metin Öğelerini Elektronik Tabloda ara"
ArticleTitle: "Tüm Metin Öğelerini Elektronik Tabloda ara – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Tüm Metin Öğelerini Elektronik Tabloda ara"
type: docs
url: /tr/cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, Arama, Metin Öğeleri, API"
description: "Aspose.Cells Cloud API kullanarak elektronik tablo dosyası içindeki tüm metin öğelerini arayın."
weight: 100
---

## Aspose.Cells Cloud Web Servislerinin Tüm Metin Öğelerini Elektronik Tabloda Arama Özelliği

Bu yöntem, yerel bir elektronik tablo dosyası içindeki tüm metin öğelerini arar. Çalışma kitabının tüm sayfalarını ve hücrelerini tarayarak arama teriminin oluşumlarını belirler. İşlem sunucu tarafında (bulut üzerinde) gerçekleştirilir ve herhangi bir bulut depolama alanı gerektirmez. Kaynak dosyayı okumak için gerekli izinlere sahip olduğunuzdan emin olun. Kaynak dosyaya erişilemezse ya da arama işlemi sırasında (desteklenmeyen dosya formatı gibi) bir hata oluşursa uygun bir istisna fırlatılır. Yöntem, uygulama detaylarına bağlı olarak eşleşmelerin konumlarını (örneğin, sayfa adı, hücre koordinatları) döndürebilir.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | Dosya | FormData | Elektronik tablo dosyasını yükleyin. |
| region | Dize | Sorgu | Elektronik tablonun bölge/dil ayarı (örneğin, `tr-TR`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmasını ve yerel ayara özgü davranışı etkiler. |
| password | Dize | Sorgu | Elektronik tablo dosyasını açmak için parola. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Yanıt**

```json
{
  "SearchResults": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Text": "Örnek metin"
    }
    // ... daha fazla öğe
  ],
  "TotalCount": 42
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|-------|----------|
| 200 | Başarılı | İstek başarılı oldu ve yanıt, bulunmuş tüm metin öğelerini içerir. |
| 400 | Geçersiz İstek | Geçersiz URL ya da bozuk istek parametreleri. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu ya da kimlik bilgileri sağlanmadı. |
| 404 | Bulunamadı | Kaynak dosyaya erişilemiyor. |
| 413 | Yük Çok Büyük | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası | Elektronik tablo, veri alma sırasında bir anomaliyle karşılaştı. |

## SDK’larla Tüm Metin Öğelerini Elektronik Tabloda Arama Nasıl Kullanılır

### Tüm Metin Öğelerini Elektronik Tabloda Arama Belirtimi

[Tüm Metin Öğelerini Elektronik Tabloda Arama API Belirtimi](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems}), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek gönderileceğini göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=tr-TR&password=myPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "SearchResults": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Text": "Örnek metin"
    }
    // ... daha fazla öğe
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini en hızlı şekilde hızlandıran yoldur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web servislerine nasıl istek gönderileceğini göstermektedir:
 `[TBD]`
---