---
title: Sayfalandırılmış Kaydetme Seçeneği
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/paginatedsaveoptions/
description: "Aspose.Cells Bulut modeli spesifikasyonu: PaginatedSaveOptions. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **sayfalandırılmışKaydetmeSeçenekleri**

 Sayfalandırma seçeneklerini temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| Varsayılan yazı tipi| Sicim| Doğru| YANLIŞ||Excel'deki karakterler Unicode olduğunda ve hücre stilinde doğru yazı tipiyle ayarlanmadığında, pdf, image'da blok olarak görünebilirler. Bu karakterleri göstermek için MingLiu veya MS Gotik gibi Varsayılan Yazı Tipini ayarlayın. Bu özellik ayarlanmazsa, Aspose.Cells bu unicode karakterleri göstermek için sistem varsayılan yazı tipini kullanır.|
| CheckWorkbookDefaultYazı Tipi| Boolean| Doğru| YANLIŞ|| Excel'deki karakterler Unicode olduğunda ve hücre stilinde doğru yazı tipiyle ayarlanmadığında, pdf, resimde blok olarak görünebilirler. Önce bu karakterleri göstermek üzere çalışma kitabının varsayılan yazı tipini kullanmayı denemek için bunu true olarak ayarlayın.|
| Yazı Tipi Uyumluluğunu Kontrol Edin| Boolean| Doğru| YANLIŞ|| Metindeki her karakter için yazı tipi uyumluluğunun kontrol edilip edilmeyeceğini belirtir.|
| IsFontSubstitutionChar Ayrıntı Düzeyi| Boolean| Doğru| YANLIŞ|| Yalnızca hücre yazı tipi uyumlu olmadığında karakterin yazı tipinin değiştirilip değiştirilmeyeceğini belirtir.|
| Sayfa Başına Bir Sayfa| Boolean| Doğru| YANLIŞ|| OnePagePerSheet true ise, bir sayfanın tüm içeriği sonuçta yalnızca bir sayfaya yazdırılacaktır. Pagesetup'ın kağıt boyutu geçersiz olacak ve pagesetup'ın diğer ayarları hala geçerli olacaktır.|
| TümüSütunlarBirSayfaBaşınaSayfa| Boolean| Doğru| YANLIŞ||AllColumnsInOnePagePerSheet true ise, bir sayfanın tüm sütun içeriği sonuçta yalnızca bir sayfaya çıkarılacaktır. Pagesetup'ın kağıt boyutunun genişliği göz ardı edilecek ve pagesetup'ın diğer ayarları etkili olmaya devam edecektir.|
| Hatayı Yoksay| Boolean| Doğru| YANLIŞ|| Oluşturma sırasında hatayı gizlemeniz gerekip gerekmediğini belirtir. Hata, şekil, resim, grafik oluşturma vb. hatalardan kaynaklanabilir.|
| Çıktı Boş Sayfa Yazdırılacak Hiçbir Şey Yokken| Boolean| Doğru| YANLIŞ|| Yazdırılacak bir şey olmadığında boş sayfa çıktısının alınıp alınmayacağını belirtir.|
| Sayfa Dizini| Tamsayı| Doğru| YANLIŞ|| Kaydedilecek ilk sayfanın 0 tabanlı dizinini alır veya ayarlar.|
| Sayfa sayısı| Tamsayı| Doğru| YANLIŞ|| Kaydedilecek sayfa sayısını alır veya ayarlar.|
| YazdırmaSayfa Türü| Sicim| Doğru| YANLIŞ|| Hangi sayfaların yazdırılmayacağını belirtir.|
| Kılavuz Çizgisi Türü| Sicim| Doğru| YANLIŞ|| Kılavuz çizgisi türünü alır veya ayarlar.|
| MetinÇapraz Türü| Sicim| Doğru| YANLIŞ|| Metin genişliği hücre genişliğinden büyük olduğunda görüntülenen metin türünü alır veya ayarlar.|
| VarsayılanDilDüzenle| Sicim| Doğru| YANLIŞ|| Varsayılan düzenleme dilini alır veya ayarlar.|
| EmfRenderSetting| Sicim| Doğru| YANLIŞ|||
| Alanları Birleştir| Boolean| Doğru| YANLIŞ|||
|DışAdları Sırala| Boolean| Doğru| YANLIŞ|||
| GüncellemeSmartArt| Boolean| Doğru| YANLIŞ|||
| Formatı Kaydet| Sicim| Doğru| YANLIŞ|||
| Önbelleğe Alınmış DosyaKlasörü| Sicim| Doğru| YANLIŞ|||
| Net veriler| Boolean| Doğru| YANLIŞ|||
| Dizin Oluştur| Boolean| Doğru| YANLIŞ|||
| HTTPSıkıştırmayı Etkinleştir| Boolean| Doğru| YANLIŞ|||
| Grafik Önbelleğini Yenile| Boolean| Doğru| YANLIŞ|||
|SıralamaAdları| Boolean| Doğru| YANLIŞ|||
| Birleştirilmiş Alanları Doğrula| Boolean| Doğru| YANLIŞ|||

**Ebeveyn adı** : (KaydetmeSeçenekleri)[kaydetmeseçenekleri]**Çocuk Adı** : 
	-  [DocxSaveOptions](docxsaveoptions) 
	-  [PptxSaveOptions](pptxsaveoptions) 
	-  [XpsSaveOptions](xpssaveoptions) 
