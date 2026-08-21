---
title: "Çalışma Kitabı Seçeneklerini Dönüştür"
second_title: "Belge"
linktitle: "Çalışma Kitabı Seçeneklerini Dönüştür"
type: docs
url: /tr/convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, Excel dönüştürme, PDF, CSV, API"
description: "Çalışma Kitabı Seçeneklerini Dönüştür – Aspose.Cells Cloud API ile Excel çalışma kitabını PDF, CSV, HTML ve daha fazla forma dönüştürme ayarlarını yapın."
weight: 79
ArticleTitle: "Çalışma Kitabı Seçeneklerini Dönüştür – Aspose.Cells Cloud API"
---

# ConvertWorkbookOptions Özellikleri

**API sürümü:** 23.12 (2024‑03)

`ConvertWorkbookOptions`, Aspose.Cells Cloud dönüştürme API'sinin bir Excel çalışma kitabını başka bir forma (PDF, CSV, HTML vb.) dönüştürme yöntemini belirlemek için kullandığı istek modelidir. Kaynak dosya bilgilerini, hedef formatı, sayfa ayarı ayarlarını ve forma özel kaydetme seçeneklerini birleştirir.

| Adı                                 | Tür         | Açıklama                                                                                                    | Notlar |
| ----------------------------------- | ----------- | ----------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Nesne**   | Veri dosyası kaynağı: `CloudFileSystem`, `RequestFiles` veya `HttpUri`.                                      |       |
| **[FileInfo](/cells/file-info/)**   | **Nesne**   | Dosya adını, boyutunu ve base64 ile kodlanmış içeriği açıklar.                                                |       |
| **[PageSetup](/cells/page-setup/)** | **Nesne**   | Kenar boşlukları, yön ve ölçekleme gibi sayfa ayarı özellikleri.                                             |       |
| **SaveOptions**                     | **Nesne**   | Format-özel kaydetme seçenekleri nesneleri için bir kapsayıcıdır (örn. `PdfSaveOptions`, `HtmlSaveOptions`). |       |
| **ConvertFormat**                   | **string**  | Hedef dosya formatı (örn. **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF**, vb.).                              |       |
| **CheckExcelRestriction**           | **boolean** | Excel’e özgü kısıtlamaları (maksimum satır, sütun, sayfa adı uzunluğu vb.) uygulayıp uygulanmayacağını alır veya ayarlar. |       |

**Önkoşullar**

- Aspose.Cells Cloud için geçerli bir OAuth 2.0 erişim belirteci edinin.  
- Kaynak dosyanın desteklenen `DataSource` türlerinden biri aracılığıyla erişilebilir olduğundan emin olun.

**Hızlı örnek**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Örnek.xlsx",
      "FileContent": "<base64‑ile‑kodlanmış‑içerik>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Örnek.pdf
