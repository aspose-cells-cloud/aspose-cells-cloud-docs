---
title: Görüntü Kaydetme Seçeneği
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/imagesaveoptions/
description: "Aspose.Cells Bulut modeli spesifikasyonu: ImageSaveOptions. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **imageSaveOptions**

 Görüntü dosyasını kaydetme seçeneklerini temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| GrafikResim Türü| Sicim| Doğru| YANLIŞ|| Dönüştürme sırasında grafik görüntü türünü belirtin.|
| EmbededImageNameInSvg| Sicim| Doğru| YANLIŞ|| Gömülü görüntünün dosya adını svg'de belirtin. Bu, "c:\\xpsEmbeded" gibi bir dizine sahip tam yol olmalıdır|
| Yatay Çözünürlük| Tamsayı| Doğru| YANLIŞ|| Oluşturulan görüntüler için yatay çözünürlüğü inç başına nokta cinsinden alır veya ayarlar. Emf formatındaki görüntüler dışında görüntü oluşturma yöntemini uygular. Varsayılan değer 96'dır.|
| Görüntü formatı| Sicim| Doğru| YANLIŞ||Oluşturulan görüntülerin formatını alır veya ayarlar. Bitmap nesnesi döndüren yöntemi uygulamayın. Varsayılan değer ImageFormat.Bmp'dir. Bitmap nesnesi döndüren yöntemi uygulamayın.|
| IsCellAutoFit| Boolean| Doğru| YANLIŞ|| Hücrelerin genişliğinin ve yüksekliğinin hücre değerine göre otomatik olarak sığdırılıp sığdırılmayacağını belirtir. Varsayılan değer false'tur.|
| Sayfa Başına Bir Sayfa| Boolean| Doğru| YANLIŞ|| OnePagePerSheet true olursa, sonuçta bir sayfanın tüm içeriği yalnızca bir sayfaya yazdırılır. Pagesetup'ın kağıt boyutu geçersiz olacak ve diğer pagesetup ayarları geçerli olmaya devam edecektir.|
| YalnızcaAlan| Boolean| Doğru| YANLIŞ|| Bu özellik true ise, yalnızca Alan çıktısı alınacak ve hiçbir ölçek etkili olmayacaktır.|
| Yazdırma Sayfası| Sicim| Doğru| YANLIŞ|| Hangi sayfaların yazdırılmayacağını belirtir.|
| PrintWithStatusDialog| Boolean| Doğru| YANLIŞ|| PrintWithStatusDialog = true ise geçerli yazdırma durumunu gösteren bir iletişim kutusu olacaktır. aksi takdirde böyle bir diyalog gösterilmez.|
|Kalite| Tamsayı| Doğru| YANLIŞ||Yalnızca sayfaları Jpeg biçiminde kaydederken uygulanacak, oluşturulan görüntülerin kalitesini belirleyen bir değer alır veya ayarlar. Yalnızca JPEG'e kaydedildiğinde etkili olur. Değer 0 ile 100 arasında olmalıdır. Varsayılan değer 100'dür.|
| TiffSıkıştırma| Sicim| Doğru| YANLIŞ|| Yalnızca sayfaları Tiff biçiminde kaydederken uygulanacak sıkıştırma türünü alır veya ayarlar. Yalnızca TIFF'e kaydedildiğinde etkili olur. Varsayılan değer Lzw'dir.|
| Dikey Çözünürlük| Tamsayı| Doğru| YANLIŞ|| Oluşturulan görüntüler için dikey çözünürlüğü inç başına nokta cinsinden alır veya ayarlar. Emf formatındaki görüntü dışında görüntü oluşturma yöntemini uygular. Varsayılan değer 96'dır.|
| Formatı Kaydet| Sicim| Doğru| YANLIŞ|||
| Önbelleğe Alınmış DosyaKlasörü| Sicim| Doğru| YANLIŞ|||
| Net veriler| Boolean| Doğru| YANLIŞ|||
| Dizin Oluştur| Boolean| Doğru| YANLIŞ|||
| HTTPSıkıştırmayı Etkinleştir| Boolean| Doğru| YANLIŞ|||
| Grafik Önbelleğini Yenile| Boolean| Doğru| YANLIŞ|||
|SıralamaAdları| Boolean| Doğru| YANLIŞ|||
| Birleştirilmiş Alanları Doğrula| Boolean| Doğru| YANLIŞ|||

**Ebeveyn adı** : (KaydetmeSeçenekleri)[kaydetmeseçenekleri]