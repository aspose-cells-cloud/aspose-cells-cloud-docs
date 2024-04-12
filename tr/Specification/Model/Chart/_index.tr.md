---
title: Karakter
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/chart/
description: "Aspose.Cells Bulut modeli spesifikasyonu: Tablo. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **çizelge**

 

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| Otomatik Ölçeklendirme| Boolean| Doğru| YANLIŞ|| Microsoft Excel, 3 boyutlu bir grafiği eşdeğer 2 boyutlu grafiğe boyut olarak daha yakın olacak şekilde ölçeklendiriyorsa doğrudur. RightAngleAxes özelliği True olmalıdır.|
| Arka duvar| Sınıf:LinkElement| Doğru| YANLIŞ|| boyutlu bir grafiğin arka duvarını temsil eden bir nesne döndürür.|
| KategoriEksen| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafiğin X eksenini alır.|
| GrafikAlan| Sınıf:LinkElement| Doğru| YANLIŞ|| Çalışma sayfasındaki grafik alanını alır.|
| GrafikVeriTablosu| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafik veri tablosunu temsil eder.|
| Grafik Nesnesi| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafik Şeklini temsil eder;|
| DerinlikYüzde| Tamsayı| Doğru| YANLIŞ|| 3 boyutlu grafiğin derinliğini grafik genişliğinin yüzdesi olarak temsil eder (yüzde 20 ile 2000 arasında).|
| Yükseklik| Tamsayı| Doğru| YANLIŞ|| 3 boyutlu harita görünümünün derece cinsinden yüksekliğini temsil eder.|
| İlk Dilim Açısı| Tamsayı| Doğru| YANLIŞ|| İlk pasta grafiğinin veya halka grafiği diliminin açısını derece cinsinden (dikeyden saat yönünde) alır veya ayarlar. Yalnızca 0 ile 360 arasındaki pasta, 3 boyutlu pasta ve halka grafikleri için geçerlidir.|
| Zemin| Sınıf:LinkElement| Doğru| YANLIŞ|| 3 boyutlu bir grafiğin duvarlarını temsil eden bir nesne döndürür.|
| Boşluk Derinliği| Tamsayı| Doğru| YANLIŞ|| 3 boyutlu grafikteki veri serileri arasındaki mesafeyi işaretçi genişliğinin yüzdesi olarak alır veya ayarlar. Bu özelliğin değeri 0 ile 500 arasında olmalıdır.|
|Boşluk Genişliği| Tamsayı| Doğru| YANLIŞ|| Çubuk veya sütun kümeleri arasındaki boşluğu, çubuk veya sütun genişliğinin yüzdesi olarak döndürür veya ayarlar. Bu özelliğin değeri 0 ile 500 arasında olmalıdır.|
| YükseklikYüzdesi| Tamsayı| Doğru| YANLIŞ|| 3 boyutlu grafiğin yüksekliğini grafik genişliğinin yüzdesi olarak döndürür veya ayarlar (yüzde 5 ile 500 arasında).|
| PivotFieldButton'ları Gizle| Boolean| Doğru| YANLIŞ|| Pivot grafik alanı düğmelerinin yalnızca grafik PivotChart olduğunda gizlenip gizlenmeyeceğini belirtir.|
| Is3D| Boolean| Doğru| YANLIŞ|| Grafiğin 3 boyutlu bir grafik olup olmadığını belirtir.|
| DikdörtgenKöşeli| Boolean| Doğru| YANLIŞ|| Grafik alanının dikdörtgen köşeli olup olmadığını gösteren bir değer alır veya ayarlar. Varsayılan doğrudur.|
| Efsane| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafik efsanesini alır.|
| İsim| Sicim| Doğru| YANLIŞ|||
| NSerisi| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafikteki veri serisini temsil eden bir koleksiyon alır.|
| Sayfa ayarı| Sınıf:LinkElement| Doğru| YANLIŞ|| Bu grafikteki sayfa yapısı açıklamasını temsil eder.|
| Perspektif| Tamsayı| Doğru| YANLIŞ|| boyutlu harita görünümünün perspektifini döndürür veya ayarlar. 0 ile 100 arasında olmalıdır. RightAngleAxes özelliği True ise bu özellik yoksayılır.|
| Özet Kaynak| Sicim| Doğru| YANLIŞ|| Kaynak, pivotTable'ın verileridir. PivotSource boş değilse grafik PivotChart'tır.|
| Atama| Sicim| Doğru| YANLIŞ|| Grafiğin altındaki hücrelere bağlanma şeklini temsil eder.|
| Arsa alanı| Sınıf:LinkElement| Doğru| YANLIŞ|| Eksen onay etiketlerini içeren grafiğin çizim alanını alır.|
| PlotEmptyCellsType| Sicim| Doğru| YANLIŞ|| Boş hücrelerin nasıl çizileceğini alır ve ayarlar.|
| ArsaGörünür Hücreler| Boolean| Doğru| YANLIŞ|| Yalnızca görünür hücrelerin çizilip çizilmeyeceğini belirtir.|
| Baskı Boyutu| Sicim| Doğru| YANLIŞ|| Yazdırılan grafik boyutunu alır ve ayarlar.|
| Dik Açı Eksenleri| Boolean| Doğru| YANLIŞ|| Grafik eksenleri dik açıdaysa doğrudur. Yalnızca 3 boyutlu grafikler için geçerlidir (3B Sütun ve 3B Pasta Grafikleri hariç).|
| Dönüş açısı| Tamsayı| Doğru| YANLIŞ|| 3 boyutlu harita görünümünün dönüşünü temsil eder (grafik alanının z ekseni etrafında derece cinsinden dönüşü).|
| İkinciKategori Ekseni| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafiğin ikinci X eksenini alır.|
|İkinciDeğer Ekseni| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafiğin ikinci Y eksenini alır.|
| SeriEksen| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafiğin seri eksenini alır.|
| Şekiller| Sınıf:LinkElement| Doğru| YANLIŞ|| Bu grafikteki tüm çizim şekillerini döndürür.|
| Veri Tablosunu Göster| Boolean| Doğru| YANLIŞ|| Grafiğin bir veri tablosu görüntüleyip görüntülemediğini gösteren bir değer alır veya ayarlar.|
| Gösteri Efsanesi| Boolean| Doğru| YANLIŞ|| Grafik göstergesinin görüntülenip görüntülenmeyeceğini belirten bir değer alır veya ayarlar. Varsayılan doğrudur.|
| Yan Duvar| Sınıf:LinkElement| Doğru| YANLIŞ|| 3 boyutlu bir grafiğin yan duvarını temsil eden bir nesneyi döndürür.|
| SizeWithPencere| Boolean| Doğru| YANLIŞ|| Microsoft Excel grafiği, grafik sayfası penceresinin boyutuyla eşleşecek şekilde yeniden boyutlandırıyorsa doğrudur.|
| Stil| Tamsayı| Doğru| YANLIŞ|| Yerleşik stili alır ve ayarlar.|
| Başlık| Sınıf:LinkElement| Doğru| YANLIŞ|||
| Tip| Sicim| Doğru| YANLIŞ|||
| Değer Ekseni| Sınıf:LinkElement| Doğru| YANLIŞ|| Grafiğin Y eksenini alır.|
| Duvarlar| Sınıf:LinkElement| Doğru| YANLIŞ|| 3 boyutlu bir grafiğin duvarlarını temsil eden bir nesne döndürür.|
| DuvarlarVeIzgaraÇizgiler2D| Boolean| Doğru| YANLIŞ|| Kılavuz çizgileri 3 boyutlu bir grafik üzerinde iki boyutlu olarak çiziliyorsa doğrudur.|
| bağlantı| Sınıf:Bağlantı| Doğru| YANLIŞ|||

**Ebeveyn adı** : (LinkElement)[bağlantıelement]