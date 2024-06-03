---
title: BiçimKoşul
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/formatcondition/
description: "Aspose.Cells Bulut modeli spesifikasyonu: FormatCondition. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
kwords: Excel, Office, Elektronik Tablo, Cloud REST API, FormatCondition
weight: 50
---
## **formatDurum**

 Koşullu biçimlendirme koşulunu temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| Öncelik| Tamsayı| Doğru| YANLIŞ||Bu koşullu biçimlendirme kuralının önceliği. Bu değer hangi formatın değerlendirilip işlenmesi gerektiğini belirlemek için kullanılır. Düşük sayısal değerler, '1'in en yüksek öncelik olduğu yüksek sayısal değerlerden daha yüksek önceliğe sahiptir.|
| Tip| Sicim| Doğru| YANLIŞ|| Koşullu formatın Type olup olmadığını alır ve ayarlar.|
| StopIfTrue| Boolean| Doğru| YANLIŞ|| Doğru, bu kural doğru olarak değerlendirildiğinde bu kurala daha düşük önceliğe sahip hiçbir kural uygulanamaz. Yalnızca Excel 2007 için geçerlidir;|
| Ortalamanın üstü| Sınıf:Ortalamanın Üstünde| Doğru| YANLIŞ|| Koşullu biçimlendirmenin "AboveAverage" örneğini alın. Varsayılan örneğin kuralı, aralıktaki tüm değerler için ortalamanın üzerinde olan hücreleri vurgular. Yalnızca = Ortalamanın Üstündeki türü için geçerlidir.|
| Renk Ölçeği| Sınıf:ColorScale| Doğru| YANLIŞ||Koşullu biçimlendirmenin "ColorScale" örneğini alın. Varsayılan örnek "yeşil-sarı-kırmızı" 3ColorScale'dir. Yalnızca tür = ColorScale için geçerlidir.|
| Veri Çubuğu| Sınıf:DataBar| Doğru| YANLIŞ|| Koşullu biçimlendirmenin "DataBar" örneğini alın. Varsayılan örneğin rengi mavidir. Yalnızca DataBar türü için geçerlidir.|
| Formül1| Sicim| Doğru| YANLIŞ|| Koşullu biçimlendirmeyle ilişkili değeri veya ifadeyi alır ve ayarlar.|
| Formül2| Sicim| Doğru| YANLIŞ|| Koşullu biçimlendirmeyle ilişkili değeri veya ifadeyi alır ve ayarlar.|
| Simge Seti| Sınıf: IconSet| Doğru| YANLIŞ|| Koşullu biçimlendirmenin "IconSet" örneğini alın. Varsayılan örneğin IconSetType'ı TrafficLights31'dir. Yalnızca type = IconSet için geçerlidir.|
| Şebeke| Sicim| Doğru| YANLIŞ|| Koşullu biçim işleç türünü alır ve ayarlar.|
| Stil| Sınıf:Stil| Doğru| YANLIŞ|| Koşullu biçimlendirilmiş hücre aralıklarının stilini alır veya ayarlar.|
| Metin| Sicim| Doğru| YANLIŞ||"Metin şunu içerir" koşullu biçimlendirme kuralındaki metin değeri. Yalnızca type = includeText, notContainsText, beginWith ve endWith için geçerlidir. Varsayılan değer null'dur.|
| Zaman dilimi| Sicim| Doğru| YANLIŞ|| "Gerçekleşen tarih..." koşullu biçimlendirme kuralındaki geçerli zaman aralığı. Yalnızca type = timePeriod için geçerlidir. Varsayılan değer TimePeriodType.Today'dır.|
| En iyi 10| Sınıf:İlk 10| Doğru| YANLIŞ|| Koşullu biçimlendirmenin "Top10" örneğini alın. Varsayılan örneğin kuralı, değerleri ilk 10 parantez içinde yer alan hücreleri vurgular. Yalnızca Top10 türü için geçerlidir.|
| bağlantı| Sınıf:Bağlantı| Doğru| YANLIŞ|||

**Ebeveyn adı** : [Bağlantı Öğesi](/specification/model/linkelement)

**Çocuk Adı** : 
	-  [StilFormatDurum](styleformatcondition) 
