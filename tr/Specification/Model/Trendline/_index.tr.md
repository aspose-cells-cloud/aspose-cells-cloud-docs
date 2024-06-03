---
title: Trend çizgisi
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/trendline/
description: "Aspose.Cells Bulut modeli spesifikasyonu: Trend çizgisi. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
kwords: Excel, Office, Elektronik Tablo, Cloud REST API, Trend Çizgisi
weight: 50
---
## **eğilim çizgisi**

 Bir grafikteki eğilim çizgisini temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| bağlantı| Sınıf:Bağlantı| Doğru| YANLIŞ|||
| Geriye| Yüzer| Doğru| YANLIŞ|| Eğilim çizgisinin geriye doğru uzandığı dönemlerin (veya dağılım grafiğindeki birimlerin) sayısını döndürür veya ayarlar. Dönem sayısı sıfırdan büyük veya sıfıra eşit olmalıdır. Grafik türü sütun ise nokta sayısı 0 ile 0,5 arasında olmalıdır.|
| Veri etiketleri| Sınıf:DataLabels| Doğru| YANLIŞ|| Belirtilen seri için DataLabels nesnesini temsil eder.|
| Görüntü Denklemi| Boolean| Doğru| YANLIŞ|| Trend çizgisi denkleminin grafikte görüntülenip görüntülenmediğini temsil eder (R-kare değeriyle aynı veri etiketinde). Bu özelliği True olarak ayarlamak veri etiketlerini otomatik olarak açar.|
| Görüntülü RSkare| Boolean| Doğru| YANLIŞ||Trend çizgisinin R-kare değerinin grafikte görüntülenip görüntülenmediğini temsil eder (denklemle aynı veri etiketinde). Bu özelliği True olarak ayarlamak veri etiketlerini otomatik olarak açar.|
| İleri| Yüzer| Doğru| YANLIŞ|| Eğilim çizgisinin ileriye doğru uzattığı dönemlerin (veya dağılım grafiğindeki birimlerin) sayısını döndürür veya ayarlar. Dönem sayısı sıfırdan büyük veya sıfıra eşit olmalıdır.|
| Tutmak| Yüzer| Doğru| YANLIŞ|| Eğilim çizgisinin değer eksenini kestiği noktayı döndürür veya ayarlar.|
| IsNameAuto| Boolean| Doğru| YANLIŞ|| Microsoft Excel trend çizgisinin adını otomatik olarak belirlerse döndürür.|
| Efsane Girişi| Sınıf:LegendEntry| Doğru| YANLIŞ|| Bu trend çizgisine göre efsane girişini alır|
| İsim| Sicim| Doğru| YANLIŞ|| Trend çizgisinin adını döndürür.|
| Emir| Tamsayı| Doğru| YANLIŞ|| Eğilim çizgisi türü Polinom olduğunda eğilim çizgisi sırasını (1'den büyük bir tam sayı) döndürür veya ayarlar. Sıralama 2 ile 6 arasında olmalıdır.|
| Dönem| Tamsayı| Doğru| YANLIŞ|| Hareketli ortalama eğilim çizgisinin periyodunu döndürür veya ayarlar.|
| Tip| Sicim| Doğru| YANLIŞ|| Eğilim çizgisi türünü döndürür.|
| BaşlangıçOkUzunluğu| Sicim| Doğru| YANLIŞ|||
| Başlangıç Ok Genişliği| Sicim| Doğru| YANLIŞ|||
| Başlangıç Türü| Sicim| Doğru| YANLIŞ|||
| CapType| Sicim| Doğru| YANLIŞ|||
| Renk| Sınıf:Renkli| Doğru| YANLIŞ|||
| Bileşik Türü| Sicim| Doğru| YANLIŞ|||
| DashType| Sicim| Doğru| YANLIŞ|||
| EndArrowLength| Sicim| Doğru| YANLIŞ|||
| EndArrowWidth| Sicim| Doğru| YANLIŞ|||
| Bitiş Türü| Sicim| Doğru| YANLIŞ|||
| Gradyan Doldurma| Sınıf:GradientFill| Doğru| YANLIŞ|||
| Otomatik| Boolean| Doğru| YANLIŞ|||
| OtomatikRenk| Boolean| Doğru| YANLIŞ|||
| Görünür| Boolean| Doğru| YANLIŞ|||
| Birleştirme Türü| Sicim| Doğru| YANLIŞ|||
| Stil| Sicim| Doğru| YANLIŞ|||
| Şeffaflık| Yüzer| Doğru| YANLIŞ|||
| Ağırlık| Sicim| Doğru| YANLIŞ|||
| AğırlıkPt| Yüzer| Doğru| YANLIŞ|||

**Ebeveyn adı** : [Astar](/specification/model/line)