```

**API isteği ayrıntıları**

Dönüştürme işlemi şu uç noktaya bir **POST** isteği ile gerçekleştirilir:

```
https://api.aspose.cloud/v3.0/cells/convert
```

Gerekli başlıklar:

| Başlık                | Değer                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

İstek gövdesi, `ConvertWorkbookOptions`’ın JSON temsili olmalıdır (yukarıdaki örneğe bakın). Tüm özellikler, seçilen `ConvertFormat` tarafından gerektirilmedikçe isteğe bağlıdır.

**API yanıtı**

Başarılı bir dönüştürme, dönüştürülen dosyayı yanıt gövdesinde akış olarak döndüren **HTTP 200 OK** (veya eşzamanlı işlem için **202 Accepted**) durum kodu döndürür. Yanıt akışla aktarıldığında, `Content-Disposition` başlığı önerilen dosya adını içerir.

Asenkron istek için JSON yanıtı örneği:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**Durum kodları**

| Kod | Anlam                                    |
|------|------------------------------------------|
| 200  | Dönüştürme tamamlandı; dosya döndürüldü.     |
| 202  | Dönüştürme kabul edildi; sonuç daha sonra kullanılabilir. |
| 400  | Hatalı istek – eksik veya geçersiz parametreler. |
| 401  | Yetkisiz – geçersiz veya eksik belirteç. |
| 403  | Yasak – yetersiz izinler.   |
| 500  | İç sunucu hatası.                   |

**Notlar / Sınırlamalar**

- `CheckExcelRestriction` bayrağı, maksimum satır (1.048.576) ve sütun (16.384) sayısını içeren Excel kısıtlamalarını uygular.  
- Tüm hedef formatlar, her `SaveOptions` özelliğini desteklemez; desteklenmeyen seçenekler yoksayılır.  
- Veri kaynağı olarak `HttpUri` kullanıldığında, URL kimlik doğrulama gerektirmeyen herkese açık olarak erişilebilir olmalıdır.  
- API yöntemi ve uç nokta bilgileri, geliştirici netliğini artırmak ve entegrasyon hatalarını azaltmak için eklenmiştir.  

## FileSource Özellikleri

| Özellik Adı    | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                                                |
| -------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------------------- |
| FileSourceType | String        | true     | false    |               | Kaynak türünü belirtir (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath       | String        | true     | false    |               | Dosya yolu konumu.                                                       |

## DbfSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ExportAsString            | Boolean       | true     | false    |               | **true** ise, sayısal değerleri dizge olarak dışa aktarır.  |
| SaveFormat                | String        | true     | false    |               | DBF dosyaları için format tanımlayıcısı.               |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.            |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.         |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.            |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.               |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.   |

## DifSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SaveFormat                | String        | true     | false    |               | DIF dosyaları için format tanımlayıcısı.               |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.            |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.         |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.            |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.               |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.   |

## DocxSaveOptions Özellikleri

| Özellik Adı                     | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | Kaynak yazı tipi kullanılamadığında kullanılan yazı tipi.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Çalışma kitabının varsayılan yazı tipinin uygulanıp uygulanmadığını denetler.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Hedef format için yazı tipi uyumluluğunu doğrular.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Karakter düzeyinde yazı tipi değiştirme kontrolünü sağlar.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Her sayfayı ayrı bir sayfaya zorlar.               |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Bir sayfanın tüm sütunlarını tek bir sayfaya sığdırır.            |
| IgnoreError                       | Boolean       | true     | false    |               | Dönüştürme sırasında kritik olmayan hataları yoksayar.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | İşlenecek bir şey yoksa boş bir sayfa oluşturur. |
| PageIndex                         | Integer       | true     | false    |               | Dışa aktarılacak ilk sayfanın dizini.                    |
| PageCount                         | Integer       | true     | false    |               | Dışa aktarılacak sayfa sayısı.                            |
| PrintingPageType                  | String        | true     | false    |               | Yazdırma için sayfa türünü belirtir.                 |
| GridlineType                      | String        | true     | false    |               | Izgara çizgilerinin nasıl işlendiğini belirler.                |
| TextCrossType                     | String        | true     | false    |               | Metin işleme için çapraz türü tanımlar.            |
| DefaultEditLanguage               | String        | true     | false    |               | Metni düzenlemek için varsayılan dil.                    |
| EmfRenderSetting                  | String        | true     | false    |               | EMF işleme ayarları.                           |
| MergeAreas                        | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.       |
| SaveFormat                        | String        | true     | false    |               | DOCX dosyaları için format tanımlayıcısı.                 |
| CachedFileFolder                  | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.               |
| ClearData                         | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.           |
| RefreshChartCache                 | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.           |
| SortNames                         | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                   |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.    |
| EncryptDocumentProperties          | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.      |

## HtmlSaveOptions Özellikleri

| Özellik Adı                   | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                          |
| ------------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean       | true     | false    |               | HTML çıktısına sayfa başlıklarını ekler.            |
| ExportPageFooters               | Boolean       | true     | false    |               | HTML çıktısına sayfa altbilgilerini ekler.            |
| ExportRowColumnHeadings         | Boolean       | true     | false    |               | Satır ve sütun başlıklarını dışa aktarır.                     |
| ShowAllSheets                   | Boolean       | true     | false    |               | Tüm çalışma sayfalarını tek bir HTML dosyasında gösterir.          |
| ImageOptions                    | Sınıf         | true     | false    |               | Görüntü işleme kontrol eden ayarlar.               |
| SaveAsSingleFile                | Boolean       | true     | false    |               | Tüm çalışma kitabını tek bir HTML dosyası olarak kaydeder.          |
| ExportHiddenWorksheet           | Boolean       | true     | false    |               | Gizli çalışma sayfalarını dışa aktarmaya ekler.            |
| ExportGridLines                 | Boolean       | true     | false    |               | HTML çıktısında ızgara çizgilerini işler.               |
| PresentationPreference          | Boolean       | true     | false    |               | HTML’yi sunum modu için optimize eder.                |
| CellCssPrefix                   | String        | true     | false    |               | Hücreler için oluşturulan CSS sınıf adlarına eklenen önek. |
| TableCssId                      | String        | true     | false    |               | Oluşturulan HTML tablosu için kimlik özniteliği.           |
| IsFullPathLink                  | Boolean       | true     | false    |               | Kaynaklar için tam yol bağlantıları oluşturur.        |
| ExportWorksheetCSSSeparately    | Boolean       | true     | false    |               | Her sayfanın CSS’ini ayrı bir dosyaya yerleştirir.      |
| ExportSimilarBorderStyle        | Boolean       | true     | false    |               | Benzer kenarlık stillerini birleştirerek CSS boyutunu küçültür.     |
| MergeEmptyTdForcely             | Boolean       | true     | false    |               | Boş `<td>` elementlerini birleştirmeye zorlar.             |
| ExportCellCoordinate            | Boolean       | true     | false    |               | HTML’e hücre koordinatlarını (örn. A1) ekler.    |
| ExportExtraHeadings             | Boolean       | true     | false    |               | Gerektiğinde ek başlık satırları/sütunları ekler.       |
| ExportHeadings                  | Boolean       | true     | false    |               | Satır ve sütun başlıklarını dışa aktarır.                     |
| ExportFormula                   | Boolean       | true     | false    |               | Hesaplanan değerler yerine formülleri gösterir.         |
| AddTooltipText                  | Boolean       | true     | false    |               | Hücre yorumları ile araç ipuçları ekler.                   |
| ExportBogusRowData              | Boolean       | true     | false    |               | Boş veriler için yer tutucu satırları ekler.            |
| ExcludeUnusedStyles             | Boolean       | true     | false    |               | Kullanılmayan CSS stillerini kaldırır.                |
| ExportDocumentProperties        | Boolean       | true     | false    |               | Belge düzeyi özelliklerini HTML meta etiketlerine yazar.  |
| ExportWorksheetProperties       | Boolean       | true     | false    |               | Çalışma sayfası düzeyi özelliklerini HTML’e yazar.           |
| ExportWorkbookProperties        | Boolean       | true     | false    |               | Çalışma kitabı düzeyi özelliklerini HTML’e yazar.            |
| ExportFrameScriptsAndProperties | Boolean       | true     | false    |               | Çerçeveler için betikleri ve özellikleri ekler.          |
| AttachedFilesDirectory          | String        | true     | false    |               | Ekli dosyalar için dizin yolu.                   |
| AttachedFilesUrlPrefix          | String        | true     | false    |               | Ekli dosyalar için URL öneki.                       |
| Encoding                        | String        | true     | false    |               | HTML dosyası için karakter kodlaması.                |
| ExportActiveWorksheetOnly       | Boolean       | true     | false    |               | Yalnızca etkin çalışma sayfasını dışa aktarır.                   |
| ExportChartImageFormat          | String        | true     | false    |               | Gömülü grafikler için kullanılan görüntü formatı.               |
| ExportImagesAsBase64            | Boolean       | true     | false    |               | Görüntüleri Base64 dizgeleri olarak kodlar.                    |
| HiddenColDisplayType            | String        | true     | false    |               | Gizli sütunların nasıl gösterileceği.                    |
| HiddenRowDisplayType            | String        | true     | false    |               | Gizli satırların nasıl gösterileceği.                       |
| HtmlCrossStringType             | String        | true     | false    |               | Çapraz dizge verilerinin nasıl işleneceğini belirler.        |
| IsExpImageToTempDir             | Boolean       | true     | false    |               | Görüntüleri geçici bir dizine dışa aktarır.             |
| PageTitle                       | String        | true     | false    |               | Oluşturulan HTML sayfası için başlık.              |
| ParseHtmlTagInCell              | Boolean       | true     | false    |               | Hücre değerlerindeki HTML etiketlerini ayrıştırır.             |
| CellNameAttribute               | String        | true     | false    |               | Hücre referansını tutan öznitelik adı.        |
| SaveFormat                      | String        | true     | false    |               | HTML dosyaları için format tanımlayıcısı.                |
| CachedFileFolder                | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.              |
| ClearData                       | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                  |
| CreateDirectory                 | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.   |
| EnableHttpCompression           | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.           |
| RefreshChartCache               | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.           |
| SortNames                       | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                   |
| ValidateMergedAreas             | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.              |
| MergeAreas                      | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                 |
| SortExternalNames               | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                     |
| CheckExcelRestriction           | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.    |
| UpdateSmartArt                  | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.      |
| EncryptDocumentProperties       | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.     |

## ImageSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ChartImageType            | String        | true     | false    |               | Grafik işleme için kullanılan görüntü formatı.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | SVG çıktısında gömülü görüntülere atanan ad.    |
| HorizontalResolution      | Integer       | true     | false    |               | Dışa aktarılan görüntünün yatay DPI’si.              |
| ImageFormat               | String        | true     | false    |               | Hedef görüntü formatı (PNG, JPG, vb.).              |
| IsCellAutoFit             | Boolean       | true     | false    |               | Hücre içeriğini görüntü boyutuna otomatik olarak sığdırır.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | Her çalışma sayfasını ayrı bir sayfada işler.         |
| OnlyArea                  | Boolean       | true     | false    |               | Yalnızca çalışma sayfasının tanımlı alanını dışa aktarır.    |
| PrintingPage              | String        | true     | false    |               | Yazdırma için kullanılan sayfa düzeni.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | Yazdırma sırasında durum iletişim kutusu gösterir.             |
| Quality                   | Integer       | true     | false    |               | JPEG görüntüleri için sıkıştırma kalitesi (0‑100).       |
| TiffCompression           | String        | true     | false    |               | TIFF görüntüleri için sıkıştırma türü.                  |
| VerticalResolution        | Integer       | true     | false    |               | Dışa aktarılan görüntünün dikey DPI’si.                |
| SaveFormat                | String        | true     | false    |               | Görüntü dosyaları için format tanımlayıcısı.             |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.            |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.         |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.            |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.               |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.   |

## JsonSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| ExportArea                | Sınıf         | true     | false    |               | Dışa aktarılacak çalışma sayfası alanını tanımlar.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | İlk satırın sütun başlıklarını içerip içermediğini belirtir. |
| ExportAsString            | Boolean       | true     | false    |               | Tüm değerleri dizge olarak dışa aktarır.                           |
| Indent                    | String        | true     | false    |               | Girinti için kullanılan dizge (örn. iki boşluk).          |
| SaveFormat                | String        | true     | false    |               | JSON dosyaları için format tanımlayıcısı.                    |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.                  |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                      |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.               |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.                  |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.         |

## MarkdownSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                                  |
| ------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------ |
| Encoding                  | String        | true     | false    |               | Markdown dosyası için karakter kodlaması.                    |
| FormatStrategy            | String        | true     | false    |               | Markdown formatlama için kullanılan strateji (örn. GitHub, CommonMark). |
| LineSeparator             | String        | true     | false    |               | Kullanılacak satır sonu karakteri(leri).                              |
| SaveFormat                | String        | true     | false    |               | Markdown dosyaları için format tanımlayıcısı.                    |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.                      |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                          |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.           |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.                   |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.                   |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                           |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.                      |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                         |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                             |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.            |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.              |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.             |

## OoxmlSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean       | true     | false    |               | Dışa aktarılan dosyaya hücre adlarını ekler.            |
| UpdateZoom                | Boolean       | true     | false    |               | Çıktı belgesinde yakınlaştırma düzeyini günceller.       |
| EnableZip64               | Boolean       | true     | false    |               | Büyük dosyalar için ZIP64 uzantılarını etkinleştirir.            |
| EmbedOoxmlAsOleObject     | Boolean       | true     | false    |               | OOXML’yi OLE nesnesi olarak gömer.                       |
| CompressionType           | String        | true     | false    |               | Uygulanan sıkıştırma türü (örn. Normal, Maximum). |
| SaveFormat                | String        | true     | false    |               | OOXML dosyaları için format tanımlayıcısı.               |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.              |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                  |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.           |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.           |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.              |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                 |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.     |

## PclSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| fontFullName              | String        | true     | false    |               | Kullanılacak tam yazı tipi adı.                      |
| fontPclName               | String        | true     | false    |               | PCL’e özgü yazı tipi adı.                            |
| SaveFormat                | String        | true     | false    |               | PCL dosyaları için format tanımlayıcısı.               |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.            |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.         |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.            |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.               |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.   |

## PDFSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean       | true     | false    |               | Belge başlığını PDF başlığı olarak kullanır.            |
| ExportDocumentStructure   | Boolean       | true     | false    |               | Belgenin mantıksal yapısını korur.     |
| EmfRenderSetting          | String        | true     | false    |               | EMF görüntülerinin işlenmesi için ayarlar.                   |
| CustomPropertiesExport    | String        | true     | false    |               | Özel belge özelliklerinin dışa aktarımını kontrol eder.       |
| OptimizationType          | String        | true     | false    |               | PDF optimizasyon türü (örn. Size, Speed).        |
| Producer                  | String        | true     | false    |               | PDF üretici uygulamasının adı.                |
| PDFCompression            | String        | true     | false    |               | PDF akışları için sıkıştırma algoritması.               |
| FontEncoding              | String        | true     | false    |               | Gömülü yazı tipleri için kodlama.                    |
| Watermark                 | Sınıf         | true     | false    |               | PDF’e uygulanan su işareti ayarları.               |
| CalculateFormula          | Boolean       | true     | false    |               | Dışa aktarmadan önce formülleri hesaplar.                   |
| CheckFontCompatibility    | Boolean       | true     | false    |               | PDF işleme için yazı tipi uyumluluğunu doğrular.      |
| Compliance                | String        | true     | false    |               | PDF/A veya PDF/X uyumluluk düzeyi.                     |
| DefaultFont               | String        | true     | false    |               | Kaynak yazı tipi kullanılamadığında kullanılan yazı tipi.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | Her çalışma sayfasını ayrı bir PDF sayfasına yerleştirir.        |
| PrintingPageType          | String        | true     | false    |               | Yazdırma için sayfa türünü belirtir.                |
| SecurityOptions           | Sınıf         | true     | false    |               | Şifreler ve izinler gibi güvenlik ayarları. |
| desiredPPI                | Integer       | true     | false    |               | İstenen piksel-birim-inch çözünürlüğü.                  |
| jpegQuality               | Integer       | true     | false    |               | JPEG görüntü kalitesi (0‑100).                          |
| ImageType                 | String        | true     | false    |               | Rasterleştirme için kullanılan görüntü türü.                   |
| SaveFormat                | String        | true     | false    |               | PDF dosyaları için format tanımlayıcısı.                 |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.              |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                  |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.           |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.           |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.              |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                 |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.     |

## PptxSaveOptions Özellikleri

| Özellik Adı                     | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                            |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------ |
| IgnoreHiddenRows                  | Boolean       | true     | false    |               | Dışa aktarım sırasında gizli satırları atlar.                       |
| AdjustFontSizeForRowType          | String        | true     | false    |               | Satır türüne göre yazı tipi boyutu ayarlamayı kontrol eder.       |
| ExportViewType                    | String        | true     | false    |               | Hangi görünümün (slayt, notlar) dışa aktarılacağını belirler.        |
| DefaultFont                       | String        | true     | false    |               | Kaynak yazı tipi kullanılamadığında kullanılan yazı tipi.           |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Çalışma kitabının varsayılan yazı tipinin uygulanıp uygulanmadığını denetler.   |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Hedef format için yazı tipi uyumluluğunu doğrular.    |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Karakter düzeyinde yazı tipi değiştirme kontrolünü sağlar.            |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Her çalışma sayfasını ayrı bir slayda yerleştirir.             |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Bir sayfanın tüm sütunlarını tek bir slayda sığdırır.            |
| IgnoreError                       | Boolean       | true     | false    |               | Dönüştürme sırasında kritik olmayan hataları yoksayar.         |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | İşlenecek bir şey yoksa boş bir slayt oluşturur. |
| PageIndex                         | Integer       | true     | false    |               | Dışa aktarılacak ilk slaytın dizini.                    |
| PageCount                         | Integer       | true     | false    |               | Dışa aktarılacak slayt sayısı.                            |
| PrintingPageType                  | String        | true     | false    |               | Yazdırma için sayfa türünü belirtir.                  |
| GridlineType                      | String        | true     | false    |               | Izgara çizgilerinin nasıl işlendiğini belirler.                 |
| TextCrossType                     | String        | true     | false    |               | Metin işleme için çapraz türü tanımlar.             |
| DefaultEditLanguage               | String        | true     | false    |               | Metni düzenlemek için varsayılan dil.                     |
| EmfRenderSetting                  | String        | true     | false    |               | EMF işleme ayarları.                            |
| MergeAreas                        | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                   |
| SortExternalNames                 | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                       |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.        |
| SaveFormat                        | String        | true     | false    |               | PPTX dosyaları için format tanımlayıcısı.                  |
| CachedFileFolder                  | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.                |
| ClearData                         | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                    |
| CreateDirectory                   | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.     |
| EnableHttpCompression             | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.             |
| RefreshChartCache                 | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.             |
| SortNames                         | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                     |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.                |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.      |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.       |

## SqlScriptSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| CheckIfTableExists        | Boolean       | true     | false    |               | Hedef tablonun zaten var olup olmadığını denetler.          |
| ColumnTypeMap             | String        | true     | false    |               | Sütun adlarının SQL veri türlerine eşlenmesi.               |
| CheckAllDataForColumnType | Boolean       | true     | false    |               | Sütun türlerini tahmin etmek için tüm satırları tarar.                    |
| AddBlankLineBetweenRows   | Boolean       | true     | false    |               | Oluşturulan satırlar arasında boş satır ekler.             |
| Separator                 | String        | true     | false    |               | Sütunları ayırmak için kullanılan dizge (örn. virgül, sekme).      |
| OperatorType              | String        | true     | false    |               | Kullanılan SQL operatörü (INSERT, UPDATE, vb.).                |
| PrimaryKey                | Integer       | true     | false    |               | Birincil anahtar olarak çalışan sütun dizini.               |
| CreateTable               | Boolean       | true     | false    |               | CREATE TABLE ifadesi oluşturur.                      |
| IdName                    | String        | true     | false    |               | Tanımlayıcı sütunun adı.                           |
| StartId                   | Integer       | true     | false    |               | Otomatik artan kimlikler için başlangıç değeri.                 |
| TableName                 | String        | true     | false    |               | Hedef veritabanı tablosunun adı.                       |
| ExportAsString            | Boolean       | true     | false    |               | Tüm değerleri dizge olarak dışa aktarır.                           |
| ExportArea                | Sınıf         | true     | false    |               | Dışa aktarılacak çalışma sayfası alanını tanımlar.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | İlk satırın sütun başlıklarını içerip içermediğini belirtir. |
| SaveFormat                | String        | true     | false    |               | SQL betik dosyaları için format tanımlayıcısı.              |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.                  |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                      |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.               |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.                  |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.         |

## SvgSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SheetIndex                | Integer       | true     | false    |               | Dışa aktarılacak çalışma sayfasının dizini.                  |
| ChartImageType            | String        | true     | false    |               | Grafik işleme için kullanılan görüntü formatı.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | SVG çıktısında gömülü görüntülere atanan ad.    |
| HorizontalResolution      | Integer       | true     | false    |               | Dışa aktarılan SVG’nin yatay DPI’si.                |
| ImageFormat               | String        | true     | false    |               | Raster elementler için hedef görüntü formatı.           |
| IsCellAutoFit             | Boolean       | true     | false    |               | Hücre içeriğini SVG boyutuna otomatik olarak sığdırır.           |
| OnePagePerSheet           | Boolean       | true     | false    |               | Her çalışma sayfasını ayrı bir SVG sayfasında işler.     |
| OnlyArea                  | Boolean       | true     | false    |               | Yalnızca çalışma sayfasının tanımlı alanını dışa aktarır.    |
| PrintingPage              | String        | true     | false    |               | Yazdırma için kullanılan sayfa düzeni.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | Yazdırma sırasında durum iletişim kutusu gösterir.             |
| Quality                   | Integer       | true     | false    |               | Raster görüntüler için sıkıştırma kalitesi.             |
| TiffCompression           | String        | true     | false    |               | SVG’ye gömülü TIFF görüntüler için sıkıştırma türü.  |
| VerticalResolution        | Integer       | true     | false    |               | Dışa aktarılan SVG’nin dikey DPI’si.                  |
| SaveFormat                | String        | true     | false    |               | SVG dosyaları için format tanımlayıcısı.               |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.            |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.         |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.            |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.               |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.   |

## TxtSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                                             |
| ------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------------------------- |
| QuoteType                 | String        | true     | false    |               | Kullanılan alıntı türü (örn. çift, tek).                            |
| Separator                 | String        | true     | false    |               | Sütun ayırıcı karakteri (örn. virgül, sekme).                          |
| SeparatorString           | String        | true     | false    |               | Birden fazla karakter gerekiyorsa ayırıcı olarak kullanılan tam dizge. |
| AlwaysQuoted              | Boolean       | true     | false    |               | Tüm alanların alıntılanmasına zorlar.                                         |
| SaveFormat                | String        | true     | false    |               | TXT dosyaları için format tanımlayıcısı.                                    |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.                                 |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                                     |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.                      |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.                              |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.                              |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                                      |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.                                 |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                                    |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                                        |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.                       |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.                         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.                        |

## XlsSaveOptions & XlsbSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| MatchColor                | Boolean       | true     | false    |               | Dışa aktarım sırasında tam hücre renklerini korur.         |
| WpsCompatibility          | Boolean       | true     | false    |               | WPS Office ile uyumluluğu etkinleştirir.             |
| SaveFormat                | String        | true     | false    |               | XLS/XLSB dosyaları için format tanımlayıcısı.          |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.            |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                |
| CreateDirectory           | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.         |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.            |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.               |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.   |

## XmlSaveOptions Özellikleri

| Özellik Adı             | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| SheetIndexes              | Dizi         | true     | false    |               | Dışa aktarmaya dahil edilecek çalışma sayfası dizinlerinin listesi.      |
| ExportArea                | Sınıf         | true     | false    |               | Dışa aktarılacak çalışma sayfası alanını tanımlar.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | İlk satırın sütun başlıklarını içerip içermediğini belirtir. |
| XmlMapName                | String        | true     | false    |               | Çalışma sayfasına uygulanan XML haritasının adı.            |
| SheetNameAsElementName    | Boolean       | true     | false    |               | Çalışma sayfası adını XML öğe adı olarak kullanır.             |
| DataAsAttribute           | Boolean       | true     | false    |               | Hücre verilerini öğeler yerine XML öznitelikleri olarak dışa aktarır. |
| SaveFormat                | String        | true     | false    |               | XML dosyaları için format tanımlayıcısı.                     |
| CachedFileFolder          | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.                  |
| ClearData                 | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                      |
| CreateDirectory           | String        | true     | false    |               | Hedef klasör yoksa oluşturur.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.               |
| SortNames                 | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.                  |
| MergeAreas                | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.         |

## XpsSaveOptions Özellikleri

| Özellik Adı                     | Özellik Türü | Boş Olabilir | Salt Okunur | Varsayılan Değer | Açıklama                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | Kaynak yazı tipi kullanılamadığında kullanılan yazı tipi.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Çalışma kitabının varsayılan yazı tipinin uygulanıp uygulanmadığını denetler.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Hedef format için yazı tipi uyumluluğunu doğrular.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Karakter düzeyinde yazı tipi değiştirme kontrolünü sağlar.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Her çalışma sayfasını ayrı bir XPS sayfasına yerleştirir.         |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Bir sayfanın tüm sütunlarını tek bir sayfaya sığdırır.            |
| IgnoreError                       | Boolean       | true     | false    |               | Dönüştürme sırasında kritik olmayan hataları yoksayar.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | İşlenecek bir şey yoksa boş bir sayfa oluşturur. |
| PageIndex                         | Integer       | true     | false    |               | Dışa aktarılacak ilk sayfanın dizini.                    |
| PageCount                         | Integer       | true     | false    |               | Dışa aktarılacak sayfa sayısı.                            |
| PrintingPageType                  | String        | true     | false    |               | Yazdırma için sayfa türünü belirtir.                 |
| GridlineType                      | String        | true     | false    |               | Izgara çizgilerinin nasıl işlendiğini belirler.                |
| TextCrossType                     | String        | true     | false    |               | Metin işleme için çapraz türü tanımlar.            |
| DefaultEditLanguage               | String        | true     | false    |               | Metni düzenlemek için varsayılan dil.                    |
| EmfRenderSetting                  | String        | true     | false    |               | EMF işleme ayarları.                           |
| MergeAreas                        | Boolean       | true     | false    |               | Mümkün olduğunda bitişik hücreleri birleştirir.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | Harici adlandırılmış referansları sıralar.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArt nesnelerini en son sürüme günceller.       |
| SaveFormat                        | String        | true     | false    |               | XPS dosyaları için format tanımlayıcısı.                  |
| CachedFileFolder                  | String        | true     | false    |               | Geçici önbellek dosyaları için kullanılan klasör.               |
| ClearData                         | Boolean       | true     | false    |               | Kaydetmeden önce mevcut verileri temizler.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | Hedef klasör yoksa oluşturur.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | Yanıt için HTTP sıkıştırmasını etkinleştirir.            |
| RefreshChartCache                 | Boolean       | true     | false    |               | Kaydetmeden önce önbelleğe alınmış grafik verilerini yeniler.            |
| SortNames                         | Boolean       | true     | false    |               | Adlandırılmış aralıkları alfabetik olarak sıralar.                    |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Birleştirilmiş hücreleri tutarlılık için doğrular.               |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Dönüştürme sırasında Excel’e özgü sınırları uygular.     |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | Çıktı dosyasındaki belge özelliklerini şifreler.      |
---