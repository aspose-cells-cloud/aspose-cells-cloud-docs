---
title: Çalışma Kitabını Dönüştür Seçeneği
second_title: Aspose.Cells Cloud Documen
linktitle: Çalışma Kitabını Dönüştür Seçeneği
type: docs
url: /tr/convert-workbook-options/
keywords: ConvertWorkbookOptions
description: Aspose.Cells Cloud REST API, Excel dosyalarını çeşitli biçimlerde destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur.
weight: 79
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Çalışma Kitabı Seçeneklerini Dönüştür
---
# ConvertWorkbookOptions Özellikleri

Adı | Türü | Açıklama | Notlar
------------ | ------------- | ------------- | -------------
**Veri Kaynağı** | **Nesne** | Veri dosyası kaynağı : CloudFileSystem ,RequestFiles , HttpUri. |
**[DosyaBilgisi](/hücreler/dosya-bilgisi/)** | **Nesne** | Dosya bilgisi açıklaması. Dosya adı, dosya boyutu ve dosya içeriği (base64 dizesi) dahildir. |
**[SayfaAyarları](/hücreler/sayfa-ayarları/)** | **Nesne** | Sayfa düzeni özellikleri. |
**Kaydetme Seçenekleri** | **Nesne** Kaydetme Seçenekleri: DbfSaveOptions, DifSaveOptions, DocxSaveOptions, HtmlSaveOptions, XlsSaveOptions, XlsxSaveOptions, XpsSaveOptions, PngSaveOptions, JpgSaveOptions, GifSaveOptions, EmfSaveOptions, BmpSaveOptions, MdSaveOptions, NumbersSaveOptions, WmfSaveOptions, SvgSaveOptions, TxtSaveOptions, TifSaveOptions, XlsbSaveOptions |
**DönüştürBiçimlendir** | **sicim** | Dosya biçimi: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, vb. |
**CheckExcelRestriction** | **Boolean** | Otomatik olarak sarılan metnin türünü alır ve ayarlar. |

## **fileSource Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|DosyaKaynakTürü|Sicim|doğru| YANLIŞ||Erişilebilen ve değiştirilebilen FileSourceType türündeki FileSourceType adlı bir özellik.(CloudFileSystem/RequestFiles/HttpUri)|
|DosyaYolu|Sicim|doğru| YANLIŞ||Dosya konum yolu.|

