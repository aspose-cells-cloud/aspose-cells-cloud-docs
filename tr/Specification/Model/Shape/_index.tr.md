---
title: Şap
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/shape/
description: "Aspose.Cells Bulut modeli spesifikasyonu: Şekil. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
kwords: Excel, Office, Elektronik Tablo, Cloud REST API, Şekil
weight: 50
---
## **şekil**

 Msodrawing nesnesini temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| İsim| Sicim| Doğru| YANLIŞ|| Şeklin adını alır ve ayarlar.|
| MsoDrawingType| Sicim| Doğru| YANLIŞ|| Mso çizim tipini alır.|
| Otomatik Şekil Türü| Sicim| Doğru| YANLIŞ|| Otomatik şekil türünü alır ve ayarlar.|
| Atama| Sicim| Doğru| YANLIŞ|| Çizim nesnesinin altındaki hücrelere bağlanma şeklini temsil eder. Özellik, bir nesnenin çalışma sayfasına yerleştirilmesini kontrol eder.|
| ÜstSolSatır| Tamsayı| Doğru| YANLIŞ|| Sol üst köşe satır dizinini temsil eder.|
| Tepe| Tamsayı| Doğru| YANLIŞ|| Piksel birimi cinsinden şeklin üst satırından dikey uzaklığını temsil eder.|
| ÜstSol Sütun| Tamsayı| Doğru| YANLIŞ|| Sol üst köşe sütun dizinini temsil eder.|
| Sol| Tamsayı| Doğru| YANLIŞ|| Şeklin sol sütunundan yatay uzaklığını piksel cinsinden temsil eder.|
| AltSağSatır| Tamsayı| Doğru| YANLIŞ|| Sağ alt köşe satır dizinini temsil eder.|
| Alt| Tamsayı| Doğru| YANLIŞ||Piksel biriminde, şeklin alt alt köşe satırından dikey uzaklığının genişliğini temsil eder.|
| Alt Sağ Sütun| Tamsayı| Doğru| YANLIŞ|| Sağ alt köşe sütun dizinini temsil eder.|
| Sağ| Tamsayı| Doğru| YANLIŞ|| Şeklin yatay uzaklığının sağ alt köşe sütunundan genişliğini piksel cinsinden temsil eder.|
| Genişlik| Tamsayı| Doğru| YANLIŞ|| Piksel birimi cinsinden şeklin genişliğini temsil eder.|
| Yükseklik| Tamsayı| Doğru| YANLIŞ|| Piksel birimi cinsinden şeklin yüksekliğini temsil eder.|
| X| Tamsayı| Doğru| YANLIŞ|| Çalışma sayfasının sol kenarlığından şeklin yatay uzaklığını piksel biriminde alır ve ayarlar.|
| e| Tamsayı| Doğru| YANLIŞ|| Çalışma sayfasının üst kenarlığından şeklin dikey uzaklığını piksel biriminde alır ve ayarlar.|
| Dönüş açısı| Yüzer| Doğru| YANLIŞ|| Şeklin dönüşünü alır ve ayarlar.|
|HtmlMetin| Sicim| Doğru| YANLIŞ|| Bu metin kutusundaki verileri ve bazı formatları içeren html dizesini alır ve ayarlar.|
| Metin| Sicim| Doğru| YANLIŞ|| Bu TextBox nesnesindeki dizeyi temsil eder.|
| Alternatif metin| Sicim| Doğru| YANLIŞ|| Nesnenin açıklayıcı (alternatif) metin dizesini döndürür veya ayarlar.|
| MetinYatay Hizalama| Sicim| Doğru| YANLIŞ|| Şeklin metin yatay hizalama türünü alır ve ayarlar.|
| MetinYatayTaşma| Sicim| Doğru| YANLIŞ|| Metni içeren şeklin metin yatay taşma türünü alır ve ayarlar.|
| Metin Yönlendirme Türü| Sicim| Doğru| YANLIŞ||Şeklin metin yönlendirme türünü alır ve ayarlar.|
| MetinDikey Hizalama| Sicim| Doğru| YANLIŞ|| Şeklin metin dikey hizalama türünü alır ve ayarlar.|
| MetinDikeyTaşma| Sicim| Doğru| YANLIŞ|| Metni içeren şeklin metin dikey taşma türünü alır ve ayarlar.|
| İşGrubu| Boolean| Doğru| YANLIŞ|| Şeklin bir grup olup olmadığını belirtir.|
| Gizli| Boolean| Doğru| YANLIŞ|| Nesnenin görünür olup olmadığını belirtir.|
| IsLockAspectRatio| Boolean| Doğru| YANLIŞ|| Doğru, en boy oranında değişikliğe izin verilmediği anlamına gelir.|
| Kilitli| Boolean| Doğru| YANLIŞ|| Nesne kilitliyse True, sayfa korunurken nesne değiştirilebiliyorsa False.|
| Yazdırılabilir| Boolean| Doğru| YANLIŞ|| Nesne yazdırılabilirse doğrudur|
| Metin Sarılmış| Boolean| Doğru| YANLIŞ|| Metin içeren şeklin metin sarma türünü alır ve ayarlar.|
| IsWordArt| Boolean| Doğru| YANLIŞ|| Bu şeklin bir kelime sanatı olup olmadığını belirtir.|
| Bağlantılı Hücre| Sicim| Doğru| YANLIŞ|| Denetimin değerine bağlı çalışma sayfası aralığını alır veya ayarlar.|
| ZOrderPozisyonu| Tamsayı| Doğru| YANLIŞ|| Bir şeklin z sırasına göre konumunu döndürür.|
| Yazı tipi| Sınıf: Yazı Tipi| Doğru| YANLIŞ|| Şeklin yazı tipini temsil eder.|
| Köprü| Sicim| Doğru| YANLIŞ|| Şeklin köprüsünü alır.|
| bağlantı| Sınıf:Bağlantı| Doğru| YANLIŞ|||

**Ebeveyn adı** : [Bağlantı Öğesi](/specification/model/linkelement)

**Çocuk Adı** : 
	-  [ArcShape](arcshape) 
	-  [Otomatik Şekil](autoshape) 
	-  [Düğme](button) 
	-  [HücrelerÇizim](cellsdrawing) 
	-  [Onay Kutusu](checkbox) 
	-  [Açılan kutu](combobox) 
	-  [Yorum Şekli](commentshape) 
	-  [Biçim](form) 
	-  [Grup Kutusu](groupbox) 
	-  [Grup Şekli](groupshape) 
	-  [Etiket](label) 
	-  [Çizgi Şekli](lineshape) 
	-  [Liste kutusu](listbox) 
	-  [Ole nesnesi](oleobject) 
	-  [Oval](oval) 
	-  [Resim](picture) 
	-  [Radyo düğmesi](radiobutton) 
	-  [Dikdörtgen şekil](rectangleshape) 
	-  [Kaydırma çubuğu](scrollbar) 
	-  [Döndürücü](spinner) 
	-  [Metin kutusu](textbox) 
	-  [Grafik Şekli](chartshape) 
