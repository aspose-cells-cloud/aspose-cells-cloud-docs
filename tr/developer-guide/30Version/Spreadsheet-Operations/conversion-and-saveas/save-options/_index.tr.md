---
title: "Kaydetme Seçenekleri"
second_title: "Belge"
linktitle: "Kaydetme seçenekleri"
type: docs
url: /tr/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Workbook, REST API, Dosya Biçimleri, PDF, CSV, JSON, HTTP Sıkıştırma, Grafik Önbelleği, Adlandırılmış Aralıklar, Dizin Oluşturma"
description: "Aspose.Cells Cloud REST API'sinin SaveOptions özelliklerini açıklar; geliştiricilerin birden fazla dosya formatı ve HTTP sıkıştırma, grafik önbelleği yenileme, otomatik dizin oluşturma gibi seçenekler üzerinden çalışma kitabının kaydedilme davranışını yapılandırmasını sağlar."
weight: 79
ArticleTitle: "Kaydetme Seçenekleri – Aspose.Cells Cloud REST API Dokümantasyonu"
---

# SaveOptions Özellikleri

SaveOptions, Aspose.Cells Cloud REST API'sini kullanırken bir çalışma kitabının nasıl kaydedileceğini kontrol etmenizi sağlar. Bu seçenekleri yapılandırarak HTTP sıkıştırma etkinleştirilebilir, çıktı formatı belirlenebilir, geçici depolama yönetilebilir ve grafik önbelleği yenileme ile otomatik dizin oluşturma gibi ek davranışlar kontrol edilebilir.

**Önkoşullar**  
- Kimliği doğrulanmış bir Aspose.Cells Cloud oturumu (OAuth 2.0 veya JWT).  
- Kaydetme işlemi öncesinde hedef çalışma kitabının API üzerinden yüklenmiş veya oluşturulmuş olması gerekir.

| Ad                        | Tür         | Açıklama                                                                                             | Notlar         |
| ------------------------- | ----------- | ---------------------------------------------------------------------------------------------------- | -------------- |
| **EnableHTTPCompression** | **bool?**   | Yanıta HTTP sıkıştırmanın etkinleştirilip etkinleştirilmeyeceğini belirler.                         | [isteğe bağlı] |
| **SaveFormat**            | **string**  | Çalışma kitabının kaydedileceği hedef dosya formatını belirtir.                                      | [isteğe bağlı] |
| **ClearData**             | **bool?**   | Dosyayı kaydettikten sonra çalışma kitabının boşaltılmasını sağlar.                                 | [isteğe bağlı] |
| **CachedFileFolder**      | **string**  | Büyük verilerin geçici olarak depolanması için kullanılan önbellek dosyası klasörünü belirtir.       | [isteğe bağlı] |
| **ValidateMergedAreas**   | **bool?**   | Dosyayı kaydetmeden önce birleştirilmiş alanların doğrulanıp doğrulanmayacağını belirtir. Varsayılan değer false’tur. | [isteğe bağlı] |
| **RefreshChartCache**     | **bool?**   | Kaydetme işleminden önce grafik önbellek verilerinin yenilenmesini sağlar.                          | [isteğe bağlı] |
| **CreateDirectory**       | **bool?**   | true olarak ayarlandığında ve hedef dizin mevcut değilse, dosya kaydedilmeden önce otomatik olarak oluşturulur. | [isteğe bağlı] |
| **SortNames**             | **bool?**   | Kaydetme sırasında adlandırılmış aralıkları alfabetik olarak sıralar.                               | [isteğe bağlı] |

**İstek**  
- **Metod:** `POST` (veya işlemine göre `PUT`)  
- **Uç Nokta:** `/cells/workbook/save`  
- **Başlıklar:**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **Gövde:** Yukarıdaki tabloda yer alan `SaveOptions` modelinin JSON gösterimi, çalışma kitabı verisi veya referansı ile birlikte.

**Yanıt Örneği**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "Çalışma kitabının kaydedilmesi başarıyla tamamlandı."
}
```

**HTTP Durum Kodları**

| Kod | Anlam                      | Açıklama                                              |
|-----|----------------------------|-------------------------------------------------------|
| 200 | OK (Tamam)                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)    | Geçersiz veya eksik JWT jetonu.                      |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.              |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                     |

**Notlar / Açıklamalar**  
- **CreateDirectory** seçeneği `true` olarak ayarlandığında, API hedef klasörü otomatik olarak oluşturur (eğer zaten mevcut değilse).  
- **EnableHTTPCompression** seçeneğinin etkinleştirilmesi büyük çalışma kitapları için yük boyutunu azaltabilir, ancak istemcinin gzip/deflate çözümlemesini desteklemesi gerekir.  
- **RefreshChartCache**, grafiklerin çalışma kitabının oluşturulmasından beri değişmiş olabilecek dinamik verilere dayalı olduğu durumlarda kullanılmalıdır.