## **DbfSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|ExportAsString|Boolean|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **DifSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **DocxSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Varsayılan Yazı Tipi|Sicim|doğru| YANLIŞ|||
|CheckWorkbookDefaultFont|Boolean|doğru| YANLIŞ|||
|Yazı Tipi Uyumluluğunu Kontrol Et|Boolean|doğru| YANLIŞ|||
|IsFontSubstitutionCharGranularity|Boolean|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfa|Boolean|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfada Tüm Sütunlar|Boolean|doğru| YANLIŞ|||
|Hatayı Yoksay|Boolean|doğru| YANLIŞ|||
|YazdırılacakHiçbirŞeyOlmadığındaÇıktıBoşSayfa|Boolean|doğru| YANLIŞ|||
|Sayfa Dizini|Tam sayı|doğru| YANLIŞ|||
|Sayfa Sayısı|Tam sayı|doğru| YANLIŞ|||
|YazdırmaSayfaTürü|Sicim|doğru| YANLIŞ|||
|Kılavuz Çizgi Türü|Sicim|doğru| YANLIŞ|||
|MetinÇapraz Tip|Sicim|doğru| YANLIŞ|||
|VarsayılanDilDüzenle|Sicim|doğru| YANLIŞ|||
|EmfRenderAyarları|Sicim|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **HtmlSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|ExportPageHeaders|Boolean|doğru| YANLIŞ|||
|ExportPageFooters|Boolean|doğru| YANLIŞ|||
|ExportRowColumnHeadings|Boolean|doğru| YANLIŞ|||
|TümSayfalarıGöster|Boolean|doğru| YANLIŞ|||
|GörüntüSeçenekleri|Sınıf|doğru| YANLIŞ|||
|TekDosyaOlarakKaydet|Boolean|doğru| YANLIŞ|||
|GizliÇalışma Sayfasını Dışa Aktar|Boolean|doğru| YANLIŞ|||
|Izgara Çizgilerini Dışa Aktar|Boolean|doğru| YANLIŞ|||
|SunumTercihi|Boolean|doğru| YANLIŞ|||
|HücreCssÖneki|Sicim|doğru| YANLIŞ|||
|TableCssId|Sicim|doğru| YANLIŞ|||
|TamYolBağlantısı|Boolean|doğru| YANLIŞ|||
|ExportWorksheetCSSSeparately|Boolean|doğru| YANLIŞ|||
|BenzerSınırStili Dışa Aktar|Boolean|doğru| YANLIŞ|||
|BoşTdZorla Birleştir|Boolean|doğru| YANLIŞ|||
|Hücre Koordinatını Dışa Aktar|Boolean|doğru| YANLIŞ|||
|Ekstra Başlıkları Dışa Aktar|Boolean|doğru| YANLIŞ|||
|Başlıkları Dışa Aktar|Boolean|doğru| YANLIŞ|||
|İhracatFormülü|Boolean|doğru| YANLIŞ|||
|İpucu Metni Ekle|Boolean|doğru| YANLIŞ|||
|Sahte Satır Verilerini Dışa Aktar|Boolean|doğru| YANLIŞ|||
|Kullanılmayan Stilleri Hariç Tut|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Dışa Aktar|Boolean|doğru| YANLIŞ|||
|ExportWorksheetProperties|Boolean|doğru| YANLIŞ|||
|ExportWorkbookProperties|Boolean|doğru| YANLIŞ|||
|ExportFrameScriptsAndProperties|Boolean|doğru| YANLIŞ|||
|EkliDosyalarDizin|Sicim|doğru| YANLIŞ|||
|EkliDosyalarUrlÖneki|Sicim|doğru| YANLIŞ|||
|Kodlama|Sicim|doğru| YANLIŞ|||
|YalnızcaActiveWorksheet'iDışa Aktar|Boolean|doğru| YANLIŞ|||
|GrafikGörüntüBiçiminiDışaAktar|Sicim|doğru| YANLIŞ|||
|ExportImagesAsBase64|Boolean|doğru| YANLIŞ|||
|GizliSütunGörüntülemeTürü|Sicim|doğru| YANLIŞ|||
|GizliSatırGörüntülemeTürü|Sicim|doğru| YANLIŞ|||
|HtmlCrossStringType|Sicim|doğru| YANLIŞ|||
|IsExpImageToTempDir|Boolean|doğru| YANLIŞ|||
|Sayfa Başlığı|Sicim|doğru| YANLIŞ|||
|ParseHtmlTagInCell|Boolean|doğru| YANLIŞ|||
|HücreAdıÖzniteliği|Sicim|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **ImageSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|GrafikGörüntüTürü|Sicim|doğru| YANLIŞ|||
|GömülüResimAdıSvg'de|Sicim|doğru| YANLIŞ|||
|Yatay Çözünürlük|Tam sayı|doğru| YANLIŞ|||
|GörüntüBiçimi|Sicim|doğru| YANLIŞ|||
|IsCellAutoFit|Boolean|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfa|Boolean|doğru| YANLIŞ|||
|SadeceAlan|Boolean|doğru| YANLIŞ|||
|Yazdırma Sayfası|Sicim|doğru| YANLIŞ|||
|PrintWithStatusDialog|Boolean|doğru| YANLIŞ|||
|Kalite|Tam sayı|doğru| YANLIŞ|||
|Tiff Sıkıştırma|Sicim|doğru| YANLIŞ|||
|Dikey Çözünürlük|Tam sayı|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **JsonSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|İhracatAlanı|Sınıf|doğru| YANLIŞ|||
|BaşlıkSatırı Var|Boolean|doğru| YANLIŞ|||
|ExportAsString|Boolean|doğru| YANLIŞ|||
|Girinti|Sicim|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **MarkdownSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Kodlama|Sicim|doğru| YANLIŞ|||
|FormatStratejisi|Sicim|doğru| YANLIŞ|||
|Satır Ayırıcı|Sicim|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **OoxmlSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|HücreAdıDışaAktar|Boolean|doğru| YANLIŞ|||
|Yakınlaştırmayı Güncelle|Boolean|doğru| YANLIŞ|||
|Zip64'ü Etkinleştir|Boolean|doğru| YANLIŞ|||
|EmbedOoxmlAsOleObject|Boolean|doğru| YANLIŞ|||
|Sıkıştırma Türü|Sicim|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **PclSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|fontFullName|Sicim|doğru| YANLIŞ|||
|fontPclName|Sicim|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **PDFSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|DisplayDocTitle|Boolean|doğru| YANLIŞ|||
|ExportDocumentStructure|Boolean|doğru| YANLIŞ|||
|EmfRenderAyarları|Sicim|doğru| YANLIŞ|||
|ÖzelÖzelliklerDışa Aktarma|Sicim|doğru| YANLIŞ|||
|Optimizasyon Türü|Sicim|doğru| YANLIŞ|||
|Yapımcı|Sicim|doğru| YANLIŞ|||
|PDF Sıkıştırma|Sicim|doğru| YANLIŞ|||
|Font Kodlaması|Sicim|doğru| YANLIŞ|||
|Filigran|Sınıf|doğru| YANLIŞ|||
|Hesaplama Formülü|Boolean|doğru| YANLIŞ|||
|Yazı Tipi Uyumluluğunu Kontrol Et|Boolean|doğru| YANLIŞ|||
|Uyumluluk|Sicim|doğru| YANLIŞ|||
|Varsayılan Yazı Tipi|Sicim|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfa|Boolean|doğru| YANLIŞ|||
|YazdırmaSayfaTürü|Sicim|doğru| YANLIŞ|||
|Güvenlik Seçenekleri|Sınıf|doğru| YANLIŞ|||
|istenenÜFE|Tam sayı|doğru| YANLIŞ|||
|jpegKalitesi|Tam sayı|doğru| YANLIŞ|||
|Resim Türü|Sicim|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **PptxSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Gizli Satırları Yoksay|Boolean|doğru| YANLIŞ|||
|Satır Türü İçin Yazı Tipi Boyutunu Ayarla|Sicim|doğru| YANLIŞ|||
|Dışa AktarmaGörünümTürü|Sicim|doğru| YANLIŞ|||
|Varsayılan Yazı Tipi|Sicim|doğru| YANLIŞ|||
|CheckWorkbookDefaultFont|Boolean|doğru| YANLIŞ|||
|Yazı Tipi Uyumluluğunu Kontrol Et|Boolean|doğru| YANLIŞ|||
|IsFontSubstitutionCharGranularity|Boolean|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfa|Boolean|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfada Tüm Sütunlar|Boolean|doğru| YANLIŞ|||
|Hatayı Yoksay|Boolean|doğru| YANLIŞ|||
|YazdırılacakHiçbirŞeyOlmadığındaÇıktıBoşSayfa|Boolean|doğru| YANLIŞ|||
|Sayfa Dizini|Tam sayı|doğru| YANLIŞ|||
|Sayfa Sayısı|Tam sayı|doğru| YANLIŞ|||
|YazdırmaSayfaTürü|Sicim|doğru| YANLIŞ|||
|Kılavuz Çizgi Türü|Sicim|doğru| YANLIŞ|||
|MetinÇapraz Tip|Sicim|doğru| YANLIŞ|||
|VarsayılanDilDüzenle|Sicim|doğru| YANLIŞ|||
|EmfRenderAyarları|Sicim|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **SqlScriptSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|TabloVarsaKontrol Et|Boolean|doğru| YANLIŞ|||
|SütunTürüHaritası|Sicim|doğru| YANLIŞ|||
|Sütun TürüİçinTümVerileriKontrolEt|Boolean|doğru| YANLIŞ|||
|SatırlarArasıBoşSatırEkle|Boolean|doğru| YANLIŞ|||
|Ayırıcı|Sicim|doğru| YANLIŞ|||
|Operatör Türü|Sicim|doğru| YANLIŞ|||
|BirincilAnahtar|Tam sayı|doğru| YANLIŞ|||
|Tablo Oluştur|Boolean|doğru| YANLIŞ|||
|KimlikAdı|Sicim|doğru| YANLIŞ|||
|Başlangıç Kimliği|Tam sayı|doğru| YANLIŞ|||
|TabloAdı|Sicim|doğru| YANLIŞ|||
|ExportAsString|Boolean|doğru| YANLIŞ|||
|İhracatAlanı|Sınıf|doğru| YANLIŞ|||
|BaşlıkSatırı Var|Boolean|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **SvgSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Sayfa Dizini|Tam sayı|doğru| YANLIŞ|||
|GrafikGörüntüTürü|Sicim|doğru| YANLIŞ|||
|GömülüResimAdıSvg'de|Sicim|doğru| YANLIŞ|||
|Yatay Çözünürlük|Tam sayı|doğru| YANLIŞ|||
|GörüntüBiçimi|Sicim|doğru| YANLIŞ|||
|IsCellAutoFit|Boolean|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfa|Boolean|doğru| YANLIŞ|||
|SadeceAlan|Boolean|doğru| YANLIŞ|||
|Yazdırma Sayfası|Sicim|doğru| YANLIŞ|||
|PrintWithStatusDialog|Boolean|doğru| YANLIŞ|||
|Kalite|Tam sayı|doğru| YANLIŞ|||
|Tiff Sıkıştırma|Sicim|doğru| YANLIŞ|||
|Dikey Çözünürlük|Tam sayı|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **TxtSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Alıntı Türü|Sicim|doğru| YANLIŞ|||
|Ayırıcı|Sicim|doğru| YANLIŞ|||
|AyırıcıDize|Sicim|doğru| YANLIŞ|||
|Her Zaman Alıntılandı|Boolean|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **XlsSaveOptions&XlsbSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Renk Eşleştirme|Boolean|doğru| YANLIŞ|||
|WpsUyumluluğu|Boolean|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **XmlSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Sayfa Endeksleri|Sıralamak|doğru| YANLIŞ|||
|İhracatAlanı|Sınıf|doğru| YANLIŞ|||
|BaşlıkSatırı Var|Boolean|doğru| YANLIŞ|||
|XmlHaritaAdı|Sicim|doğru| YANLIŞ|||
|SayfaAdıÖğeAdıOlarak|Boolean|doğru| YANLIŞ|||
|VeriÖznitelikOlarak|Boolean|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||

