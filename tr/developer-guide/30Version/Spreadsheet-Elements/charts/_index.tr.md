---
title: "Excel Grafikleri ile Çalışma"
second_title: "Belge"
linktype: "Grafikler"
type: docs
url: /tr/charts/
aliases: [  /tr/working-with-charts/ ]
keywords: "Aspose, Cells, Excel, grafik, API, REST, Bulut, elektronik tablo"
description: "Aspose.Cells Cloud API ile Excel grafiklerini nasıl yöneteceğinizi öğrenin. Grafikleri alma, ekleme, güncelleme, silme ve görüntü formatlarına dönüştürme için adım adım rehberler, kod örnekleri ve hata işleme."
weight: 100
ArticleTitle: "Excel Grafikleri ile Çalışma – Aspose.Cells Cloud Dokümantasyonu"
---

## Excel Dosyasında Grafiklerle Çalışma

**Son güncelleme:** Temmuz 2026  

Excel grafikleri, kullanıcıların eğilimleri ve desenleri hızlıca anlamasına yardımcı olan verilerin görsel temsilidir.  
Aspose.Cells Cloud API, geliştiricilerin bulutta depolanan Excel çalışma kitapları içindeki bu grafiklerle programlı olarak çalışmasını sağlar. API ile mevcut grafikleri alabilir, yeni grafikler ekleyebilir, başlıklar, eksenler ve efsaneler gibi özelliklerini değiştirebilir, istenmeyen grafikleri silebilir ve raporlama veya ileri işlem için grafikleri görüntü formatlarına dönüştürebilirsiniz. Aşağıdaki bağlantılar, her desteklenen grafikle ilgili eylem için ayrıntılı işlem sayfalarına doğrudan erişim sağlar.

### Hızlı Başvuru

| İşlem | HTTP Yöntemi | Uç Nokta (şablon) | Dokümantasyon |
|-------|--------------|-------------------|---------------|
| Grafik Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Çalışma Sayfasından Grafik Al](/cells/get-chart-from-a-worksheet/) |
| Grafik Ekle | POST | `/cells/{file}/worksheets/{sheet}/charts` | [Çalışma Sayfasına Grafik Ekle](/cells/add-a-chart-in-a-worksheet/) |
| Tüm Grafikleri Sil | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [Çalışma Sayfasından Tüm Grafikleri Sil](/cells/delete-all-charts-from-a-worksheet/) |
| Grafik Sil | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Çalışma Sayfasından Grafik Sil](/cells/delete-a-chart-from-a-worksheet/) |
| Grafik Görüntüye Dönüştür | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [Grafiği Görüntüye Dönüştür](/cells/convert-chart-to-image/) |
| Grafik Alanı Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [Çalışma Sayfasından Grafik Alanı Al](/cells/get-chart-area-from-a-worksheet/) |
| Doldurma Biçimi Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [Çalışma Sayfasından Grafik Alanı Doldurma Biçimi Al](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| Efsane Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Çalışma Sayfasından Grafik Efsanesi Al](/cells/get-chart-legend-from-a-worksheet/) |
| Efsane Güncelle | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Çalışma Sayfasında Grafik Efsanesini Güncelle](/cells/update-chart-legend-in-a-worksheet/) |
| Efsane Göster | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [Çalışma Sayfasında Grafik Efsanesini Göster](/cells/show-chart-legend-in-a-worksheet/) |
| Efsane Gizle | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [Çalışma Sayfasında Grafik Efsanesini Gizle](/cells/hide-chart-legend-in-a-worksheet/) |
| Başlık Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Çalışma Sayfasından Grafik Başlığı Al](/cells/get-chart-title-from-a-worksheet/) |
| Başlık Ayarla | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Excel Çalışma Sayfasında Grafik Başlığı Ayarla](/cells/set-chart-title-in-excel-worksheet/) |
| Başlığı Güncelle | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Excel Çalışma Sayfasında Grafik Başlığını Güncelle](/cells/update-chart-title-in-excel-worksheet/) |
| Başlığı Sil | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Çalışma Sayfasında Grafik Başlığını Sil](/cells/delete-chart-title-in-a-worksheet/) |
| Grafik Özelliklerini Güncelle | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Grafik Özelliklerini Güncelle](/cells/charts/properties/update/) |
| Kategori Ekseni Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Grafik Kategori Ekseni Al](/cells/charts/category-axis/get/) |
| Değer Ekseni Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Grafik Değer Ekseni Al](/cells/charts/value-axis/get/) |
| İkinci Kategori Ekseni Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Grafik İkinci Kategori Ekseni Al](/cells/charts/second-category-axis/get/) |
| İkinci Değer Ekseni Al | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Grafik İkinci Değer Ekseni Al](/cells/charts/second-value-axis/get/) |
| Kategori Ekseni Güncelle | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Grafik Kategori Ekseni Güncelle](/cells/charts/category-axis/update/) |
| Değer Ekseni Güncelle | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Grafik Değer Ekseni Güncelle](/cells/charts/value-axis/update/) |
| İkinci Kategori Ekseni Güncelle | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Grafik İkinci Kategori Ekseni Güncelle](/cells/charts/second-category-axis/update/) |
| İkinci Değer Ekseni Güncelle | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Grafik İkinci Değer Ekseni Güncelle](/cells/charts/second-value-axis/update/) |

