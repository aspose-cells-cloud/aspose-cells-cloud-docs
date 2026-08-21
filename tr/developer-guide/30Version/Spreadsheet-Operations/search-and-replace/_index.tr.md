---
title: "Excel Dosyaları İçinde Metin İçeriğini Arama ve Değiştirme"
second_title: "Dokümantasyon"
linktitle: "Arama ve Değiştirme"
type: docs
url: /tr/search-and-replace/
aliases: [  /tr/working-with-text/ , /tr/text/ ]
description: "Aspose.Cells Cloud REST API kullanarak Excel çalışma kitapları ve çalışma sayfalarında metin arama ve değiştirme işlemlerini öğrenin. İstek formatını, .NET, Java, Python için örnek kodları ve hata işleme yöntemlerini içerir."
keywords: "Aspose.Cells Cloud, Excel, arama ve değiştirme, REST API, .NET, Java, Python"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API Kullanılarak Excel Dosyalarında Metin Arama ve Değiştirme"
---

Metin işlemleri, Excel dosyaları için karmaşık işlemlerdir. Bu karmaşıklığa birçok faktör katkı sağlar ve işleme sırasında dikkate alınmalıdır. Aspose.Cells Cloud, çeşitli elektronik tablo formatlarında metin arama ve değiştirme konusunda güvenilir bir çözüm sunar.

Excel çalışma kitaplarında metinle çalışmak, genellikle belirli dizeleri bulup bunları birden fazla sayfada güncellemeyi gerektirir. Aspose.Cells Cloud API, bu görevi basitleştirerek desteklenen tüm elektronik tablo formatlarında çalışan tek bir **arama ve değiştirme** işlemi sağlar.

## Genel Bakış

Arama ve değiştirme işlemi, bir çalışma kitabında veya belirli bir çalışma sayfasında belirli dizeleri bulup bunları yeni değerlerle değiştirme imkanı sunar. İşlem, Aspose.Cells Cloud tarafından desteklenen **XLS, XLSX, XLSM, XLSB, ODS, CSV** ve diğer tüm formatlarla çalışır. **Arama ve değiştirme** özelliği sayesinde verileri hızlı bir şekilde temizleyebilir, tekrarlanan yazım hatalarını düzeltebilir veya tüm çalışma kitabında toplu adlandırma kurallarını uygulayabilirsiniz.

## Ön Gereksinimler

- Geçerli bir **Client‑Id** ve **Client‑Secret** içeren aktif bir Aspose.Cloud hesabı.
- OAuth 2.0 kimlik doğrulama akışı ile elde edilen erişim belirteci (access token).
- Hedef çalışma kitabının Aspose Cloud depolama alanına kaydedilmiş ya da herkese açık bir URL üzerinden erişilebilir olması.
- Gerekli SDK'nın yüklü olması (örneğin, .NET, Java veya Python için Aspose.Cells‑Cloud).

## API Referansı

**Yöntem:** `POST`  
**Uç Nokta**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| Parametre         | Tür      | Gerekli | Açıklama                                                                            |
| ----------------- | -------- | ------- | ----------------------------------------------------------------------------------- |
| `fileName`        | string   | Evet    | Çalışma kitabının adı (uzantısı dahil).                                              |
| `folder`          | string   | Hayır   | Bulut depolama klasör yolu.                                                         |
| `storage`         | string   | Hayır   | Varsayılan olmayan bir depo adı.                                                    |
| `sheetName`       | string   | Hayır   | Belirli bir çalışma sayfası adı; atlanırsa işlem tüm çalışma kitabına uygulanır.    |
| `searchString`    | string   | Evet    | Aranacak metin.                                                                     |
| `replaceString`   | string   | Evet    | Bulunan ögelerin değiştirileceği metin.                                             |
| `ignoreCase`      | boolean  | Hayır   | Büyük/küçük harf duyarsız arama yapmak için `true` olarak ayarlayın.                |
| `matchWholeCell`  | boolean  | Hayır   | Sadece tüm hücre eşleşmelerini değiştirmek için `true` olarak ayarlayın.            |

**Başlıklar**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**İstek Gövdesi (JSON)**

