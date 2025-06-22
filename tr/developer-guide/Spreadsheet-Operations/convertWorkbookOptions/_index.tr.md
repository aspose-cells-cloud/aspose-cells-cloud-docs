---
title: Çalışma Kitabını Dönüştür Seçeneği
second_title: Aspose.Cells Cloud Documen
linktitle: Çalışma Kitabını Dönüştür Seçeneği
type: docs
url: /tr/convert-workbook-options/
keywords: ConvertWorkbookOptions
description: Aspose.Cells Cloud REST API, excel dosyalarını çeşitli biçim dosyalarına dönüştürmeyi destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir.
weight: 79
kwords: Excel, Office Bulut, REST API, E-Tablo, PDF, CSV, Json, Markdown, Çalışma Kitabı Seçeneklerini Dönüştür
---
# ConvertWorkbookOptions Özellikleri

İsim | Tür | Açıklama | Notlar
------------ | ------------- | ------------- | -------------
**Veri Kaynağı** | **Nesne** | Veri dosyası kaynağı : CloudFileSystem ,RequestFiles , HttpUri. |
**[DosyaBilgisi](/hücreler/dosya-bilgisi/)** | **Nesne** | Dosya bilgisi açıklaması. Dosya adı, dosya boyutu ve dosya içeriğini (base64 dizesi) içerir. |
**[SayfaKurulumu](/hücreler/sayfa-kurulumu/)** | **Nesne** | Sayfa düzeni özellikleri. |
**KaydetSeçenekler** | **Nesne** Kaydetme Seçenekleri: DbfSaveOptions, DifSaveOptions, DocxSaveOptions, HtmlSaveOptions, XlsSaveOptions, XlsxSaveOptions, XpsSaveOptions, PngSaveOptions, JpgSaveOptions, GifSaveOptions, EmfSaveOptions, BmpSaveOptions, MdSaveOptions, NumbersSaveOptions, WmfSaveOptions, SvgSaveOptions, TxtSaveOptions, TifSaveOptions, XlsbSaveOptions |
**DönüştürBiçimlendir** | **sicim** | Dosya biçimi: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, vb. |
**ExcelKısıtlamasınıKontrol Et** | **Boolean** | Otomatik olarak sarılmış metnin türünü alır ve ayarlar. |

## **fileSource Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|DosyaKaynak Türü|Sicim|doğru| YANLIŞ||Erişilebilen ve değiştirilebilen FileSourceType türündeki FileSourceType adlı bir özellik.(CloudFileSystem/RequestFiles/HttpUri)|
|DosyaYolu|Sicim|doğru| YANLIŞ||Dosya konum yolu.|

