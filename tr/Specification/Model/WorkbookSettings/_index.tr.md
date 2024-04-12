---
title: Çalışma Kitabı Ayarı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/workbooksettings/
description: "Aspose.Cells Bulut modeli spesifikasyonu: WorkbookSettings. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **çalışma kitabıAyarlar**

 

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| Otomatik SıkıştırmaResimleri| Boolean| Doğru| YANLIŞ|| Uygulamanın çalışma kitabındaki resimleri otomatik olarak sıkıştırdığını gösteren bir boole değeri belirtir.|
| Otomatik Kurtarma| Boolean| Doğru| YANLIŞ|| Dosyanın otomatik kurtarma için işaretlenip işaretlenmediğini belirtir.|
| Derleme Sürümü| Sicim| Doğru| YANLIŞ|| Uygulamanın artımlı genel yayınını belirtir.|
| Hesap Modu| Sicim| Doğru| YANLIŞ||Çoklu tablo işlemleri dışında formüllerin manuel mi, otomatik mi yoksa otomatik olarak mı hesaplanacağını belirtir.|
| Hesaplama Kimliği| Sicim| Doğru| YANLIŞ|| Çalışma kitabındaki değerleri hesaplamak için kullanılan hesaplama altyapısının sürümünü belirtir.|
| Uyumluluğu Kontrol Edin| Boolean| Doğru| YANLIŞ|| Çalışma kitabını kaydederken uyumluluğun kontrol edilip edilmeyeceğini belirtir. Açıklamalar: Varsayılan değer true'dur.|
| CheckExcelKısıtlaması| Boolean| Doğru| YANLIŞ||Kullanıcı hücrelerle ilgili nesneleri değiştirdiğinde excel dosyasının kısıtlamasının kontrol edilip edilmeyeceği. Örneğin Excel, 32K'dan uzun dize değerinin girilmesine izin vermez. Cell.PutValue(string) gibi 32K'dan daha uzun bir değer girdiğinizde, bu özellik doğruysa bir Exception alırsınız. Bu özellik false ise giriş dizesi değerinizi hücrenin değeri olarak kabul edeceğiz, böylece daha sonra CSV gibi diğer dosya biçimleri için dize değerinin tamamının çıktısını alabilirsiniz. Ancak excel dosya formatı için geçersiz bir değer belirlediyseniz çalışma kitabını daha sonra excel dosya formatı olarak kaydetmemelisiniz. Aksi takdirde oluşturulan excel dosyasında beklenmeyen hatalar oluşabilir.|
| Kilitlenme Kaydetme| Boolean| Doğru| YANLIŞ|| uygulamanın bir kilitlenmeden sonra çalışma kitabı dosyasını en son kaydedip kaydetmediğini gösterir.|
| CalcChain Oluştur| Boolean| Doğru| YANLIŞ|| Hesaplanan formüller zincirini oluşturup oluşturmadığı. Varsayılan yanlıştır.|
| Veri Çıkarma Yükü| Boolean| Doğru| YANLIŞ||uygulamanın veri kurtarma için çalışma kitabını en son açıp açmadığını gösterir.|
| Tarih1904| Boolean| Doğru| YANLIŞ|| Çalışma kitabının 1904 tarih sistemini kullanıp kullanmadığını temsil eden bir değer alır veya ayarlar.|
| DisplayDrawingObjects| Sicim| Doğru| YANLIŞ|| Çalışma kitabındaki nesnelerin gösterilip gösterilmeyeceğini ve nasıl gösterileceğini belirtir.|
| Makroları Etkinleştir| Boolean| Doğru| YANLIŞ|| Makroları etkinleştirin;|
| İlk Görünür Sekme| Tamsayı| Doğru| YANLIŞ|| İlk görünür çalışma sayfası sekmesini alır veya ayarlar.|
| PivotFieldList'i Gizle| Boolean| Doğru| YANLIŞ|| PivotTable için alan listesinin gizlenip gizlenmeyeceğini alır ve ayarlar.|
| IsDefaultŞifrelenmiş| Boolean| Doğru| YANLIŞ|| Çalışma kitabının Yapısı ve Windows'i kilitliyse, çalışma kitabının varsayılan parolayla şifrelenip şifrelenmeyeceğini belirtir.|
| Gizli| Boolean| Doğru| YANLIŞ|| Bu çalışma kitabının gizli olup olmadığını gösterir.|
| IsHScrollBarVisible| Boolean| Doğru| YANLIŞ|| Oluşturulan elektronik tablonun yatay kaydırma çubuğu içerip içermeyeceğini belirten bir değer alır veya ayarlar.|
| Minimize Edilmiş| Boolean| Doğru| YANLIŞ|| Oluşturulan elektronik tablonun Küçültülmüş olarak açılıp açılmayacağını temsil eder.|
| IsVScrollBarVisible| Boolean| Doğru| YANLIŞ||Oluşturulan elektronik tablonun dikey kaydırma çubuğu içerip içermeyeceğini belirten bir değer alır veya ayarlar.|
| Yineleme| Boolean| Doğru| YANLIŞ|| Döngüsel referansları çözümlemek için yinelemeli hesaplamanın etkinleştirilip etkinleştirilmeyeceğini belirtir.|
| Dil kodu| Sicim| Doğru| YANLIŞ|| Dosyayı kaydeden CountryCode'a göre Çalışma Kitabı sürümünün kullanıcı arayüzü dilini alır veya ayarlar.|
| Maksimum Değişim| Yüzer| Doğru| YANLIŞ|| Döngüsel bir referansı çözümlemek için maksimum değişiklik sayısını döndürür veya ayarlar.|
| Maksimum Yineleme| Tamsayı| Doğru| YANLIŞ|| Döngüsel bir referansı çözümlemek için maksimum yineleme sayısını döndürür veya ayarlar.|
| Bellek Ayarı| Sicim| Doğru| YANLIŞ|| Bellek kullanım seçeneklerini alır veya ayarlar. Yeni seçenek, yeni oluşturulan çalışma sayfaları için varsayılan seçenek olarak alınacaktır ancak mevcut çalışma sayfaları için geçerli değildir.|
| SayıOndalık Ayırıcı| Sicim| Doğru| YANLIŞ|| Sayısal değerleri biçimlendirmek/ayrıştırmak için ondalık ayırıcıyı alır veya ayarlar. Varsayılan, geçerli Bölgenin ondalık ayırıcısıdır.|
| NumaraGrup Ayırıcı| Sicim| Doğru| YANLIŞ|| Sayısal değerlerde ondalık sayının solundaki basamak gruplarını ayıran karakteri alır veya ayarlar. Varsayılan, geçerli Bölgenin grup ayırıcısıdır.|
| AyrıştırmaFormulaOnOpen| Boolean| Doğru| YANLIŞ||Dosya okunurken formülün ayrıştırılıp ayrıştırılmayacağını belirtir.|
| Görüntülendiği Gibi Hassasiyet| Boolean| Doğru| YANLIŞ|| Bu çalışma kitabındaki hesaplamalar yalnızca görüntülenen sayıların kesinliği kullanılarak yapılacaksa doğrudur|
| Kaydetmeden Önce Yeniden Hesapla| Boolean| Doğru| YANLIŞ|| Belgeyi kaydetmeden önce yeniden hesaplama yapılıp yapılmayacağını belirtir.|
| Açıldığında Yeniden Hesapla| Boolean| Doğru| YANLIŞ|| Dosya açıldığında tüm formüllerin yeniden hesaplanıp hesaplanmayacağını belirtir.|
| Tavsiye Edin Salt Okunur| Boolean| Doğru| YANLIŞ|| Salt Okunur Önerilen seçeneğinin seçilip seçilmediğini gösterir.|
| Bölge| Sicim| Doğru| YANLIŞ|| Çalışma kitabının bölgesel ayarlarını alır veya ayarlar.|
| Kişisel Bilgileri Kaldır| Boolean| Doğru| YANLIŞ|| Kişisel bilgiler belirtilen çalışma kitabından kaldırılabiliyorsa doğrudur.|
| OnarımYük| Boolean| Doğru| YANLIŞ|| Uygulamanın çalışma kitabını en son güvenli modda mı yoksa onarım modunda mı açtığını belirtir.|
| Paylaşıldı| Boolean| Doğru| YANLIŞ|| Çalışma Kitabının paylaşılıp paylaşılmadığını gösteren bir değer alır veya ayarlar.|
| SheetTabBarWidth| Tamsayı| Doğru| YANLIŞ|| Çalışma sayfası sekme çubuğunun genişliği (pencere genişliğinin 1/1000'i kadar).|
| Sekmeleri Göster| Boolean| Doğru| YANLIŞ||Çalışma Kitabı sekmelerinin görüntülenip görüntülenmeyeceğine dair bir değer alın veya ayarlar.|
| Bitişik Hücreleri Güncelle Kenarlık| Boolean| Doğru| YANLIŞ|| Bitişik hücrelerin kenarlarının güncellenip güncellenmeyeceğini belirtir.|
| Bağlantı Türünü Güncelle| Sicim| Doğru| YANLIŞ|| Çalışma kitabı açıldığında dış bağlantıların nasıl güncelleştirileceğini alır ve ayarlar.|
| Pencere Yüksekliği| Yüzer| Doğru| YANLIŞ|| Nokta birimi cinsinden pencerenin yüksekliği.|
| PencereSol| Yüzer| Doğru| YANLIŞ|| Nokta birimi cinsinden istemci alanının sol kenarından pencerenin sol kenarına kadar olan mesafe.|
| PencereÜst| Yüzer| Doğru| YANLIŞ|| Nokta birimi cinsinden istemci alanının üst kenarından pencerenin üst kenarına kadar olan mesafe.|
| Pencere Genişliği| Yüzer| Doğru| YANLIŞ|| Nokta birimi cinsinden pencerenin genişliği.|
| Yazar| Sicim| Doğru| YANLIŞ|| Dosyanın yazarını alır ve ayarlar.|
| ÖzelNumaraBiçimini Kontrol Et| Boolean| Doğru| YANLIŞ|| Style.Custom ayarlanırken özel sayı biçiminin kontrol edilip edilmeyeceğini belirtir.|
| Koruma Türü| Sicim| Doğru| YANLIŞ|| Çalışma kitabının koruma türünü alır.|
| KüreselleşmeAyarları| Sınıf:GlobalizationSettings| Doğru| YANLIŞ|| Genelleştirme ayarlarını alır ve ayarlar.|
| Şifre| Sicim| Doğru| YANLIŞ||Çalışma Kitabı dosya şifreleme parolasını temsil eder.|
| Yazma Koruması| Sınıf:Yazma Koruması| Doğru| YANLIŞ|| Çalışma kitabı yazma koruması seçeneklerine erişim sağlar.|
| Şifrelendi| Boolean| Doğru| YANLIŞ|| Bu çalışma kitabını açmak için parola gerekip gerekmediğini gösteren bir değer alır.|
| Korunuyor| Boolean| Doğru| YANLIŞ|| Çalışma Kitabının yapısının veya penceresinin korunup korunmadığını gösteren bir değer alır.|
| MaxRow| Tamsayı| Doğru| YANLIŞ|| Sıfır tabanlı maksimum satır dizinini alır.|
| Maksimum Sütun| Tamsayı| Doğru| YANLIŞ|| Sıfır tabanlı maksimum sütun dizinini alır.|
| Önemli Rakamlar| Tamsayı| Doğru| YANLIŞ|| Önemli basamakların sayısını alır ve ayarlar. Varsayılan değer şudur.|
| Uyumluluğu Kontrol Edin| Boolean| Doğru| YANLIŞ|| Çalışma kitabını kaydederken önceki sürümlerle uyumluluğun kontrol edilip edilmeyeceğini belirtir.|
| Kağıt boyutu| Sicim| Doğru| YANLIŞ|| Varsayılan yazdırma kağıdı boyutunu alır ve ayarlar.|
| MaxRowsOfSharedFormula| Tamsayı| Doğru| YANLIŞ|| Paylaşılan formülün maksimum satır sayısını alır ve ayarlar.|
| uyma| Sicim| Doğru| YANLIŞ|| Çıktı belgesinin OOXML sürümünü belirtir. Varsayılan değer Ecma376_2006'dır.|
| AlıntıPrefixToStyle| Boolean| Doğru| YANLIŞ||Hücreye dize değeri (tek tırnak işaretiyle başlayan) girilirken özelliğin ayarlanıp ayarlanamayacağını belirtir.|
| FormülAyarları| Sınıf:FormulaSettings| Doğru| YANLIŞ|| Formülle ilgili özelliklerin ayarlarını alır.|
| ZorlaTamHesaplama| Boolean| Doğru| YANLIŞ|| Bir hesaplama her tetiklendiğinde tam olarak hesaplama yapar.|

