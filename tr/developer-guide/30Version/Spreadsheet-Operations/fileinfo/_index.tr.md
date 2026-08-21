---
title: "Dosya Bilgisi"
second_title: "Belge"
linktype: "Dosya Bilgisi"
type: docs
url: /file-info/
keywords: "Dosya, Bilgi, Excel, Aspose.Cells, Bulut API, Meta Veri, Base64"
description: "Aspose.Cells Bulut API kullanarak Excel dosyasının adını, boyutunu ve Base64 içeriğini alın. İstek sözdizimi, örnek kod ve hata işleme içerir."
weight: 79
ArticleTitle: "Dosya Bilgisi – Excel Dosyası Meta Verisi ve Base64 İçeriği (Aspose.Cells Bulut API)"
---

## FileInfo Özellikleri


| Adı             | Tür    | Açıklama                                            |
| --------------- | ------ | --------------------------------------------------- |
| **FileName**    | string | Dosyanın uzantısı dahil tam adı.                     |
| **FileSize**    | long   | Dosyanın bayt cinsinden boyutu.                     |
| **FileContent** | string | Base64 ile kodlanmış ham Excel dosyası verilerini içerir. |

Yanıt, yukarıdaki tabloda gösterilen aynı üç özellik içeren JSON olarak döndürülür; örneğin:

```json
{
  "FileName": "MyWorkbook.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### Hatalar

| HTTP Kodu | Anlam                   | Ne Zaman Oluşur                           |
| --------- | ----------------------- | ---------------------------------------- |
| 200       | Tamam – istek başarılı. | Normal yanıt.                            |
| 401       | Yetkisiz                | Eksik veya geçersiz kimlik doğrulama belirteci. |
| 404       | Bulunamadı              | Belirtilen dosya mevcut değil.           |
| 500       | Sunucu İç Hatası        | Beklenmeyen sunucu tarafı hatası.        |

Her hata için, kimlik doğrulama belirtecini geçerli olduğunu kontrol edin (401), dosya yolunu doğrulayın (404) veya yeniden deneme stratejileri için genel hata işleme kılavuzunu inceleyin (500).

## Ayrıca Bkz.

- [Çalışma Kitabını Al](https://docs.aspose.cloud/cells/get-workbook) – bir çalışma kitabı nesnesini ve çalışma sayfalarını alın.  
- [Dosyayı İndir](https://docs.aspose.cloud/cells/download-file) – Base64 kodlaması olmadan ham dosya baytlarını indirin.  
- [Kimlik Doğrulama Genel Bakışı](https://docs.aspose.cloud/cells/authentication) – erişim belirteçlerinin nasıl alınacağını ve nasıl kullanılacağını öğrenin.  
---