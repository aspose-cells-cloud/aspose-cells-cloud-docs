---
title: Cel
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/cell/
description: "Aspose.Cells Bulut modeli spesifikasyonu: Hücre. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
kwords: Excel, Office, Elektronik Tablo, Cloud REST API, Hücre
weight: 50
---
## **hücre**

 Tek bir Çalışma Kitabı hücresini temsil eden nesneyi kapsüller.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| İsim| Sicim| Doğru| YANLIŞ|| Hücrenin adını alır.|
| Sıra| Tamsayı| Doğru| YANLIŞ|| Hücrenin satır numarasını (sıfır tabanlı) alır.|
| Kolon| Tamsayı| Doğru| YANLIŞ|| Hücrenin sütun numarasını (sıfır tabanlı) alır.|
| Değer| Sicim| Doğru| YANLIŞ|| Bu hücrenin içerdiği değeri alır.|
| Tip| Sicim| Doğru| YANLIŞ|| Hücre değer türünü temsil eder.|
| Formül| Sicim| Doğru| YANLIŞ||Formülünü alır veya ayarlar.|
| IsFormula| Boolean| Doğru| YANLIŞ|| Belirtilen hücrenin formül içerip içermediğini temsil eder.|
| Birleştirildi| Boolean| Doğru| YANLIŞ|| Bir hücrenin birleştirilmiş aralığın parçası olup olmadığını kontrol eder.|
| IsArrayHeader| Boolean| Doğru| YANLIŞ|| Hücrenin formülünün ve dizi formülü olduğunu ve dizinin ilk hücresi olduğunu belirtir.|
| IsInArray| Boolean| Doğru| YANLIŞ|| Hücre formülünün bir dizi formülü olup olmadığını gösterir.|
| HataDeğeri| Boolean| Doğru| YANLIŞ|| Bu hücrenin değerinin bir hata olup olmadığını kontrol eder.|
| IsInTable| Boolean| Doğru| YANLIŞ|| Bu hücrenin tablo formülünün parçası olup olmadığını gösterir.|
| IsStyleSet| Boolean| Doğru| YANLIŞ|| Hücrenin stilinin ayarlanıp ayarlanmadığını gösterir. Yanlış döndürürseniz, bu, bu hücrenin varsayılan hücre biçimine sahip olduğu anlamına gelir.|
| HtmlString| Sicim| Doğru| YANLIŞ|| Bu hücredeki verileri ve bazı biçimleri içeren html dizesini alır ve ayarlar.|
| Stil| Sınıf:LinkElement| Doğru| YANLIŞ|||
| Çalışma kağıdı| Sicim| Doğru| YANLIŞ|| Ana çalışma sayfasını alır.|
| bağlantı| Sınıf:Bağlantı| Doğru| YANLIŞ|||

**Ebeveyn adı** : [Bağlantı Öğesi](/specification/model/linkelement)

