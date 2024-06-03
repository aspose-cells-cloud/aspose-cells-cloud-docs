---
title: HesaplamaSeçeneği
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/model/calculationoptions/
description: "Aspose.Cells Bulut modeli spesifikasyonu: CalculationOptions. Açma, oluşturma, düzenleme, bölme, birleştirme, karşılaştırma ve dönüştürme gibi özelliklerle Excel ve diğer elektronik tablo belgelerini zahmetsizce yönetin"
kwords: Excel, Office, Elektronik Tablo, Cloud REST API, CalculationOptions
weight: 50
---
## **hesaplamaSeçenekler**

 Hesaplama seçeneklerini temsil eder.

| Mülkiyet adı| Emlak Tipi| Geçersiz kılınabilir| Sadece oku| Varsayılan değer| Tanım|
|:- |:- |:- |:- |:- |:- |
| CalcStackSize| Tamsayı| Doğru| YANLIŞ|| Hücreleri yinelemeli olarak hesaplamak için yığın boyutunu belirtir.|
| Hatayı Yoksay| Boolean| Doğru| YANLIŞ|| Formüller hesaplanırken karşılaşılan hataların göz ardı edilip edilmeyeceğini belirtir. Hata, desteklenmeyen işlev, harici bağlantılar vb. olabilir. Varsayılan değer true'dur.|
| Hassas Strateji| Sicim| Doğru| YANLIŞ|| Hesaplamanın kesinliğini işleme stratejisini belirtir.|
| Özyinelemeli| Boolean| Doğru| YANLIŞ|| Bir hücre hesaplanırken bağımlı hücrelerin yinelemeli olarak hesaplanıp hesaplanmayacağını ve bunun diğer hücrelere bağlı olup olmadığını belirtir. Varsayılan değer doğrudur.|
| Özel Motor|Sınıf:AbstractCalculationEngine| Doğru| YANLIŞ|| Aspose.Cells numaralı varsayılan hesaplama motorunu genişletmek için özel formül hesaplama motoru.|
| HesaplamaMonitör| Sınıf:AbstractCalculationMonitor| Doğru| YANLIŞ|| Kullanıcının formül hesaplamasının ilerlemesini izlemesini sağlayan monitör.|
| BağlantılıVeri Kaynakları|Sıralamak<Class:Workbook> | Doğru| YANLIŞ|| Formüllerde kullanılan dış bağlantılara ilişkin veri kaynaklarını belirtir.|

