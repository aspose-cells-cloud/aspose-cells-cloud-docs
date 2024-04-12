---
title: HtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/htmlsaveoptions/
description: "Aspose.Cells Bulut modeli spesifikasyonu: HtmlSaveOptions. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **htmlKaydetmeSeçenekleri**

 .html dosyasını kaydetme seçeneklerini temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| Sayfa Başlıklarını Dışa Aktar| Boolean| Doğru| YANLIŞ|||
| Sayfayı Dışa Aktarma Altbilgileri| Boolean| Doğru| YANLIŞ|||
| ExportRowColumnBaşlıkları| Boolean| Doğru| YANLIŞ|||
| Tüm Sayfaları Göster| Boolean| Doğru| YANLIŞ|||
| Resim Seçenekleri| Sınıf:ImageOrPrintOptions| Doğru| YANLIŞ|||
| Tek Dosya Olarak Farklı Kaydet| Boolean| Doğru| YANLIŞ|| Html'nin tek dosya olarak kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer false'tur.|
| GizliÇalışma Sayfasını Dışa Aktar| Boolean| Doğru| YANLIŞ|| Html'nin tek dosya olarak kaydedilip kaydedilmeyeceğini belirtir. Varsayılan değer false'tur.|
| Izgara Çizgilerini Dışa Aktar| Boolean| Doğru| YANLIŞ||Kılavuz çizgilerinin dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer false'tur.|
| Sunum Tercihi| Boolean| Doğru| YANLIŞ|| Sunum tercihinin html mi yoksa mht dosyası mı olduğunu belirtir. Varsayılan değer false'tur. Daha güzel bir sunum istiyorsanız lütfen değeri true olarak ayarlayın.|
| CellCssÖneki| Sicim| Doğru| YANLIŞ|| Css adının önekini alır ve ayarlar, varsayılan değer ""'dir.|
| TabloCssId| Sicim| Doğru| YANLIŞ|| Tr,col,td vb. gibi css türünün önekini alır ve ayarlar; bunlar, belirli TableCssId niteliğine sahip tablo öğesinde bulunur. Varsayılan değer ""dir.|
| IsFullPathLink| Boolean| Doğru| YANLIŞ|| Sheet00x.htm,filelist.xml ve tabstrip.htm'de tam yol bağlantısının kullanılıp kullanılmayacağını belirtir. Varsayılan değer false'tur.|
| Çalışma Sayfasını Dışa AktarCSSAyrı Olarak| Boolean| Doğru| YANLIŞ|| Çalışma sayfası css'sinin ayrı olarak dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer false'tur.|
| Benzer Kenarlık Stilini Dışa Aktar| Boolean| Doğru| YANLIŞ|||
| BoşTd'yiZorla Birleştir| Boolean| Doğru| YANLIŞ||Dosyayı html'ye aktarırken boş TD öğesinin zorla birleştirilip birleştirilmeyeceğini belirtir. Değeri true olarak ayarladıktan sonra html dosyasının boyutu önemli ölçüde azalacaktır. Varsayılan değer false'tur. Html dosyasını excel'e aktarmak veya dosyayı html'ye kaydederken mükemmel ızgara çizgilerini dışa aktarmak istiyorsanız lütfen varsayılan değeri koruyun.|
| Dışa AktarmaHücre Koordinatı| Boolean| Doğru| YANLIŞ|| Dosyayı html'ye kaydederken boş olmayan hücrelerin excel koordinatlarının dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer false'tur. Çıktı html'sini excel'e aktarmak istiyorsanız lütfen varsayılan değeri koruyun.|
| Ekstra Başlıkları Dışa Aktar| Boolean| Doğru| YANLIŞ|| Metin uzunluğu maksimum görüntüleme sütunundan uzun olduğunda ekstra başlıkların dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer false'tur. Html dosyasını excel'e aktarmak istiyorsanız lütfen varsayılan değeri koruyun.|
| Dışa Aktarma Başlıkları| Boolean| Doğru| YANLIŞ||Dosyayı html'ye kaydederken başlıkların dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer false'tur. Html dosyasını excel'e aktarmak istiyorsanız lütfen varsayılan değeri koruyun.|
| Dışa Aktarma Formülü| Boolean| Doğru| YANLIŞ|| Dosyayı html'ye kaydederken formülün dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer doğrudur. Çıktı html'sini excel'e aktarmak istiyorsanız lütfen varsayılan değeri koruyun|
| Araç İpucu Metni Ekle| Boolean| Doğru| YANLIŞ|| Veriler tam olarak görüntülenemediğinde araç ipucu metninin eklenip eklenmeyeceğini belirtir.|
| BogusRowData'yı Dışa Aktar| Boolean| Doğru| YANLIŞ|| Sahte alt satır verilerinin dışa aktarılıp aktarılmadığını belirtir. Varsayılan değer true'dur. Html veya mht dosyasını excel'e aktarmak istiyorsanız lütfen varsayılan değeri koruyun.|
| Kullanılmayan Stilleri Hariç Tut| Boolean| Doğru| YANLIŞ|| Kullanılmayan stillerin hariç tutulup tutulmayacağını belirtir.Varsayılan değer false'tur.Html veya mht dosyasını excel'e aktarmak istiyorsanız, lütfen varsayılan değeri koruyun.|
| Belgeyi Dışa Aktarma Özellikleri| Boolean| Doğru| YANLIŞ||Belge özelliklerinin dışa aktarılıp aktarılmayacağını belirtir.Varsayılan değer true'dur.Html veya mht dosyasını excel'e aktarmak istiyorsanız lütfen varsayılan değeri koruyun.|
| Çalışma Sayfası Özelliklerini Dışa Aktar| Boolean| Doğru| YANLIŞ|| Çalışma sayfası özelliklerinin dışa aktarılıp aktarılmayacağını belirtir.Varsayılan değer true'dur.Html veya mht dosyasını excel'e aktarmak istiyorsanız lütfen varsayılan değeri koruyun.|
| Çalışma Kitabı Özelliklerini Dışa Aktar| Boolean| Doğru| YANLIŞ|| Çalışma kitabı özelliklerinin dışa aktarılıp aktarılmayacağını belirtir.Varsayılan değer true'dur.Html veya mht dosyasını excel'e aktarmak istiyorsanız, lütfen varsayılan değeri koruyun.|
| FrameScriptsAndProperties'i Dışa Aktar| Boolean| Doğru| YANLIŞ|| Çerçeve komut dosyalarının ve belge özelliklerinin dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer true'dur. Html veya mht dosyasını excel'e aktarmak istiyorsanız lütfen varsayılan değeri koruyun.|
| Ekli Dosyalar Dizini| Sicim| Doğru| YANLIŞ|| Ekli dosyaların kaydedileceği dizin. Yalnızca html akışına kaydetmek için.|
| Ekli DosyalarUrlÖneki| Sicim| Doğru| YANLIŞ||Html dosyasındaki resim gibi ekli dosyaların Url önekini belirtin. Yalnızca html akışına kaydetmek için.|
| Kodlama| Sicim| Doğru| YANLIŞ|||
| Yalnızca ActiveWorksheet'i Dışa Aktar| Boolean| Doğru| YANLIŞ|| Çalışma kitabının tamamının html dosyasına aktarılıp aktarılmayacağını belirtir.|
| ExportChartImageFormat| Sicim| Doğru| YANLIŞ|| Dışa aktarmadan önce grafik görüntüsünün biçimini alın veya ayarlayın|
| ExportImagesAsBase64| Boolean| Doğru| YANLIŞ|||
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