---
title: "Aspose.Cells Cloud 3.0 Geliştirici Kılavuzu"
ArticleTitle: "Aspose.Cells Cloud 3.0 REST API Geliştirici Kılavuzu – Excel Çalışma Kitabı Oluşturma, Dönüştürme ve Stil Verme"
second_title: "Belge"
type: docs
url: /tr/developer-guide-3.0/
aliases: [/tr/developer-guide/v3.0/,/tr/developer-guide-v3.0/]
keywords: "Aspose.Cells Cloud, Excel REST API, çalışma kitabını dönüştürme, grafik API'si, veri içe aktarma, dışa aktarma, PDF, CSV, JSON, geliştirici kılavuzu"
description: "Aspose.Cells Cloud 3.0 REST API'lerini kullanarak Excel çalışma kitapları oluşturma, dönüştürme, stillendirme, grafikler, tablolar ve daha fazlası konularında bilgi edinin. Kod örnekleri ve en iyi uygulama önerileri içerir."
weight: 150
---

## Aspose.Cells Cloud REST API’leri ile Çalışmak

**Aspose.Cells Cloud 3.0 Geliştirici Kılavuzu**, Excel çalışma kitapları ve çalışma sayfaları için en çok kullanılan REST API işlemleriyle ilgili özet, aranabilir bir bilgi kaynağı sunar. Bu kılavuz, Excel dosyalarını programlı olarak oluşturma, değiştirme, dönüştürme ve işlemek isteyen geliştiriciler için hazırlanmıştır. Aşağıdaki bölümleri kullanarak ihtiyacınız olan işlemi bulun; her bir bağlantı, istek sözdizimi, parametreler ve örnekler içeren ayrıntılı sayfaya yönlendirir. Bu ana sayfa, **Aspose.Cells Cloud REST API** referansını merkezileştirerek, çalışma kitabına ilişkin uç noktalar, grafik yönetimi, veri içe/dışa aktarma ve işlevlerini daha kolay bulmanızı sağlar.

**Ön Koşullar:** API’leri kullanmadan önce geçerli bir Aspose Cloud hesabınızın, bir API anahtarınızın ve gizli anahtarınızın ve geliştirme ortamınız için uygun SDK’ların kurulu olduğundan emin olun.

