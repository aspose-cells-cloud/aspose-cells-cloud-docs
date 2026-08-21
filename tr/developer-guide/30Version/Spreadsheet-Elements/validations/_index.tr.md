---
title: "Excel Veri Doğrulama ile Çalışmak"
second_title: "Belge"
linktype: "Doğrulamalar"
type: docs
url: /tr/validations/
keywords: "Excel veri doğrulama, Aspose.Cells Cloud, REST API, elektronik tablo, Office Cloud"
description: "Aspose.Cells Cloud REST API ile Excel veri doğrulama kurallarını programlı olarak nasıl ekleyeceğinizi, alacağınızı, güncelleyeceğinizi, sileceğinizi ve temizleyeceğinizi öğrenin. .NET, Java, Python ve PHP için örnekler içerir."
weight: 100
ArticleTitle: "Excel Veri Doğrulama ile Çalışmak - Aspose.Cells Cloud API Dokümantasyonu"
---

Excel veri doğrulama, Microsoft Excel'de bir çalışma sayfası hücresine kullanıcı tarafından ne girilebileceğini kontrol etmek için kullanılan bir özelliktir. Girdileri belirli bir tarih aralığına, yalnızca tam sayılara veya hatta alanı tasarruf edip tek bir hücrede değerleri görüntüleyen açılır listelere kısıtlayabilir. Ayrıca, kullanıcı hatalı bir değer veya geçersiz bir biçim girdiğinde görünecek özel bir mesaj tanımlayabilirsiniz.

Örneğin, bir kullanıcı 9:00 ile 18:00 arasında gerçekleşen bir toplantı belirleyebilir.

Veri doğrulama, bir değerın pozitif bir sayı, bir ayın 15’i ile 30’u arasında bir tarih, sonraki 30 gün içinde gerçekleşen bir tarih veya 25 karakterden az içeren bir metin girdisi olduğundan emin olmak için kullanılabilir ve böylece devam eder.

### API Özeti

| İşlem | HTTP Yöntemi | Uç Nokta | Açıklama |
|-------|--------------|----------|-----------|
| Ekle | POST | `/cells/{file}/worksheets/{sheet}/validations` | Bir doğrulama kuralı oluştur |
| Al | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Belirli bir kuralı al |
| Tümünü Al | GET | `/cells/{file}/worksheets/{sheet}/validations` | Tüm kuralları listele |
| Güncelle | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Bir kuralı değiştir |
| Sil | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Bir kuralı kaldır |
| Temizle | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | Tüm kuralları kaldır |

## Excel dosyası üzerinde doğrulamalarla çalışma

- [Excel çalışma sayfasına nasıl doğrulama kuralı eklenir](/cells/validations/add/)
- [Excel çalışma sayfasından nasıl doğrulama kuralı alınır](/cells/validations/get/)
- [Excel çalışma sayfasından tüm doğrulama kuralları nasıl alınır](/cells/validations/get-all/)
- [Excel çalışma sayfasından nasıl doğrulama kuralı silinir](/cells/validations/delete/)
- [Excel çalışma sayfasından tüm doğrulama kuralları nasıl temizlenir](/cells/validations/clear/)
- [Excel çalışma sayfasında nasıl doğrulama kuralı güncellenir](/cells/validations/update/)