- [Çalışma Sayfasından Grafik Al](/cells/get-chart-from-a-worksheet/)
- [Çalışma Sayfasına Grafik Ekle](/cells/add-a-chart-in-a-worksheet/)
- [Çalışma Sayfasından Tüm Grafikleri Sil](/cells/delete-all-charts-from-a-worksheet/)
- [Çalışma Sayfasından Grafik Sil](/cells/delete-a-chart-from-a-worksheet/)
- [Grafiği Görüntüye Dönüştür](/cells/convert-chart-to-image/)
- [Çalışma Sayfasından Grafik Alanı Al](/cells/get-chart-area-from-a-worksheet/)
- [Çalışma Sayfasından Grafik Alanı Doldurma Biçimi Al](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [Çalışma Sayfasından Grafik Efsanesi Al](/cells/get-chart-legend-from-a-worksheet/)
- [Çalışma Sayfasında Grafik Efsanesini Güncelle](/cells/update-chart-legend-in-a-worksheet/)
- [Çalışma Sayfasında Grafik Efsanesini Göster](/cells/show-chart-legend-in-a-worksheet/)
- [Çalışma Sayfasında Grafik Efsanesini Gizle](/cells/hide-chart-legend-in-a-worksheet/)
- [Çalışma Sayfasından Grafik Başlığı Al](/cells/get-chart-title-from-a-worksheet/)
- [Excel Çalışma Sayfasında Grafik Başlığı Ayarla](/cells/set-chart-title-in-excel-worksheet/)
- [Excel Çalışma Sayfasında Grafik Başlığını Güncelle](/cells/update-chart-title-in-excel-worksheet/)
- [Çalışma Sayfasında Grafik Başlığını Sil](/cells/delete-chart-title-in-a-worksheet/)
- [Grafik Özelliklerini Güncelle](/cells/charts/properties/update/)
- [Grafik Kategori Ekseni Al](/cells/charts/category-axis/get/)
- [Grafik Değer Ekseni Al](/cells/charts/value-axis/get/)
- [Grafik İkinci Kategori Ekseni Al](/cells/charts/second-category-axis/get/)
- [Grafik İkinci Değer Ekseni Al](/cells/charts/second-value-axis/get/)
- [Grafik Kategori Ekseni Güncelle](/cells/charts/category-axis/update/)
- [Grafik Değer Ekseni Güncelle](/cells/charts/value-axis/update/)
- [Grafik İkinci Kategori Ekseni Güncelle](/cells/charts/second-category-axis/update/)
- [Grafik İkinci Değer Ekseni Güncelle](/cells/charts/second-value-axis/update/)