## **XpsSaveOptions Özellikleri**

| Mülk Adı| Emlak Türü| Boş bırakılabilir| Salt Okunur| VarsayılanDeğer| Tanım|
|:- |:- |:- |:- |:- |:- |
|Varsayılan Yazı Tipi|Sicim|doğru| YANLIŞ|||
|CheckWorkbookDefaultFont|Boolean|doğru| YANLIŞ|||
|Yazı Tipi Uyumluluğunu Kontrol Et|Boolean|doğru| YANLIŞ|||
|IsFontSubstitutionCharGranularity|Boolean|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfa|Boolean|doğru| YANLIŞ|||
|Sayfa Başına Bir Sayfada Tüm Sütunlar|Boolean|doğru| YANLIŞ|||
|Hatayı Yoksay|Boolean|doğru| YANLIŞ|||
|YazdırılacakHiçbirŞeyOlmadığındaÇıktıBoşSayfa|Boolean|doğru| YANLIŞ|||
|Sayfa Dizini|Tam sayı|doğru| YANLIŞ|||
|Sayfa Sayısı|Tam sayı|doğru| YANLIŞ|||
|YazdırmaSayfaTürü|Sicim|doğru| YANLIŞ|||
|Kılavuz Çizgi Türü|Sicim|doğru| YANLIŞ|||
|MetinÇapraz Tip|Sicim|doğru| YANLIŞ|||
|VarsayılanDilDüzenle|Sicim|doğru| YANLIŞ|||
|EmfRenderAyarları|Sicim|doğru| YANLIŞ|||
|Birleştirme Alanları|Boolean|doğru| YANLIŞ|||
|SıralaHariciAdlar|Boolean|doğru| YANLIŞ|||
|AkıllıSanat'ı Güncelle|Boolean|doğru| YANLIŞ|||
|SaveFormat|Sicim|doğru| YANLIŞ|||
|Önbelleğe AlınmışDosyaKlasörü|Sicim|doğru| YANLIŞ|||
|ClearData|Boolean|doğru| YANLIŞ|||
|Dizin Oluştur|Boolean|doğru| YANLIŞ|||
|HTTP Sıkıştırmayı Etkinleştir|Boolean|doğru| YANLIŞ|||
|RefreshChartCache|Boolean|doğru| YANLIŞ|||
|SıralamaAdları|Boolean|doğru| YANLIŞ|||
|Birleştirilmiş Alanları Doğrula|Boolean|doğru| YANLIŞ|||
|CheckExcelRestriction|Boolean|doğru| YANLIŞ|||
|Belge Özelliklerini Şifrele|Boolean|doğru| YANLIŞ|||
