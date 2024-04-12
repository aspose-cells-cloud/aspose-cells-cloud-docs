---
title: DataBa
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/databar/
description: "Aspose.Cells Bulut modeli spesifikasyonu: DataBar. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **veri çubuğu**

 DataBar koşullu biçimlendirme kuralını açıklayın. Bu koşullu biçimlendirme kuralı, hücre aralığında derecelendirilmiş bir veri çubuğu görüntüler.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| EksenRenk| Sınıf:Renkli| Doğru| YANLIŞ|| Veri çubukları olarak koşullu biçimlendirmeye sahip hücrelerin eksen rengini alır.|
| Eksen Konumu| Sicim| Doğru| YANLIŞ|| Koşullu biçimlendirme kuralı tarafından belirtilen veri çubuklarının ekseninin konumunu alır veya ayarlar.|
| Bar Sınırı| Sınıf:DataBarBorder| Doğru| YANLIŞ||Veri çubuğunun kenarlığını belirten bir nesne alır.|
| BarFillType| Sicim| Doğru| YANLIŞ|| Veri çubuğunun renkle nasıl doldurulacağını alır veya ayarlar.|
| Renk| Sınıf:Renkli| Doğru| YANLIŞ|| Bu DataBar'ın Rengini alın veya ayarlayın.|
| Yön| Sicim| Doğru| YANLIŞ|| Veri çubuğunun görüntülenme yönünü alır veya ayarlar.|
| MaxCfvo| Sınıf:ConditionalFormattingValue| Doğru| YANLIŞ|| Bu DataBar'ın maksimum değer nesnesini alın veya ayarlayın. FormatConditionValueType.Min türüyle null veya CFValueObject ayarlanamaz.|
| Maksimum uzunluk| Tamsayı| Doğru| YANLIŞ|| Veri çubuğunun maksimum uzunluğunu temsil eder.|
| MinCfvo| Sınıf:ConditionalFormattingValue| Doğru| YANLIŞ|| Bu DataBar'ın minimum değer nesnesini alın veya ayarlayın. FormatConditionValueType.Max türüyle null veya CFValueObject öğesi ayarlanamıyor.|
| MinimumUzunluk| Tamsayı| Doğru| YANLIŞ|| Veri çubuğunun minimum uzunluğunu temsil eder.|
| NegatifBarFormat| Sınıf:NegativeBarFormat| Doğru| YANLIŞ|| Veri çubuğu koşullu biçimlendirme kuralıyla ilişkili NegativeBarFormat nesnesini alır.|
| Değeri Göster| Boolean| Doğru| YANLIŞ|| Bu veri çubuğunun uygulandığı hücrelerin değerlerinin gösterilip gösterilmeyeceğini belirten bayrağı alın veya ayarlayın. Varsayılan değer doğrudur.|