## **DbfSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Dışa AktarDize Olarak|Boolean|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **DifSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **DocxSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|VarsayılanYazı Tipi|Sicim|doğru| YANLIŞ|||
|ÇalışmaKitabınıDenetleVarsayılanYazı Tipi|Boolean|doğru| YANLIŞ|||
|YazıtipiUyumluluğunuKontrol Et|Boolean|doğru| YANLIŞ|||
|IsFontSubstitutionCharGranularity|Boolean|doğru| YANLIŞ|||
|SayfaBaşınaBirSayfa|Boolean|doğru| YANLIŞ|||
|AllColumnsInOnePagePerSheet|Boolean|doğru| YANLIŞ|||
|Hatayı Yoksay|Boolean|doğru| YANLIŞ|||
|ÇıktıBoşSayfaHiçbirŞeyYazdırılmadığında|Boolean|doğru| YANLIŞ|||
|SayfaIndeksi|Tam sayı|doğru| YANLIŞ|||
|Sayfa Sayısı|Tam sayı|doğru| YANLIŞ|||
|YazdırmaSayfaTürü|Sicim|doğru| YANLIŞ|||
|Kılavuz Çizgi Türü|Sicim|doğru| YANLIŞ|||
|MetinÇapraz Tip|Sicim|doğru| YANLIŞ|||
|VarsayılanDüzenleDil|Sicim|doğru| YANLIŞ|||
|EmfRenderAyarları|Sicim|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **HtmlSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|ExportPageHeaders|Boolean|doğru| YANLIŞ|||
|ExportPageFooters|Boolean|doğru| YANLIŞ|||
|SatırSütunBaşlıklarınıDışa Aktar|Boolean|doğru| YANLIŞ|||
|TümSayfaları Göster|Boolean|doğru| YANLIŞ|||
|ResimSeçenekleri|Sınıf|doğru| YANLIŞ|||
|TekDosyaOlarakKaydet|Boolean|doğru| YANLIŞ|||
|GizliÇalışmaSayfasınıDışa Aktar|Boolean|doğru| YANLIŞ|||
|Izgara Çizgilerini Dışa Aktar|Boolean|doğru| YANLIŞ|||
|SunumTercih|Boolean|doğru| YANLIŞ|||
|HücreCssÖneki|Sicim|doğru| YANLIŞ|||
|TabloCssId|Sicim|doğru| YANLIŞ|||
|TamYolBağlantısı mı|Boolean|doğru| YANLIŞ|||
|ExportWorksheetCSSSeparately|Boolean|doğru| YANLIŞ|||
|BenzerSınırStili Dışa Aktar|Boolean|doğru| YANLIŞ|||
|BoşTdForcely'yi Birleştir|Boolean|doğru| YANLIŞ|||
|Hücre Koordinatını Dışa Aktar|Boolean|doğru| YANLIŞ|||
|Ekstra Başlıkları Dışa Aktar|Boolean|doğru| YANLIŞ|||
|Başlıkları Dışa Aktar|Boolean|doğru| YANLIŞ|||
|İhracatFormülü|Boolean|doğru| YANLIŞ|||
|İpucu Metni Ekle|Boolean|doğru| YANLIŞ|||
|SahteSatırVerileriniDışa Aktar|Boolean|doğru| YANLIŞ|||
|Kullanılmayan Stilleri Hariç Tut|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Dışa Aktar|Boolean|doğru| YANLIŞ|||
|ExportWorksheetProperties|Boolean|doğru| YANLIŞ|||
|ExportWorkbookProperties|Boolean|doğru| YANLIŞ|||
|ÇerçeveKomutDosyalarınıVeÖzellikleriniDışaAktar|Boolean|doğru| YANLIŞ|||
|EkliDosyalarDizin|Sicim|doğru| YANLIŞ|||
|EkliDosyalarUrlÖneki|Sicim|doğru| YANLIŞ|||
|Kodlama|Sicim|doğru| YANLIŞ|||
|YalnızcaActiveWorksheet'iDışa Aktar|Boolean|doğru| YANLIŞ|||
|GrafikGörüntüBiçiminiDışa Aktar|Sicim|doğru| YANLIŞ|||
|ResimleriBase64 Olarak Dışa Aktar|Boolean|doğru| YANLIŞ|||
|GizliColDisplayType|Sicim|doğru| YANLIŞ|||
|GizliSatırGörüntülemeTürü|Sicim|doğru| YANLIŞ|||
|HtmlÇaprazDizeTürü|Sicim|doğru| YANLIŞ|||
|Görüntüden TempDir'e|Boolean|doğru| YANLIŞ|||
|SayfaBaşlığı|Sicim|doğru| YANLIŞ|||
|AyrıştırmaHtmlTagInCell|Boolean|doğru| YANLIŞ|||
|HücreAdıÖzniteliği|Sicim|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **ImageSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|GrafikGörüntüTürü|Sicim|doğru| YANLIŞ|||
|GömülüResimAdıSvg'de|Sicim|doğru| YANLIŞ|||
|Yatay Çözünürlük|Tam sayı|doğru| YANLIŞ|||
|GörüntüBiçimi|Sicim|doğru| YANLIŞ|||
|HücreOtomatikUyumlu mu|Boolean|doğru| YANLIŞ|||
|SayfaBaşınaBirSayfa|Boolean|doğru| YANLIŞ|||
|SadeceAlan|Boolean|doğru| YANLIŞ|||
|YazdırmaSayfası|Sicim|doğru| YANLIŞ|||
|PrintWithStatusDialog|Boolean|doğru| YANLIŞ|||
|Kalite|Tam sayı|doğru| YANLIŞ|||
|TiffSıkıştırma|Sicim|doğru| YANLIŞ|||
|Dikey Çözünürlük|Tam sayı|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **JsonSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|İhracatAlanı|Sınıf|doğru| YANLIŞ|||
|BaşlıkSatırı Var|Boolean|doğru| YANLIŞ|||
|Dışa AktarDize Olarak|Boolean|doğru| YANLIŞ|||
|Girinti|Sicim|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **MarkdownSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Kodlama|Sicim|doğru| YANLIŞ|||
|Biçim Stratejisi|Sicim|doğru| YANLIŞ|||
|Satır Ayırıcı|Sicim|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **OoxmlSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|HücreAdınıDışa Aktar|Boolean|doğru| YANLIŞ|||
|GüncellemeYakınlaştırma|Boolean|doğru| YANLIŞ|||
|Zip64'ü Etkinleştir|Boolean|doğru| YANLIŞ|||
|GömülüOoxmlAsOleObject|Boolean|doğru| YANLIŞ|||
|Sıkıştırma Türü|Sicim|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **PclSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|yazıtipiTamAdı|Sicim|doğru| YANLIŞ|||
|fontPclAdı|Sicim|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **PdfSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|BelgeBaşlığını Göster|Boolean|doğru| YANLIŞ|||
|BelgeYapısınıDışa Aktar|Boolean|doğru| YANLIŞ|||
|EmfRenderAyarları|Sicim|doğru| YANLIŞ|||
|ÖzelÖzelliklerDışa Aktarma|Sicim|doğru| YANLIŞ|||
|Optimizasyon Türü|Sicim|doğru| YANLIŞ|||
|Yapımcı|Sicim|doğru| YANLIŞ|||
|PDFSıkıştırma|Sicim|doğru| YANLIŞ|||
|Font Kodlaması|Sicim|doğru| YANLIŞ|||
|Filigran|Sınıf|doğru| YANLIŞ|||
|Formülü Hesapla|Boolean|doğru| YANLIŞ|||
|YazıtipiUyumluluğunuKontrol Et|Boolean|doğru| YANLIŞ|||
|Uyumluluk|Sicim|doğru| YANLIŞ|||
|VarsayılanYazı Tipi|Sicim|doğru| YANLIŞ|||
|SayfaBaşınaBirSayfa|Boolean|doğru| YANLIŞ|||
|YazdırmaSayfaTürü|Sicim|doğru| YANLIŞ|||
|GüvenlikSeçenekleri|Sınıf|doğru| YANLIŞ|||
|istenenPPI|Tam sayı|doğru| YANLIŞ|||
|jpegKalitesi|Tam sayı|doğru| YANLIŞ|||
|Resim Türü|Sicim|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **PptxSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Gizli Satırları Yoksay|Boolean|doğru| YANLIŞ|||
|Satır Türü İçin FontBoyutunuAyarla|Sicim|doğru| YANLIŞ|||
|Dışa AktarımGörünümTürü|Sicim|doğru| YANLIŞ|||
|VarsayılanYazı Tipi|Sicim|doğru| YANLIŞ|||
|ÇalışmaKitabınıDenetleVarsayılanYazı Tipi|Boolean|doğru| YANLIŞ|||
|YazıtipiUyumluluğunuKontrol Et|Boolean|doğru| YANLIŞ|||
|IsFontSubstitutionCharGranularity|Boolean|doğru| YANLIŞ|||
|SayfaBaşınaBirSayfa|Boolean|doğru| YANLIŞ|||
|AllColumnsInOnePagePerSheet|Boolean|doğru| YANLIŞ|||
|Hatayı Yoksay|Boolean|doğru| YANLIŞ|||
|ÇıktıBoşSayfaHiçbirŞeyYazdırılmadığında|Boolean|doğru| YANLIŞ|||
|SayfaIndeksi|Tam sayı|doğru| YANLIŞ|||
|Sayfa Sayısı|Tam sayı|doğru| YANLIŞ|||
|YazdırmaSayfaTürü|Sicim|doğru| YANLIŞ|||
|Kılavuz Çizgi Türü|Sicim|doğru| YANLIŞ|||
|MetinÇapraz Tip|Sicim|doğru| YANLIŞ|||
|VarsayılanDüzenleDil|Sicim|doğru| YANLIŞ|||
|EmfRenderAyarları|Sicim|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **SqlScriptSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|TabloVarsaDenetle|Boolean|doğru| YANLIŞ|||
|SütunTürüHaritası|Sicim|doğru| YANLIŞ|||
|Sütun TürüİçinTümVerileriKontrolEt|Boolean|doğru| YANLIŞ|||
|Satırlar Arasına Boş Satır Ekle|Boolean|doğru| YANLIŞ|||
|Ayırıcı|Sicim|doğru| YANLIŞ|||
|Operatör Türü|Sicim|doğru| YANLIŞ|||
|BirincilAnahtar|Tam sayı|doğru| YANLIŞ|||
|Tablo Oluştur|Boolean|doğru| YANLIŞ|||
|KimlikAdı|Sicim|doğru| YANLIŞ|||
|BaşlangıçKimliği|Tam sayı|doğru| YANLIŞ|||
|TabloAdı|Sicim|doğru| YANLIŞ|||
|Dışa AktarDize Olarak|Boolean|doğru| YANLIŞ|||
|İhracatAlanı|Sınıf|doğru| YANLIŞ|||
|BaşlıkSatırı Var|Boolean|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **SvgSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Sayfa Dizini|Tam sayı|doğru| YANLIŞ|||
|GrafikGörüntüTürü|Sicim|doğru| YANLIŞ|||
|GömülüResimAdıSvg'de|Sicim|doğru| YANLIŞ|||
|Yatay Çözünürlük|Tam sayı|doğru| YANLIŞ|||
|GörüntüBiçimi|Sicim|doğru| YANLIŞ|||
|HücreOtomatikUyumlu mu|Boolean|doğru| YANLIŞ|||
|SayfaBaşınaBirSayfa|Boolean|doğru| YANLIŞ|||
|SadeceAlan|Boolean|doğru| YANLIŞ|||
|YazdırmaSayfası|Sicim|doğru| YANLIŞ|||
|PrintWithStatusDialog|Boolean|doğru| YANLIŞ|||
|Kalite|Tam sayı|doğru| YANLIŞ|||
|TiffSıkıştırma|Sicim|doğru| YANLIŞ|||
|Dikey Çözünürlük|Tam sayı|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **TxtSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Alıntı Türü|Sicim|doğru| YANLIŞ|||
|Ayırıcı|Sicim|doğru| YANLIŞ|||
|AyırıcıDize|Sicim|doğru| YANLIŞ|||
|Her zamanAlıntılandı|Boolean|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **XlsSaveOptions&XlsbSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Eşleşen Renk|Boolean|doğru| YANLIŞ|||
|WpsUyumluluğu|Boolean|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **XmlSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Sayfa Endeksleri|Sıralamak|doğru| YANLIŞ|||
|İhracatAlanı|Sınıf|doğru| YANLIŞ|||
|BaşlıkSatırı Var|Boolean|doğru| YANLIŞ|||
|XmlHaritaAdı|Sicim|doğru| YANLIŞ|||
|SayfaAdıÖğeAdıOlarak|Boolean|doğru| YANLIŞ|||
|VeriÖznitelikOlarak|Boolean|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **XpsSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|VarsayılanYazı Tipi|Sicim|doğru| YANLIŞ|||
|ÇalışmaKitabınıDenetleVarsayılanYazı Tipi|Boolean|doğru| YANLIŞ|||
|YazıtipiUyumluluğunuKontrol Et|Boolean|doğru| YANLIŞ|||
|IsFontSubstitutionCharGranularity|Boolean|doğru| YANLIŞ|||
|SayfaBaşınaBirSayfa|Boolean|doğru| YANLIŞ|||
|AllColumnsInOnePagePerSheet|Boolean|doğru| YANLIŞ|||
|Hatayı Yoksay|Boolean|doğru| YANLIŞ|||
|ÇıktıBoşSayfaHiçbirŞeyYazdırılmadığında|Boolean|doğru| YANLIŞ|||
|SayfaIndeksi|Tam sayı|doğru| YANLIŞ|||
|Sayfa Sayısı|Tam sayı|doğru| YANLIŞ|||
|YazdırmaSayfaTürü|Sicim|doğru| YANLIŞ|||
|Kılavuz Çizgi Türü|Sicim|doğru| YANLIŞ|||
|MetinÇapraz Tip|Sicim|doğru| YANLIŞ|||
|VarsayılanDüzenleDil|Sicim|doğru| YANLIŞ|||
|EmfRenderAyarları|Sicim|doğru| YANLIŞ|||
|BirleştirmeAlanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|KaydetBiçimlendir|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|Temiz Veri|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|GrafikÖnbelleğiniYenile|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|ExcelKısıtlamasınıKontrol Et|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||