### İçindekiler
- [Dosya İşlemleri](#file-operations)
- [Ana Sayfa (Hücre Biçimlendirme ve Satır/Sütun Yönetimi)](#home-cell-formatting--rowcolumn-management)
- [Ekle (Grafikler, Tablolar ve OLE Nesneleri)](#insert-charts-tables--ole-objects)
- [Sayfa Düzeni (Sayfa Sonları ve Ayarlar)](#page-layout-page-breaks--setup)
- [Formüller (Hesaplama ve İsimler)](#formulas-calculate--names)
- [Veri (Anahat, Filtre ve İçe Aktarma)](#data-outline-filter--import)
- [İnceleme (Yorumlar ve Korumalar)](#review-comments--protection)
- [Görünüm (Pencere ve Yakınlaştırma Kontrolleri)](#view-window--zoom-controls)

### Hızlı API Özeti

| API Grubu | Örnek Uç Nokta | Temel Eylem |
|-----------|----------------|----------------|
| **Çalışma Kitabı Oluştur** | `POST /cells/workbook` | Yeni boş bir Excel çalışma kitabını oluştur |
| **Çalışma Kitabını Dönüştür** | `PUT /cells/workbook/convert` | Excel dosyasını PDF, CSV, JSON vb. formatlara dönüştür |
| **Grafik Ekle** | `POST /cells/worksheets/{sheetName}/charts` | Çalışma sayfasına yeni bir grafik ekle |
| **Tabloları Yönet** | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | Liste nesnesini (tablo) güncelle veya sil |
| **Veri İçe Aktar** | `POST /cells/worksheets/{sheetName}/import` | CSV, JSON, resim veya dizileri çalışma sayfasına içe aktar |
| **Formülleri Hesapla** | `POST /cells/workbook/calculate` | Çalışma kitabındaki tüm formülleri yeniden hesapla |
| **Filtre Uygula** | `POST /cells/worksheets/{sheetName}/filters` | Otomatik Filtre kriterlerini ekle veya kaldır |
| **Çalışma Kitabını Korumalı Yap** | `POST /cells/workbook/protect` | Çalışma kitabına şifre koruması uygula |

Bu yüksek frekanslı işlemler, **Aspose.Cells Cloud Excel REST API**’sinin temel işlevlerini kapsar ve doğrudan ayrıntılı belgeleme sayfalarına bağlanır.

Hızlı API Özeti tablosunun PDF sürümünü çevrimdışı referans için indirebilirsiniz.

{{< tabs tabTotal="8" tabID="1" tabName1="Dosya" tabName2="Ana Sayfa" tabName3="Ekle" tabName4="Sayfa Düzeni" tabName5="Formüller" tabName6="Veri" tabName7="İnceleme" tabName8="Görünüm" >}}
{{< tab tabNum="1" >}}
<div class="row">
    <div class="col-md-6">
        <p>Çalışma Kitabı: Yeni Oluştur, Dönüştür, Farklı Kaydet</p>
        <ul>
            <li><a href="/tr/cells/create-an-empty-excel-workbook/" title="API ile boş bir Excel çalışma kitabını oluştur" rel="noopener">Boş bir Excel çalışma kitabını oluştur.</a></li>
            <li><a href="/tr/cells/create-excel-workbook-from-a-template-file/" title="Şablon dosyasından bir çalışma kitabını oluştur" rel="noopener">Şablon dosyasından bir Excel çalışma kitabını oluştur.</a></li>
            <li><a href="/tr/cells/create-excel-workbook-from-a-smartmarker-template/" title="SmartMarker şablonundan bir çalışma kitabını oluştur" rel="noopener">SmartMarker şablonundan bir Excel çalışma kitabını oluştur.</a></li>
            <li><a href="/tr/cells/convert/" title="Excel çalışma kitabını başka bir formata dönüştür" rel="noopener">Excel çalışma kitabını farklı dosya formatlarına dönüştür.</a></li>
            <li><a href="/tr/cells/saveas-other-formats/" title="Excel çalışma kitabını başka bir formatta kaydet" rel="noopener">Excel çalışma kitabını farklı dosya formatlarında kaydet.</a></li>
        </ul>
        <p>Ara, Değiştir</p>
        <ul>
            <li><a href="/tr/cells/search/" title="Excel dosyalarında metin ara" rel="noopener">Excel dosyalarında metin ara.</a></li>
            <li><a href="/tr/cells/replace/" title="Excel dosyalarında değerleri değiştir" rel="noopener">Excel dosyalarında eski değerleri yeni değerlerle değiştir.</a></li>
        </ul>
        <p>Sıkıştır</p>
        <ul>
            <li><a href="/tr/cells/compress/" title="Excel dosyalarını sıkıştır" rel="noopener">Excel dosyalarını sıkıştır.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Çalışma Kitabı: Birleştir, Böl</p>
        <ul>
            <li><a href="/tr/cells/merge/" title="Birden fazla Excel çalışma kitabını birleştir" rel="noopener">Excel çalışma kitaplarını birleştir.</a></li>
            <li><a href="/tr/cells/split/" title="Excel çalışma kitabını ayrı dosyalara böl" rel="noopener">Excel çalışma kitaplarını böl.</a></li>
        </ul>
        <p>Su İmzaları</p>
        <ul>
            <li><a href="/tr/cells/add-background-in-workbook/" title="Çalışma kitabına arka plan resmi ekle" rel="noopener">Çalışma kitabına arka plan ekle.</a></li>
            <li><a href="/tr/cells/delete-background-in-workbook/" title="Çalışma kitabının arka plan resmini sil" rel="noopener">Çalışma kitabından arka plan sil.</a></li>
            <li><a href="/tr/cells/set-background-or-watermark-for-excel-worksheet/" title="Çalışma sayfasına arka plan veya su imzası ayarla" rel="noopener">Excel çalışma sayfasına arka plan veya su imzası ayarla.</a></li>
            <li><a href="/tr/cells/delete-background-or-watermark-of-excel-worksheet/" title="Çalışma sayfasının arka planını veya su imzasını sil" rel="noopener">Excel çalışma sayfasından arka plan veya su imzası sil.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>Hücre yazı tipleri, stilleri, koşullu biçimlendirme ve değerleri</p>
        <ul>
            <li><a href="/tr/cells/get-cell-style-from-a-worksheet/" title="Çalışma sayfasından bir hücre stili al" rel="noopener">Excel çalışma sayfasından hücre stili al.</a></li>
            <li><a href="/tr/cells/update-multiple-cells-style/" title="Birden fazla hücre stilini güncelle" rel="noopener">Excel çalışma sayfasında birden fazla hücrenin stilini güncelle.</a></li>
            <li><a href="/tr/cells/change-cell-style-in-excel-worksheet/" title="Tek bir hücrenin stilini değiştir" rel="noopener">Excel çalışma sayfasında hücre stilini güncelle.</a></li>
            <li><a href="/tr/cells/apply-rich-text-formatting-to-a-cell/" title="Hücreye zengin metin biçimlendirmesi uygula" rel="noopener">Excel çalışma sayfasında hücreye zengin metin biçimlendirmesi ayarla.</a></li>
            <li><a href="/tr/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="Hücre içeriklerini ve stillerini temizle" rel="noopener">Excel çalışma sayfasındaki hücre içeriklerini ve stillerini temizle.</a></li>
            <li><a href="/tr/cells/working-with-conditional-formatting/" title="Koşullu biçimlendirme kurallarını yönet" rel="noopener">Excel çalışma sayfasına koşullu biçimlendirme ekle, sil ve güncelle.</a></li>
            <li><a href="/tr/cells/set-value-of-a-cell-in-a-worksheet/" title="Hücrenin değerini ayarla" rel="noopener">Excel çalışma sayfasında hücrenin değerini ayarla.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Satır/Sütun: Ekle, Sil, Kopyala, Gizle ve Otomatik Uydur</p>
        <ul>
            <li><a href="/tr/cells/add-an-empty-row-in-a-worksheet/" title="Çalışma sayfasına boş bir satır ekle" rel="noopener">Excel çalışma sayfasına boş bir satır ekle.</a></li>
            <li><a href="/tr/cells/delete-row-from-a-worksheet/" title="Çalışma sayfasından bir satır sil" rel="noopener">Excel çalışma sayfasından bir satır sil.</a></li>
            <li><a href="/tr/cells/copy-rows-in-excel-worksheet/" title="Çalışma sayfası içinde satırları kopyala" rel="noopener">Excel çalışma sayfasında satırları kopyala.</a></li>
            <li><a href="/tr/cells/hide-rows-in-excel-worksheet/" title="Çalışma sayfasında satırları gizle" rel="noopener">Excel çalışma sayfasında satırları gizle.</a></li>
            <li><a href="/tr/cells/auto-fit-rows-in-excel-workbooks/" title="Çalışma kitabında satırları otomatik uydur" rel="noopener">Excel çalışma kitabında satırları otomatik uydur.</a></li>
            <li><a href="/tr/cells/columns/add/" title="Çalışma sayfasına boş bir sütun ekle" rel="noopener">Excel çalışma sayfasına boş bir sütun ekle.</a></li>
            <li><a href="/tr/cells/columns/delete/" title="Çalışma sayfasından bir sütun sil" rel="noopener">Excel çalışma sayfasından bir sütun sil.</a></li>
            <li><a href="/tr/cells/columns/copy/" title="Çalışma sayfası içinde sütunları kopyala" rel="noopener">Excel çalışma sayfasında sütunları kopyala.</a></li>
            <li><a href="/tr/cells/columns/hide/" title="Çalışma sayfasında sütunları gizle" rel="noopener">Excel çalışma sayfasında sütunları gizle.</a></li>
            <li><a href="/tr/cells/columns/autofit/" title="Çalışma kitabında sütunları otomatik uydur" rel="noopener">Excel çalışma kitabında sütunları otomatik uydur.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>Grafik</p>
        <ul>
            <li><a href="/tr/cells/add-a-chart-in-a-worksheet/" title="Çalışma sayfasına bir grafik ekle" rel="noopener">Excel çalışma sayfasına bir grafik ekle.</a></li>
            <li><a href="/tr/cells/delete-a-chart-from-a-worksheet/" title="Çalışma sayfasından bir grafik sil" rel="noopener">Excel çalışma sayfasından bir grafik sil.</a></li>
            <li><a href="/tr/cells/delete-all-charts-from-a-worksheet/" title="Çalışma sayfasındaki tüm grafikleri sil" rel="noopener">Excel çalışma sayfasındaki tüm grafikleri sil.</a></li>
            <li><a href="/tr/cells/convert-chart-to-image/" title="Bir grafikleri resim dosyasına dönüştür" rel="noopener">Bir grafikleri resime dönüştür.</a></li>
            <li><a href="/tr/cells/hide-chart-legend-in-a-worksheet/" title="Grafik anahtarını gizle" rel="noopener">Excel çalışma sayfasında grafik anahtarını gizle.</a></li>
            <li><a href="/tr/cells/update-chart-title-in-excel-worksheet/" title="Grafik başlığını güncelle" rel="noopener">Excel çalışma sayfasında grafik başlığını güncelle.</a></li>
            <li><a href="/tr/cells/delete-chart-title-in-a-worksheet/" title="Grafik başlığını sil" rel="noopener">Çalışma sayfasından grafik başlığını sil.</a></li>
        </ul>
        <p>Tablo</p>
        <ul>
            <li><a href="/tr/cells/add-a-list-object-or-table-inside-the-worksheet/" title="Çalışma sayfasına bir tablo (liste nesnesi) ekle" rel="noopener">Excel çalışma sayfasına bir liste nesnesi ekle.</a></li>
            <li><a href="/tr/cells/update-a-list-object-or-table-inside-the-worksheet/" title="Çalışma sayfasındaki bir tabloyu güncelle" rel="noopener">Excel çalışma sayfasında bir liste nesnesini güncelle.</a></li>
            <li><a href="/tr/cells/convert-list-object-or-table-to-range/" title="Bir tabloyu bir aralığa dönüştür" rel="noopener">Bir liste nesnesini bir aralığa dönüştür.</a></li>
            <li><a href="/tr/cells/sort-table-data/" title="Tablo içindeki verileri sırala" rel="noopener">Tablo verilerini sırala.</a></li>
        </ul>
        <p>OleObject</p>
        <ul>
            <li><a href="/tr/cells/add-oleobject-to-excel-worksheet/" title="Çalışma sayfasına bir OLE nesnesi ekle" rel="noopener">Excel çalışma sayfasına bir OLE nesnesi ekle.</a></li>
            <li><a href="/tr/cells/update-a-specific-oleobject-from-excel-worksheet/" title="Belirli bir OLE nesnesini güncelle" rel="noopener">Excel çalışma sayfasında belirli bir OLE nesnesini güncelle.</a></li>
            <li><a href="/tr/cells/convert-oleobject-to-image/" title="Bir OLE nesnesini resme dönüştür" rel="noopener">OLE nesnesini resme dönüştür.</a></li>
            <li><a href="/tr/cells/delete-all-oleobjects-from-excel-worksheet/" title="Çalışma sayfasındaki tüm OLE nesnelerini sil" rel="noopener">Excel çalışma sayfasındaki tüm OLE nesnelerini sil.</a></li>
            <li><a href="/tr/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="Belirli bir OLE nesnesini sil" rel="noopener">Excel çalışma sayfasından belirli bir OLE nesnesini sil.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Şekil</p>
        <ul>
            <li><a href="/tr/cells/add-a-shape-inside-the-worksheet/" title="Çalışma sayfasına bir şekil ekle" rel="noopener">Excel çalışma sayfasına bir şekil ekle.</a></li>
            <li><a href="/tr/cells/delete-all-shapes-inside-the-worksheet/" title="Çalışma sayfasındaki tüm şekilleri sil" rel="noopener">Excel çalışma sayfasındaki tüm şekilleri sil.</a></li>
            <li><a href="/tr/cells/delete-a-shape-by-index-inside-the-worksheet/" title="İndekse göre bir şekli sil" rel="noopener">Excel çalışma sayfasından indekse göre bir şekil sil.</a></li>
        </ul>
        <p>Pivot Tablo</p>
        <ul>
            <li><a href="/tr/cells/add-a-pivot-table-in-a-worksheet/" title="Çalışma sayfasına bir pivot tablo ekle" rel="noopener">Excel çalışma sayfasına bir pivot tablo ekle.</a></li>
            <li><a href="/tr/cells/delete-worksheet-pivot-tables/" title="Çalışma sayfasındaki tüm pivot tabloları sil" rel="noopener">Excel çalışma sayfasındaki tüm pivot tabloları sil.</a></li>
            <li><a href="/tr/cells/delete-worksheet-pivot-table-by-index/" title="İndekse göre bir pivot tabloyu sil" rel="noopener">Excel çalışma sayfasından indekse göre bir pivot tabloyu sil.</a></li>
            <li><a href="/tr/cells/update-cell-style-for-pivot-table/" title="Pivot tabloda hücre stilini güncelle" rel="noopener">Excel çalışma sayfasındaki pivot tablonun hücre stilini güncelle.</a></li>
            <li><a href="/tr/cells/update-style-for-pivot-table/" title="Pivot tablonun genel stilini güncelle" rel="noopener">Excel çalışma sayfasındaki pivot tablonun stilini güncelle.</a></li>
            <li><a href="/tr/cells/working-with-pivot-filters/" title="Pivot tablo filtreleriyle çalış" rel="noopener">Excel çalışma sayfasında pivot filtreleriyle çalış.</a></li>
            <li><a href="/tr/cells/hide-pivot-field-item/" title="Pivot alanı ögesini gizle" rel="noopener">Excel çalışma sayfasında pivot alan ögelerini gizle.</a></li>
            <li><a href="/tr/cells/move-pivot-table/" title="Pivot tabloyu çalışma sayfası içinde taşı" rel="noopener">Excel çalışma sayfasında pivot tabloyu taşı.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>Sayfa Sonu</p>
        <ul>
            <li><a href="/tr/cells/insert-horizontal-page-break-inside-worksheet/" title="Yatay bir sayfa sonu ekle" rel="noopener">Excel çalışma sayfasına yatay bir sayfa sonu ekle.</a></li>
            <li><a href="/tr/cells/insert-vertical-page-break-inside-worksheet/" title="Dikey bir sayfa sonu ekle" rel="noopener">Excel çalışma sayfasına dikey bir sayfa sonu ekle.</a></li>
            <li><a href="/tr/cells/delete-horizontal-page-break-inside-worksheet/" title="Yatay sayfa sonunu sil" rel="noopener">Excel çalışma sayfasından yatay sayfa sonunu sil.</a></li>
            <li><a href="/tr/cells/delete-vertical-page-break-inside-worksheet/" title="Dikey sayfa sonunu sil" rel="noopener">Excel çalışma sayfasından dikey sayfa sonunu sil.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Sayfa Ayarı</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>Hesapla</p>
        <ul>
            <li><a href="/tr/cells/calculate-all-formulas-in-a-workbook/" title="Çalışma kitabındaki tüm formülleri hesapla" rel="noopener">Excel çalışma kitabındaki tüm formülleri hesapla.</a></li>
            <li><a href="/tr/cells/calculate-cells-formula/" title="Belirli bir hücrenin formülünü hesapla" rel="noopener">Excel çalışma kitabında hücre formüllerini hesapla.</a></li>
            <li><a href="/tr/cells/calculate-formula-in-a-worksheet/" title="Çalışma sayfasında bir formülü hesapla" rel="noopener">Excel çalışma sayfasında bir formülü hesapla.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>İsim</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>Anahat</p>
        <ul>
            <li><a href="/tr/cells/group-rows-in-excel-worksheet/" title="Çalışma sayfasında satırları grupla" rel="noopener">Excel çalışma sayfasında satırları grupla.</a></li>
            <li><a href="/tr/cells/ungroup-rows-in-excel-worksheet/" title="Çalışma sayfasındaki satır gruplarını kaldır" rel="noopener">Excel çalışma sayfasındaki satır gruplarını kaldır.</a></li>
        </ul>
        <p>Filtre</p>
        <ul>
            <li><a href="/tr/cells/add-a-filter-for-a-filter-column/" title="Bir sütuna bir filtre ekle" rel="noopener">Excel çalışma sayfasına bir sütun için filtre ekle.</a></li>
            <li><a href="/tr/cells/delete-a-filter-for-a-filter-column/" title="Bir sütun filtresini sil" rel="noopener">Excel çalışma sayfasından bir sütun filtresini sil.</a></li>
            <li><a href="/tr/cells/remove-a-date-filter/" title="Tarih filtresini kaldır" rel="noopener">Excel çalışma sayfasından bir tarih filtresini kaldır.</a></li>
            <li><a href="/tr/cells/add-an-icon-filter/" title="Bir simge filtresi ekle" rel="noopener">Excel çalışma sayfasına bir simge filtresi ekle.</a></li>
            <li><a href="/tr/cells/add-date-filter-in-a-worksheet/" title="Bir tarih filtresi ekle" rel="noopener">Excel çalışma sayfasına bir tarih filtresi ekle.</a></li>
            <li><a href="/tr/cells/filter-data-by-using-an-autofilter/" title="Otomatik Filtre kullanarak verileri filtrele" rel="noopener">Excel çalışma sayfasında Otomatik Filtre kullanarak verileri filtrele.</a></li>
            <li><a href="/tr/cells/filter-the-top-10-items-in-the-list/" title="Listedeki en yüksek 10 ögeyi filtrele" rel="noopener">Excel çalışma sayfasında listedeki en yüksek 10 ögeyi filtrele.</a></li>
            <li><a href="/tr/cells/match-all-blank-cells-in-the-list/" title="Listedeki tüm boş hücreleri eşleştir" rel="noopener">Excel çalışma sayfasında listedeki tüm boş hücreleri eşleştir.</a></li>
        </ul>
        <p>Sırala</p>
        <ul>
            <li><a href="/tr/cells/sort-worksheet-data/" title="Çalışma sayfası verilerini sırala" rel="noopener">Excel çalışma sayfasında verileri sırala.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Veri İçe Aktar</p>
        <ul>
            <li><a href="/tr/cells/import/" title="Verileri Excel dosyalarına içe aktar" rel="noopener">Verileri Excel dosyalarına içe aktar.</a></li>
            <li><a href="/tr/cells/import-CSV-data-into-worksheet/" title="CSV verilerini çalışma sayfasına içe aktar" rel="noopener">CSV verilerini Excel çalışma sayfasına içe aktar.</a></li>
            <li><a href="/tr/cells/import/picture/" title="Bir resmi çalışma sayfasına içe aktar" rel="noopener">Bir resmi Excel çalışma sayfasına içe aktar.</a></li>
            <li><a href="/tr/cells/import/double-array/" title="Çift dizi içe aktar" rel="noopener">Çift bir dizi veriyi Excel çalışma sayfasına içe aktar.</a></li>
            <li><a href="/tr/cells/import/integer-array/" title="Tamsayı dizi içe aktar" rel="noopener">Tamsayı bir dizi veriyi Excel çalışma sayfasına içe aktar.</a></li>
            <li><a href="/tr/cells/import/string-array/" title="Dize dizi içe aktar" rel="noopener">Dize bir dizi veriyi Excel çalışma sayfasına içe aktar.</a></li>
            <li><a href="/tr/cells/import/with-using-storage/" title="Depolama kullanarak veri içe aktar" rel="noopener">Depolama kullanarak veriyi Excel çalışma sayfasına içe aktar.</a></li>
            <li><a href="/tr/cells/import/without-using-storage/" title="Depolama kullanmadan veri içe aktar" rel="noopener">Depolama kullanmadan veriyi Excel çalışma sayfasına içe aktar.</a></li>
        </ul>
        <p>Toplu İşlem</p>
        <ul>
            <li><a href="/tr/cells/assembly/" title="Excel dosyalarında verileri topla" rel="noopener">Excel dosyalarında verileri topla.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>Yorumlar</p>
        <ul>
            <li><a href="/tr/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="Hücreye bir yorum ekle" rel="noopener">Excel çalışma sayfasındaki bir hücreye bir yorum ekle.</a></li>
            <li><a href="/tr/cells/update-a-comment-in-excel-workbook/" title="Bir hücre yorumunu güncelle" rel="noopener">Excel çalışma sayfasında bir yorumu güncelle.</a></li>
            <li><a href="/tr/cells/delete-all-comments-in-a-worksheet/" title="Çalışma sayfasındaki tüm yorumları sil" rel="noopener">Excel çalışma sayfasındaki tüm yorumları sil.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Değişiklikler</p>
        <ul>
            <li><a href="/tr/cells/protect-excel-workbooks/" title="Bir Excel çalışma kitabını koru" rel="noopener">Bir Excel çalışma kitabını koru.</a></li>
            <li><a href="/tr/cells/unprotect-excel-workbooks/" title="Bir Excel çalışma kitabının korumasını kaldır" rel="noopener">Bir Excel çalışma kitabının korumasını kaldır.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>Pencereler</p>
        <ul>
            <li><a href="/tr/cells/freeze-panes-in-excel-worksheet/" title="Çalışma sayfasında paneleri dondur" rel="noopener">Excel çalışma sayfasında paneleri dondur.</a></li>
            <li><a href="/tr/cells/unfreeze-panes-in-excel-worksheet/" title="Çalışma sayfasındaki panelerin dondurulmasını kaldır" rel="noopener">Excel çalışma sayfasındaki panelerin dondurulmasını kaldır.</a></li>
            <li><a href="/tr/cells/hide-excel-worksheets/" title="Çalışma sayfasını gizle" rel="noopener">Bir Excel çalışma sayfasını gizle.</a></li>
            <li><a href="/tr/cells/unhide-excel-worksheets/" title="Çalışma sayfasının gizliliğini kaldır" rel="noopener">Bir Excel çalışma sayfasının gizliliğini kaldır.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Yakınlaştırma</p>
        <ul>
            <li><a href="/tr/cells/set-zoom-in-excel-worksheet/" title="Çalışma sayfası yakınlaştırma düzeyini ayarla" rel="noopener">Excel çalışma sayfasında yakınlaştırmayı ayarla.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}
---