---
title: Seri
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/series/
description: "Aspose.Cells Bulut modeli spesifikasyonu: Seri. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
kwords: Excel, Office, Elektronik Tablo, Cloud REST API, Seri
weight: 50
---
## **seri**

 Bir grafikte tek bir veri serisini temsil eden nesneyi kapsüller.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| Alan| Sınıf:Alan| Doğru| YANLIŞ|| Series nesnesinin arka plan alanını temsil eder.|
| Bar3DShapeType| Sicim| Doğru| YANLIŞ|| 3B çubuk veya sütun grafiğiyle kullanılan 3B şekil türünü alır veya ayarlar.|
| Sınır| Sınıf:Çizgi| Doğru| YANLIŞ|| Series nesnesinin kenarlığını temsil eder.|
| KabarcıkÖlçeği| Tamsayı| Doğru| YANLIŞ||Belirtilen grafik grubundaki kabarcıklar için ölçek faktörünü alır veya ayarlar. Varsayılan boyutun yüzdesine karşılık gelen 0 (sıfır) ile 300 arasında bir tamsayı değeri olabilir. Yalnızca kabarcık grafikleri için geçerlidir.|
| Kabarcık Boyutları| Sicim| Doğru| YANLIŞ|| Grafik serisinin kabarcık boyutları değerlerini alır veya ayarlar.|
| Veri SayısıDeğerleri| Tamsayı| Doğru| YANLIŞ|| Veri değerlerinin sayısını alır.|
| Veri etiketleri| Sınıf:DataLabels| Doğru| YANLIŞ|| Belirtilen ASeries için DataLabels nesnesini temsil eder.|
| Ekran adı| Sicim| Doğru| YANLIŞ|| Grafik grafiğinde görüntülenen serinin adını alır.|
| ÇörekDelik Boyutu| Tamsayı| Doğru| YANLIŞ|| Halka grafik grubundaki deliğin boyutunu döndürür veya ayarlar. Delik boyutu, grafik boyutunun yüzde 10 ila 90'ı arasındaki bir yüzdesi olarak ifade edilir.|
| Aşağı Çubuklar| Sınıf: DropBar'lar| Doğru| YANLIŞ|| Çizgi grafiğindeki aşağı çubukları temsil eden bir nesne döndürür. Yalnızca çizgi grafikleri için geçerlidir.|
| Bırakma Hatları| Sınıf:Çizgi| Doğru| YANLIŞ||Çizgi grafiği veya alan grafiğindeki bir serinin bırakma çizgilerini temsil eden bir nesneyi döndürür. Yalnızca çizgi grafik veya alan grafikleri için geçerlidir.|
| Patlama| Tamsayı| Doğru| YANLIŞ|| Açık bir pasta diliminin pasta grafiğinin merkezinden uzaklığı, pasta çapının yüzdesi olarak ifade edilir.|
| İlk Dilim Açısı| Tamsayı| Doğru| YANLIŞ|| İlk pasta grafiğinin veya halka grafiği diliminin açısını derece cinsinden (dikeyden saat yönünde) alır veya ayarlar. Yalnızca 0 ile 360 arasındaki pasta, 3 boyutlu pasta ve halka grafikleri için geçerlidir.|
| Boşluk Genişliği| Tamsayı| Doğru| YANLIŞ|| Çubuk veya sütun kümeleri arasındaki boşluğu, çubuk veya sütun genişliğinin yüzdesi olarak döndürür veya ayarlar. Bu özelliğin değeri 0 ile 500 arasında olmalıdır.|
| Has3DEffect| Boolean| Doğru| YANLIŞ|| Serinin üç boyutlu bir görünümü varsa doğrudur. Yalnızca kabarcık grafikleri için geçerlidir.|
| HasDropLines| Boolean| Doğru| YANLIŞ|| Grafikte düşme çizgileri varsa doğrudur. Yalnızca çizgi grafik veya alan grafikleri için geçerlidir.|
| HasHiLoLines| Boolean| Doğru| YANLIŞ|| Çizgi grafiğinde yüksek-düşük çizgiler varsa doğrudur. Yalnızca çizgi grafikleri için geçerlidir.|
| HasLeaderLines| Boolean| Doğru| YANLIŞ|| Serinin lider çizgileri varsa doğrudur.|
| HasRadarAxisEtiketleri| Boolean| Doğru| YANLIŞ|| Bir radar grafiğinde kategori ekseni etiketleri varsa doğrudur. Yalnızca radar grafikleri için geçerlidir.|
| HasSeriesLines| Boolean| Doğru| YANLIŞ||Yığılmış sütun grafiği veya çubuk grafiğinde seri çizgiler varsa veya Pasta Pasta grafiği veya Pasta Çubuğu grafiğinde iki bölüm arasında bağlayıcı çizgiler varsa doğrudur. Yalnızca yığılmış sütun grafikleri, çubuk grafikler, Pasta Pasta grafikleri veya Pasta Çubuğu grafikleri için geçerlidir.|
| HasUpDownBar'lar| Boolean| Doğru| YANLIŞ|| Çizgi grafiğinde yukarı ve aşağı çubuklar varsa doğrudur. Yalnızca çizgi grafikleri için geçerlidir.|
| MerhabaLoLines| Sınıf:Çizgi| Doğru| YANLIŞ|| Çizgi grafiğindeki bir serinin yüksek-düşük çizgilerini temsil eden bir HiLoLines nesnesi döndürür. Yalnızca çizgi grafikleri için geçerlidir.|
| Otomatik Bölme| Boolean| Doğru| YANLIŞ|| Eşik değerinin otomatik olup olmadığını belirtir.|
| Renk Çeşitliliği| Boolean| Doğru| YANLIŞ|| Noktaların renginin değişip değişmediğini temsil eder. Grafik yalnızca bir seri içermelidir.|
| Lider Çizgiler| Sınıf:Çizgi| Doğru| YANLIŞ||Bir grafikteki lider çizgilerini temsil eder. Lider çizgiler veri etiketlerini veri noktalarına bağlar. Bu nesne bir koleksiyon değil; tek bir lider çizgisini temsil eden hiçbir nesne yoktur.|
| Efsane Girişi| Sınıf:LegendEntry| Doğru| YANLIŞ|| Bu seriye göre efsane girişini alır.|
| İşaretleyici| Sınıf:İşaretçi| Doğru| YANLIŞ|| İşaretçiyi alır.|
| İsim| Sicim| Doğru| YANLIŞ|| Veri serisinin adını alır veya ayarlar.|
| Örtüşmek| Tamsayı| Doğru| YANLIŞ|| Çubukların ve sütunların nasıl konumlandırılacağını belirtir. – 100 ile 100 arasında bir değer olabilir. Yalnızca 2 boyutlu çubuk ve 2 boyutlu sütun grafikleri için geçerlidir.|
| PlotOnSecondAxis| Boolean| Doğru| YANLIŞ|| Bu serinin ikinci değer ekseninde çizilip çizilmediğini gösterir.|
| Puanlar| Sınıf:LinkElement| Doğru| YANLIŞ|| Bir grafikteki bir serideki noktaların toplanmasını alır.|
| İkinciPlotBoyutu| Tamsayı| Doğru| YANLIŞ|| Bir pasta grafiğinin veya pasta grafiğinin bir çubuğunun ikincil bölümünün boyutunu, birincil pastanın boyutunun yüzdesi olarak döndürür veya ayarlar. 5 ila 200 arasında bir değer olabilir.|
| SeriÇizgiler| Sınıf:Çizgi| Doğru| YANLIŞ||Yığılmış bir çubuk grafik veya yığılmış sütun grafiği için seri çizgilerini temsil eden bir SeriesLines nesnesi döndürür. Yalnızca yığılmış çubuk ve yığılmış sütun grafikleri için geçerlidir.|
| Gölge| Boolean| Doğru| YANLIŞ|| Serinin gölgesi varsa doğrudur.|
| Negatif Kabarcıkları Göster| Boolean| Doğru| YANLIŞ|| Grafik grubu için negatif baloncuklar gösteriliyorsa doğrudur. Yalnızca kabarcık grafikleri için geçerlidir.|
| Boyut Temsil Ediyor| Sicim| Doğru| YANLIŞ|| Kabarcık grafiğinde kabarcık boyutunun neyi temsil ettiğini alır veya ayarlar.|
| Düz| Boolean| Doğru| YANLIŞ|| Eğri yumuşatmayı temsil eder. Çizgi grafiği veya dağılım grafiği için eğri yumuşatma açıksa doğrudur. Yalnızca çizgi grafikleriyle bağlanan çizgi ve dağılım için geçerlidir.|
| Bölünmüş Tip| Sicim| Doğru| YANLIŞ|| Bir pasta pastası veya pasta çubuğu grafiğindeki ikinci pasta veya çubukta hangi veri noktalarının bulunduğunun nasıl belirleneceğini belirleyen bir değer döndürür veya ayarlar.|
| Bölünmüş Değer| Yüzer| Doğru| YANLIŞ||Bir pasta pastası veya çubuk pasta grafiğindeki ikinci pasta veya çubukta hangi veri noktalarının bulunduğunu belirlemek için kullanılacak bir değeri döndürür veya ayarlar.|
| Trend Çizgileri| Sınıf:Trend Çizgileri| Doğru| YANLIŞ|| Serinin tüm eğilim çizgilerinin bir koleksiyonunu temsil eden bir nesne döndürür.|
| Tip| Sicim| Doğru| YANLIŞ|| Bir veri serisinin türünü alır veya ayarlar.|
| Yukarı Çubuklar| Sınıf: DropBar'lar| Doğru| YANLIŞ|| Çizgi grafikteki yukarı çubukları temsil eden bir DropBars nesnesi döndürür. Yalnızca çizgi grafikleri için geçerlidir.|
| Değerler| Sicim| Doğru| YANLIŞ|| Grafik serisinin verilerini temsil eder.|
| XErrorBar| Sınıf:ErrorBar| Doğru| YANLIŞ|| Serinin X yönündeki hata çubuğunu temsil eder.|
| XDeğerler| Sicim| Doğru| YANLIŞ|| Grafik serisinin x değerlerini temsil eder.|
| Hata Çubuğu| Sınıf:ErrorBar| Doğru| YANLIŞ|| Serinin Y yönündeki hata çubuğunu temsil eder.|
| bağlantı| Sınıf:Bağlantı| Doğru| YANLIŞ|||

**Ebeveyn adı** : [Bağlantı Öğesi](/specification/model/linkelement)

