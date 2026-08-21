---
title: "Bir Excel Çalışma Sayfasında Satırları Silme İşlemleri"
second_title: "Belge"
linktitle: "Sil"
type: docs
url: /tr/rows/delete/
keywords: "Aspose.Cells, satır sil, Excel API, REST, bulut, elektronik tablo, Excel, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında tek veya birden fazla satırı nasıl sileceğinizi öğrenin. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift için kod örnekleri içerir."
weight: 20
ArticleTitle: "Bir Excel Çalışma Sayfasında Satırları Silme İşlemleri – Aspose.Cells Cloud API Kılavuzu"
---

## Kullanılabilir Silme İşlemleri

Aşağıdaki örnekler, Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından tek bir boş satırı veya birden fazla satırı nasıl sileceğinizi göstermektedir.

- [Bir Excel çalışma sayfasında boş bir satırı silme](/cells/rows/delete/row/)
- [Bir Excel çalışma sayfasında birden fazla satırı silme](/cells/rows/delete/rows/)

**API Referansı**

| Öğe                 | Detaylar |
|---------------------|---------------------------------------------------------------|
| **HTTP Yöntemi**     | DELETE |
| **Uç Nokta**        | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **Yol Parametreleri**| `fileName` – Excel dosyasının adı (zorunlu)<br>`sheetName` – çalışma sayfasının adı (zorunlu) |
| **Sorgu Parametreleri**| `startrow` – silinecek ilk satırın indeksi (zorunlu)<br>`totalRows` – silinecek satır sayısı (zorunlu)<br>`storage` – bulut depo adı (isteğe bağlı)<br>`folder` – depodaki klasör yolu (isteğe bağlı) |
| **İstek Gövdesi**    | *Yok* |
| **Yanıt Örneği**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **Olası Durum Kodları**| 200 OK – satırlar başarıyla silindi<br>400 Bad Request – geçersiz parametreler<br>401 Unauthorized – kimlik doğrulama hatası<br>404 Not Found – dosya veya çalışma sayfası bulunamadı<br>500 Internal Server Error – sunucu tarafında sorun |

**Ayrıca bakınız**

- [Satır Ekle](/cells/rows/add/)
- [Satırı Al](/cells/rows/get/)
- [Satırı Kopyala](/cells/rows/copy/)
- [Satırı Gizle](/cells/rows/hide/)
- [Satırlara Genel Bakış](/cells/rows/)
---