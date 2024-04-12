---
title: PdfKaydetme Seçeneği
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/pdfsaveoptions/
description: "Aspose.Cells Bulut modeli spesifikasyonu: PdfSaveOptions. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **pdfKaydetmeSeçenekleri**

 Pdf dosyasını kaydetme seçeneklerini temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| DisplayDocTitle| Boolean| Doğru| YANLIŞ|| Pencerenin başlık çubuğunun belge başlığını görüntüleyip görüntülemeyeceğini belirtir.|
| Dışa AktarmaBelge Yapısı| Boolean| Doğru| YANLIŞ|| Belge yapısının dışa aktarılıp aktarılmayacağını belirtir.|
| EmfRenderSetting| Sicim| Doğru| YANLIŞ|| Emf meta dosyasını işlemeye yönelik ayar.|
| ÖzelÖzelliklerDışa Aktarma| Sicim| Doğru| YANLIŞ|| CustomDocumentPropertyCollection'ın PDF dosyasına aktarılma biçimini belirtir.|
| Optimizasyon Türü| Sicim| Doğru| YANLIŞ|| PDF optimizasyon türünü alır ve ayarlar.|
| Üretici| Sicim| Doğru| YANLIŞ|| Oluşturulan pdf belgesinin üreticisini alır ve ayarlar.|
| PdfSıkıştırma| Sicim| Doğru| YANLIŞ||Sıkıştırma algoritmasını belirtin.|
| Yazı Tipi Kodlaması| Sicim| Doğru| YANLIŞ|| PDF olarak gömülü yazı tipi kodlamasını alır veya ayarlar.|
| Filigran| Sınıf:RenderingFiligran| Doğru| YANLIŞ|| Çıktıya filigran alır veya ayarlar.|
| HesaplaFormül| Boolean| Doğru| YANLIŞ|| Formüllerin pdf dosyasını kaydetmeden önce hesaplanıp hesaplanmayacağını belirtir. Varsayılan değer false'tur.|
| Yazı Tipi Uyumluluğunu Kontrol Edin| Boolean| Doğru| YANLIŞ|| Metindeki her karakter için yazı tipi uyumluluğunun kontrol edilip edilmeyeceğini belirtir. Varsayılan değer doğrudur. Bu özelliğin devre dışı bırakılması daha iyi performans sağlayabilir. Ancak varsayılan veya belirtilen metin/karakter yazı tipi bunu oluşturmak için kullanılamadığında, oluşturulan pdf'te okunamayan karakterler (blok gibi) oluşabilir. Böyle bir durumda, metni oluşturmak için alternatif yazı tipinin aranabilmesi ve kullanılabilmesi için kullanıcının bu özelliği true olarak tutması gerekir;|
| uyma| Sicim| Doğru| YANLIŞ|| Çalışma kitabı bu özellikteki PdfCompliance'a göre pdf'ye dönüştürülür.|
| Varsayılan yazı tipi| Sicim| Doğru| YANLIŞ||Excel'deki karakterler unicode olduğunda ve hücre stilinde doğru yazı tipiyle ayarlanmadığında, pdf, resimde blok olarak görünebilirler. Bu karakterleri göstermek için MingLiu veya MS Gotik gibi Varsayılan Yazı Tipini ayarlayın. Bu özellik ayarlanmazsa, Aspose.Cells bu unicode karakterleri göstermek için sistem varsayılan yazı tipini kullanır.|
| Sayfa Başına Bir Sayfa| Boolean| Doğru| YANLIŞ|| OnePagePerSheet true olursa, sonuçta bir sayfanın tüm içeriği yalnızca bir sayfaya yazdırılır. Pagesetup'ın kağıt boyutu geçersiz olacak ve diğer pagesetup ayarları geçerli olmaya devam edecektir.|
| YazdırmaSayfa Türü| Sicim| Doğru| YANLIŞ|| Hangi sayfaların yazdırılmayacağını belirtir.|
| Güvenlik seçenekleri| Sınıf:PdfSecurityOptions| Doğru| YANLIŞ|| Xls2pdf sonucunda güvenliğe ihtiyaç duyulduğunda bu seçeneği ayarlayın.|
| İstenilen ÜFE| Tamsayı| Doğru| YANLIŞ||Yeniden örnekleme görüntülerinin ve jpeg kalitesinin istenen ÜFE'sini (inç başına piksel) ve jpeg kalitesini ayarlayın Tüm görüntüler, belirtilen kalite ayarıyla JPEG'e dönüştürülecek ve belirtilen PPI'den (inç başına piksel) daha büyük görüntüler yeniden örneklenecektir. İnç başına istenen piksel. 220 yüksek kalite. 150 ekran kalitesi. 96 e-posta kalitesi.|
| jpegKalite| Tamsayı| Doğru| YANLIŞ|| Yeniden örnekleme görüntülerinin ve jpeg kalitesinin istenen ÜFE'sini (inç başına piksel) ve jpeg kalitesini ayarlayın Tüm görüntüler, belirtilen kalite ayarıyla JPEG'e dönüştürülecek ve belirtilen PPI'den (inç başına piksel) daha büyük görüntüler yeniden örneklenecektir. 0 - 100% JPEG kalitesi.|
| Resim türü| Sicim| Doğru| YANLIŞ|| Grafiği ve şekli dönüştürürken görüntü türünü temsil eder.|
| Formatı Kaydet| Sicim| Doğru| YANLIŞ|||
| Önbelleğe Alınmış DosyaKlasörü| Sicim| Doğru| YANLIŞ|||
| Net veriler| Boolean| Doğru| YANLIŞ|||
| Dizin Oluştur| Boolean| Doğru| YANLIŞ|||
| HTTPSıkıştırmayı Etkinleştir| Boolean| Doğru| YANLIŞ|||
| Grafik Önbelleğini Yenile| Boolean| Doğru| YANLIŞ|||
|SıralamaAdları| Boolean| Doğru| YANLIŞ|||
| Birleştirilmiş Alanları Doğrula| Boolean| Doğru| YANLIŞ|||

**Ebeveyn adı** : (KaydetmeSeçenekleri)[kaydetmeseçenekleri]