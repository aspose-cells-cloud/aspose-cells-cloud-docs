---
---
title: "Çalışma Sayfası Sayfa Ayarları"
second_title: "Belge"
linktitle: "Sayfa ayarları"
type: docs
url: /page-setup/
keywords: "Aspose.Cells, pageSetup, çalışma sayfası, yazdırma ayarları, kenar boşlukları, yön, kağıt boyutu, başlık, altlık, ölçekleme"
description: "Aspose.Cells Cloud’ın PageSetup nesnesi ile Excel çalışma sayfası yazdırma düzenini nasıl yapılandıracağınızı öğrenin. Özellik listesi, varsayılan değerler, aralıklar ve C#, Java ve Python için kod örneklerini içerir."
weight: 20
ArticleTitle: "Çalışma Sayfası Sayfa Ayarları – Aspose.Cells Cloud ile Yazdırma Düzenini Yapılandırma"
---

# **PageSetup**

Excel yazdırma sayfa ayarları

## Genel Bakış

**PageSetup** nesnesi, kenar boşlukları, yön, ölçekleme, başlıklar, altlıklar ve diğer yazdırma ile ilgili ayarlar gibi Excel çalışma sayfasının yazdırma düzeni seçeneklerini tanımlar. Bu özelliklerin yapılandırılması, geliştiricilerin istenilen görünüme ve sayfalama uygun yazdırılabilir defterler oluşturmasını sağlar.

Aşağıda, Aspose.Cells Cloud SDK kullanılarak yaygın sayfa ayarı özelliklerinin nasıl ayarlanacağı gösterilen kısa bir C# örneği yer almaktadır:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API istemcisini başlatın (kimlik bilgilerinizle değiştirin)
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// PageSetup ayarlarını tanımlayın
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// Ayarları defterin ilk çalışma sayfasına uygulayın
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

Bu kod parçası, çalışma sayfasını yatay yöne (landscape) ayarlar, A4 kağıt boyutunu kullanır, içeriği ortalar ve %100 ölçeklendirme faktörünü uygular.

## Özellikler

| Özellik Adı           | Özellik Türü  |nullable| Okunur Olmayan | Varsayılan Değer | Açıklama                                                                     |
| --------------------- | ------------- | ------ | ------------- | -------------- | ---------------------------------------------------------------------------- |
| BlackAndWhite         | bool          | false  | false         | false          | Çalışma sayfasını siyah-beyaz modda yazdırır.                                |
| BottomMargin          | float         | true   | false         | 2.54 cm        | Alt kenar boşluğunun santimetre cinsinden boyutu.                            |
| CenterHorizontally    | bool          | false  | false         | false          | Yazdırırken sayfayı yatayda ortalama.                                        |
| CenterVertically      | bool          | false  | false         | false          | Yazdırırken sayfayı dikeyde ortalama.                                        |
| FirstPageNumber       | int           | true   | false         | 1              | Sayfa yazdırılırken kullanılan ilk sayfa numarası.                           |
| FitToPagesTall        | int           | false  | false         | 1              | Çalışma sayfasının ölçekleneceği sayfa yüksekliği (sayfa sayısı).           |
| FitToPagesWide        | int           | false  | false         | 1              | Çalışma sayfasının ölçekleneceği sayfa genişliği (sayfa sayısı).            |
| FooterMargin          | float         | true   | false         | 2.54 cm        | Sayfanın altı ile altlığın arasındaki mesafe, santimetre cinsinden.         |
| HeaderMargin          | float         | true   | false         | 2.54 cm        | Sayfanın üstü ile başlığın arasındaki mesafe, santimetre cinsinden.          |
| IsAutoFirstPageNumber | bool          | false  | false         | false          | İlk sayfa numarasını otomatik olarak atar.                                   |
| IsHFAlignMargins      | bool          | false  | false         | true           | true ise, başlık/altlık kenar boşlukları sayfa kenar boşluklarıyla hizalanır.|
| IsHFDiffFirst         | bool          | false  | false         | false          | İlk sayfadaki başlığın/altlığın diğer sayfalardan farklı olduğunu belirtir.  |
| IsHFDiffOddEven       | bool          | false  | false         | false          | Tek sayfalardaki başlığın/altlığın çift sayfalardan farklı olduğunu belirtir.|
| IsHFScaleWithDoc      | bool          | false  | false         | false          | Başlığı ve altlığı belgeyle birlikte ölçekler (Excel 2007+).                |
| IsPercentScale        | bool          | false  | false         | true           | false ise, `FitToPagesWide` ve `FitToPagesTall` ölçeklemeyi kontrol eder.   |
| LeftMargin            | float         | true   | false         | 2.54 cm        | Sol kenar boşluğunun santimetre cinsinden boyutu.                            |
| Order                 | string        | true   | false         | "DownThenOver" | Büyük bir çalışma sayfası yazdırılırken Excel’in sayfaları numaralandırma sırası. |
| Orientation           | string        | false  | false         | "Portrait"     | Sayfa yönü: **Landscape** (yatay) veya **Portrait** (dikey).                |
| PaperSize             | string        | true   | false         | "A4"           | Yazdırma için kullanılan kağıt boyutu.                                       |
| PrintArea             | string        | true   | false         | (yok)          | Yazdırılacak hücre aralığı (örneğin, `"A1:D20"`).                            |
| PrintComments         | string        | true   | false         | "NoComments"   | Sayfa ile birlikte yorumların nasıl yazdırılacağı.                           |
| PrintCopies           | int           | true   | false         | 1              | Yazdırılacak kopya sayısı.                                                   |
| PrintDraft            | bool          | false  | false         | false          | Çalışma sayfasını taslak modda yazdırır (grafikler olmadan).                 |
| PrintErrors           | string        | true   | false         | "Display"      | Gösterilecek yazdırma hatası türü.                                           |
| PrintGridlines        | bool          | false  | false         | false          | Hücre ızgarası çizgilerini yazdırır.                                         |
| PrintHeadings         | bool          | false  | false         | false          | Satır ve sütun başlıklarını yazdırır.                                        |
| PrintQuality          | int           | true   | false         | 600            | Yazdırma kalitesi ayarı (dots per inch - dpi).                               |
| PrintTitleColumns     | string        | true   | false         | (yok)          | Her yazdırılan sayfanın sol tarafında tekrar edilecek sütunlar.             |
| PrintTitleRows        | string        | true   | false         | (yok)          | Her yazdırılan sayfanın üst kısmında tekrar edilecek satırlar.              |
| RightMargin           | float         | true   | false         | 2.54 cm        | Sağ kenar boşluğunun santimetre cinsinden boyutu.                            |
| TopMargin             | float         | true   | false         | 2.54 cm        | Üst kenar boşluğunun santimetre cinsinden boyutu.                            |
| Zoom                  | int           | false  | false         | 100            | Yüzde cinsinden ölçeklendirme faktörü (%10 – %400).                          |
| Header                | object        | true   | false         | (yok)          | Sayfa başlığı yapılandırması.                                                |
| Footer                | object        | true   | false         | (yok)          | Sayfa altlığı yapılandırması.                                                |

## İlgili Nesneler

- **Header** – Çalışma sayfası başlığını yapılandırır.  
- **Footer** – Çalışma sayfası altlığını yapılandırır.  
- **PrintOptions** – Sayfa kırılımları ve yazdırma alanı gibi ek yazdırma ile ilgili ayarlar.  
---