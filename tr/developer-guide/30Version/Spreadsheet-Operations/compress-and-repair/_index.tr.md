---
title: "Excel Dosyalarını Sıkıştırma ve Onarma"
second_title: "Belge"
type: docs
url: /tr/compress-and-repair-excel-files/
linktitle: "Sıkıştırma ve Onarma"
keywords: "Aspose.Cells, Excel sıkıştırma, Excel onarma, bulut API, Excel dosya boyutunu küçültme, bozuk çalışma kitabını onarma, Excel dosyası sıkıştırma, Excel çalışma kitabını onarma"
description: "Aspose.Cells Cloud API kullanarak büyük Excel çalışma kitaplarını nasıl sıkıştıracağınızı ve bozuk dosyaları nasıl onaracağınızı öğrenin. Adım adım örnekler, desteklenen diller ve en iyi uygulamalar."
weight: 100
ArticleTitle: "Excel Dosyalarını Sıkıştırma ve Onarma – Aspose.Cells Cloud API"
---

Bir Excel çalışma kitabını sıkıştırmak, kullanılmayan stilleri, resimleri ve paylaşılan dizeleri kaldırarak dosya boyutunu küçültürken, onarmak bozuk çalışma kitaplarının bütünlüğünü geri yükler. Aspose.Cells Cloud API, bu iki işlem için özel uç noktalar sunar.

- **[Excel dosyasındaki verileri sıkıştırın](https://docs.aspose.cloud/cells/compress-excel-files/).**
- **[Excel Dosyalarını Onarın](https://docs.aspose.cloud/cells/repair-excel-files/).**

**Çalışma Kitabını Sıkıştırma API’si**  
**Sıkıştır** işlemi basit bir POST isteği ile gerçekleştirilir. Aşağıda tam bir istek/yanıt tanımlaması bulunmaktadır:

| Yöntem | Uç Nokta | Gerekli Parametreler | İstek Gövdesi | Örnek Yanıt | Tipik Durum Kodları |
|--------|----------|---------------------|--------------|-----------------|----------------------|
| POST   | `/cells/compress` | `file` (ikili) – sıkıştırılacak çalışma kitabı; isteğe bağlı `outPath` (dize) – hedef yol | *Yok* (dosya multipart/form‑data olarak gönderilir) | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**Çalışma Kitabını Onarma API’si**  
**Onar** işlemi de bir POST isteği ile gerçekleştirilir. Tanımlaması aşağıdaki gibidir:

| Yöntem | Uç Nokta | Gerekli Parametreler | İstek Gövdesi | Örnek Yanıt | Tipik Durum Kodları |
|--------|----------|---------------------|--------------|-----------------|----------------------|
| POST   | `/cells/repair` | `file` (ikili) – bozuk çalışma kitabı; isteğe bağlı `outPath` (dize) – onarılmış dosyanın kaydedileceği yol | *Yok* (dosya multipart/form‑data olarak gönderilir) | `{ "isRepaired": true, "message": "Çalışma kitabı başarıyla onarıldı." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

Bu tablolar, geliştiricilerin diğer yerlere girmeden API’leri doğrudan çağırmak için gerekli temel bilgileri sağlar.

**Ek Kaynaklar**  
- Kullanılmayan satır ve sütunları kaldırma gibi gelişmiş seçenekler için tam **[Excel Dosyalarını Sıkıştırma](/tr/compress-excel-files/)** kılavuzuna bakın.  
- Sorun giderme ipuçları ve hata kodu açıklamaları için **[Excel Dosyalarını Onarma](/tr/repair-excel-files/)** belgelerini inceleyin.  
- Aspose.Cells Cloud API’nin daha kapsamlı bir anlayışı için **[Dosya Bilgisi Alın](/tr/file-info/)** ve **[Elektronik Tablo İşlemleri](/tr/spreadsheet-operations/)** gibi ilgili işlemlere de göz atın.  
---