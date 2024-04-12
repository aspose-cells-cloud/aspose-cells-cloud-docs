---
title: MHTmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/mhtmlsaveoptions/
description: "Aspose.Cells Bulut modeli spesifikasyonu: MHtmlSaveOptions. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **mHtmlSaveOptions**

 .mhtml dosyasını kaydetme seçeneklerini temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| Ekli Dosyalar Dizini| Sicim| Doğru| YANLIŞ|| Ekli dosyaların kaydedileceği dizin. Yalnızca html akışına kaydetmek için.|
| Ekli DosyalarUrlÖneki| Sicim| Doğru| YANLIŞ||Html dosyasındaki resim gibi ekli dosyaların Url önekini belirtin. Yalnızca html akışına kaydetmek için.|
| Kodlama| Sicim| Doğru| YANLIŞ|| Ayarlanmazsa, varsayılan kodlama türü olarak Encoding.UTF8'i kullanın.|
| Yalnızca ActiveWorksheet'i Dışa Aktar| Boolean| Doğru| YANLIŞ|| Çalışma kitabının tamamının html dosyasına aktarılıp aktarılmayacağını belirtir.|
| ExportChartImageFormat| Sicim| Doğru| YANLIŞ|| Dışa aktarmadan önce grafik görüntüsünün biçimini alın veya ayarlayın|
| ExportImagesAsBase64| Boolean| Doğru| YANLIŞ|| Görüntülerin Base64 formatında HTML'e, MHTML'ye mi yoksa EPUB'a mı kaydedileceğini belirtir.|
| HiddenColDisplayType| Sicim| Doğru| YANLIŞ|| Excel'de gizli sütun (bu sütunun genişliği 0'dır), bunu html formatında kaydetmeden önce, HtmlHiddenColDisplayType "Kaldır" ise, gizli sütun çıktısı alınmaz, değer "Gizli" ise sütun çıktısı alınır, ancak gizliydi, varsayılan değer "Gizli"dir|
| HiddenRowDisplayType| Sicim| Doğru| YANLIŞ||Excel'de gizli satır (bu satırın yüksekliği 0'dır), bunu html formatında kaydetmeden önce, HtmlHiddenRowDisplayType "Kaldır" ise gizli satır çıkarılmaz, değer "Gizli" ise satırın çıktısı alınır, ancak gizliydi, varsayılan değer "Gizli"dir|
| HtmlCrossStringType| Sicim| Doğru| YANLIŞ|| Bir Excel dosyasını html formatında kaydederken hücreler arası bir dizenin MS Excel ile aynı şekilde görüntülenip görüntülenmeyeceğini belirtir. Varsayılan olarak değer Varsayılan'dır, dolayısıyla hücreler arası dizeler için, Aspose.Cells ve MS Excel tarafından oluşturulan html dosyaları arasında çok az fark vardır. Ancak büyük html dosyaları oluşturma performansı, değeri Çapraz olarak ayarlamak, bundan birkaç kat daha hızlı olacaktır. Varsayılan veya Fit2Cell olarak ayarlayarak.|
| IsExpImageToTempDir| Boolean| Doğru| YANLIŞ|| Görüntü dosyalarının geçici dizine aktarılıp aktarılmayacağını belirtir. Yalnızca html akışına kaydetmek için.|
| Sayfa başlığı| Sicim| Doğru| YANLIŞ||Html sayfasının başlığı. Yalnızca html akışına kaydetmek için.|
| AyrıştırmaHtmlTagInCell| Boolean| Doğru| YANLIŞ|| Hücredeki html etiketini, hücre değeri olarak veya html etiketi olarak ayrıştırın, varsayılan değer doğrudur|
| Formatı Kaydet| Sicim| Doğru| YANLIŞ|||
| Önbelleğe Alınmış DosyaKlasörü| Sicim| Doğru| YANLIŞ|||
| Net veriler| Boolean| Doğru| YANLIŞ|||
| Dizin Oluştur| Boolean| Doğru| YANLIŞ|||
| HTTPSıkıştırmayı Etkinleştir| Boolean| Doğru| YANLIŞ|||
| Grafik Önbelleğini Yenile| Boolean| Doğru| YANLIŞ|||
|SıralamaAdları| Boolean| Doğru| YANLIŞ|||
| Birleştirilmiş Alanları Doğrula| Boolean| Doğru| YANLIŞ|||

**Ebeveyn adı** : (KaydetmeSeçenekleri)[kaydetmeseçenekleri]