```json
{
  "searchString": "EskiDeger",
  "replaceString": "YeniDeger",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Sayfa1"
}
```

**Başarılı Yanıt (JSON)**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## Desteklenen Formatlar

| Format                                | Uzantı                    |
| ------------------------------------- | ------------------------- |
| Excel Çalışma Kitabı                  | .xls, .xlsx, .xlsm, .xlsb |
| OpenDocument Elektronik Tablosu       | .ods                      |
| CSV                                   | .csv                      |
| Diğerleri (Aspose.Cells tarafından desteklenenler) | —                         |

## Kod Örnekleri

Aşağıda, üç popüler SDK için minimum örnekler verilmiştir. `{clientId}`, `{clientSecret}` ve diğer yer tutucuları gerçek değerlerinizle değiştirin. Bu örnekler, **arama ve değiştirme** işlemini programatik olarak nasıl gerçekleştireceğinizi gösterir.

## Hata İşleme ve Kenar Durumları

| HTTP Kodu | Anlamı                                           | Önerilen Eylem                                                          |
| --------- | ------------------------------------------------ | ----------------------------------------------------------------------- |
| 400       | Hatalı İstek – eksik veya geçersiz parametreler | Gerekli alanları ve veri türlerini kontrol edin.                        |
| 401       | Yetkisiz – geçersiz veya süresi dolmuş belirteç | Erişim belirtecini yenileyin.                                           |
| 404       | Bulunamadı – çalışma kitabı veya çalışma sayfası yok | Dosya adını, klasör yolunu ve `sheetName` değerini kontrol edin.        |
| 415       | Desteklenmeyen Medya Türü – geçersiz dosya formatı | Yüklenecek dosyanın desteklenen Excel veya CSV formatında olduğundan emin olun. |
| 202       | Kabul Edildi – işlem işlenmek üzere kabul edildi | Eşzamansız işlem kullanılıyorsa işlemin durumunu periyodik olarak kontrol edin. |
| 204       | İçerik Yok – işlem gövdesiz başarıyla tamamlandı | Değiştirme uygulandı; ek veri döndürülmedi.                            |
| 500       | İç Sunucu Hatası – beklenmeyen hata              | Kısa bir gecikmeden sonra yeniden deneyin; sorun devam ederse Aspose desteğiyle iletişime geçin. |

**Notlar:**  
- Büyük çalışma kitapları istek boyutu sınırlarını aşabilir; bu nedenle dosyayı önce bulut depolama alanına yüklemeyi düşünün.  
- `ignoreCase` değeri `true` olarak ayarlandığında, yerel ayara özel büyük/küçük harf eşleştirmeleri sonuçları etkileyebilir.  
- Formüllerde `matchWholeCell` kullanmak, formül metni içindeki kısmi eşleşmelerin değiştirilmesine izin vermez.

## Excel dosyalarında arama ve değiştirme

- [Excel çalışma kitabından metin ögelerini alma.](/tr/cells/workbook/get-text-items/)
- [Excel çalışma sayfasından metin ögelerini alma.](/tr/cells/worksheets/get-text-items/)
- [Excel çalışma kitabından metin arama.](/tr/cells/workbook/find-text/)
- [Excel çalışma sayfasından metin arama.](/tr/cells/worksheets/find-text/)
- [Dosya yüklemeden Excel dosyalarında metin bulma.](/tr/cells/search/)
- [Excel çalışma kitabından metin değiştirme.](/tr/cells/workbook/replace-text/)
- [Excel çalışma sayfasından metin değiştirme.](/tr/cells/worksheets/replace-text/)
- [Dosya yüklemeden Excel dosyalarında metin değiştirme.](/tr/cells/replace/)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud API Kullanılarak Excel Dosyalarında Metin Arama ve Değiştirme",
  "description": "Aspose.Cells Cloud'un arama ve değiştirme uç noktası için dokümantasyon, istek formatı, parametreler, örnekler ve hata işleme yöntemlerini içerir.",
  "url": "https://docs.aspose.cloud/cells/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, arama ve değiştirme, API, REST"
}
</script>