---
title: IconSe
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/iconset/
description: "Aspose.Cells Bulut modeli spesifikasyonu: IconSet. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
weight: 50
---
## **simge seti**

 IconSet koşullu biçimlendirme kuralını açıklayın. Bu koşullu biçimlendirme kuralı, simgelere değerlerine göre hücrelere uygulanır.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| CfSimgeler| Konteyner| Doğru| YANLIŞ|| Koleksiyondan alın|
| Cfvo'lar| Konteyner| Doğru| YANLIŞ|| CFValueObjects örneğini alın.|
| Özeldir| Boolean| Doğru| YANLIŞ|| Simge kümesinin özel olup olmadığını gösterir. Varsayılan değer false'tur.|
| Tersi| Boolean| Doğru| YANLIŞ||Bu simge setindeki simgelerin varsayılan sırasının tersine çevrilip çevrilmeyeceğini belirten bayrağı alın veya ayarlayın. Varsayılan değer false'tur.|
| Değeri Göster| Boolean| Doğru| YANLIŞ|| Bu simge setinin uygulandığı hücrelerin değerlerinin gösterilip gösterilmeyeceğini belirten bayrağı alın veya ayarlayın. Varsayılan değer doğrudur.|
| IconSetType| Sicim| Doğru| YANLIŞ|| Görüntülenecek simge seti türünü alın veya ayarlayın. Türün ayarlanması, mevcut Cfvos sayısının yeni türe uygun olup olmadığını otomatik olarak kontrol edecektir. Uyum sağlanmadığı takdirde eski Cfvo'lar temizlenecek ve varsayılan Cfvo'lar eklenecektir.|

