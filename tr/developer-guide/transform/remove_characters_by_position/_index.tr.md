---
---
title: "Konumuna Göre Karakterleri Kaldır"
ArticleTitle: "Konumuna Göre Karakterleri Kaldır – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Konumuna Göre Karakterleri Kaldır"
type: docs
url: /cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, Karakterleri Kaldır, API"
description: "Karakterleri bir hesaplama tablosundaki hücrelerden konumlarına göre siler."
weight: 100
---

## Aspose.Cells Cloud Web Hizmetlerinin Konumuna Göre Karakterleri Kaldırma Özelliği

Hedef aralıktaki her hücreden konuma göre (ilk/son N karakter, bir alt dize öncesinde/sonrasında veya iki sınırlayıcı arasında) karakterleri siler; formülleri,Biçimlendirmeyi ve veri doğrulamayı korur.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Güvenlik ve Yetkilendirme**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı yetkilendirme</a> gerektirir.

### İstek Parametreleri

| Parametre Adı             | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                      |
|---------------------------|---------|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | Dosya   | FormData                      | Hesaplama tablosu dosyasını yükler.                                                                           |
| theFirstNCharacters       | Tamsayı | Sorgu                         | Seçili hücrelerden ilk n karakteri kaldırmayı belirtir. İsteğe bağlı.                                          |
| theLastNCharacters        | Tamsayı | Sorgu                         | Seçili hücrelerden son n karakteri kaldırmayı belirtir. İsteğe bağlı.                                         |
| allCharactersBeforeText   | Dize    | Sorgu                         | Belirtilen alt dizeden önceki metni siler. İsteğe bağlı.                                                      |
| allCharactersAfterText    | Dize    | Sorgu                         | Belirtilen alt dizeden sonraki metni siler. İsteğe bağlı.                                                     |
| caseSensitive             | Boole   | Sorgu                         | `Substring` modu ve etkinleştirildiğinde `CustomChars` için geçerlidir. İsteğe bağlı.                         |
| worksheet                 | Dize    | Sorgu                         | Hesaplama tablosunun çalışma sayfasını belirtir. İsteğe bağlı.                                                |
| range                     | Dize    | Sorgu                         | Hesaplama tablosunun çalışma sayfası aralığını belirtir (örneğin, `A1:B10`). İsteğe bağlı.                    |
| outPath                   | Dize    | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan null’dir. İsteğe bağlı.                  |
| outStorageName            | Dize    | Sorgu                         | Çıkış dosyası için depo adı. İsteğe bağlı.                                                                    |
| region                    | Dize    | Sorgu                         | Hesaplama tablosu bölgesi/dil ayarı (örneğin, `en-US`, `fr-FR`). İsteğe bağlı.                                |
| password                  | Dize    | Sorgu                         | Hesaplama tablosu dosyasını açmak için gerekli şifre. İsteğe bağlı.                                           |

### Gövde Parametresi

| Parametre Adı | Tür  | Açıklama                     |
| -------------- | ---- | ---------------------------- |
| Spreadsheet    | Dosya | Hesaplama tablosu dosyasını yükler. |

### **Yanıt**

```json
{
  "status": "OK",
  "message": "Karakterler başarıyla kaldırıldı.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**Yanıt Durum Kodları**

| Kod | Anlamı | Açıklama |
|-----|--------|----------|
| 200 | OK | İşlem başarıyla tamamlandı ve işlenmiş dosya döndürüldü. |
| 400 | Bad Request | İstek bozuk veya geçersiz parametreler içeriyor. |
| 401 | Unauthorized | Yetkilendirme başarısız oldu veya JWT belirteci eksik/geçersiz. |
| 413 | Payload Too Large | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | Internal Server Error | Sunucu tarafında beklenmeyen bir hata oluştu. |

## SDK’lar ile Konumuna Göre Karakterleri Kaldırma Nasıl Kullanılır?

### Konumuna Göre Karakterleri Kaldırma Belirtimi

[Konumuna Göre Karakterleri Kaldır API Belirtimi](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

cURL komut satırı aracını kullanarak Aspose.Cells Cloud web hizmetlerine kolayca ulaşabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek gönderileceğini göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
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
  "status": "OK",
  "message": "Karakterler başarıyla kaldırıldı.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme hızını en hızlı şekilde artıran yoldur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, Aspose Cells Cloud web hizmetlerine çeşitli SDK’lar kullanılarak nasıl istek gönderileceğini göstermektedir:
`[TBD]`
---