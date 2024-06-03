---
title: SoyutHesaplamaEngin
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/abstractcalculationengine/
description: "Aspose.Cells Bulut modeli spesifikasyonu: AbstractCalculationEngine. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
kwords: Excel, Office, Elektronik Tablo, Cloud REST API, AbstractCalculationEngine
weight: 50
---
## **özetHesaplamaMotoru**

Aspose.Cells varsayılan hesaplama motorunu genişletmek için kullanıcının özel hesaplama motorunu temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| IsParamLiteralGereklidir| Boolean| Doğru| YANLIŞ|| Bu motorun hesaplama yaparken parametrenin tam metnine ihtiyacı olup olmadığını gösterir. Varsayılan değer false'tur.|
| IsParamArrayModeGereklidir| Boolean| Doğru| YANLIŞ|| Bu motorun dizi modunda hesaplanması için parametreye ihtiyacı olup olmadığını gösterir. Varsayılan değer false'tur. Özel fonksiyonlar hesaplanırken gerekli ise bu özelliğin true olarak ayarlanması gerekir.|
| ProcessBuiltInFunctions| Boolean| Doğru| YANLIŞ|| Yerleşik motor tarafından desteklenen yerleşik işlevlerin bu uygulama tarafından kontrol edilmesi ve işlenmesi gerekip gerekmediği. Varsayılan yanlıştır. Kullanıcının bazı yerleşik fonksiyonların hesaplama mantığını değiştirmesi gerekiyorsa bu özelliğin true olarak ayarlanması gerekir. Aksi halde lütfen performansın değerlendirilmesi için bu özelliği false olarak bırakın.|

