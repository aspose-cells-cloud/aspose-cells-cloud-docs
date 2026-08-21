---
title: "Excel AutoFilter ile Çalışma"
second_title: "Belge"
linktitle: "AutoFilter"
type: docs
url: /tr/autofilter/
aliases: [  /tr/working-with-autofilter/ ]
keywords: "AutoFilter, Aspose.Cells Cloud, Excel filtresi, renk filtresi, tarih filtresi, dinamik filtre, sayı filtresi, metin filtresi, boşluk filtresi, özel filtre"
description: "Aspose.Cells Cloud API'lerini kullanarak Excel AutoFilter'ları (renk, tarih, dinamik, sayı, metin, boşluk) ekleme, düzenleme ve silme yöntemlerini öğrenin. Birden fazla programlama dilinde kod örnekleri."
weight: 100
ArticleTitle: "Excel AutoFilter ile Çalışma – Aspose.Cells Cloud Belgeleri"
---

AutoFilter, bir çalışma sayfasından yalnızca ihtiyacınız olan öğeleri görüntülemenin en hızlı yoludur. AutoFilter özelliği, kullanıcıların belirli kriterlere göre (metin, sayı veya tarihe göre) bir listeyi filtrelemesini sağlar.

**Farklı Filtre Türleri**

Aspose.Cells Cloud, Renk Filtresi, Tarih Filtresi, Sayı Filtresi, Metin Filtresi, Boşluk Filtresi ve Boş Olmayan Filtre gibi çeşitli filtre türlerini uygulamak için birden fazla API sağlar.

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>Dolu Renk</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud, hücrelerin dolgu rengi özelliğine göre veri filtrelemek için <a href="/cells/autofilter/add-color-filter/">Dolu Renk Filtresi Ekle API’sini</a> sunar.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Tarih</strong></td>
    <td class="col-md-10">
      <p>Ocak 2018 tarihli satırları filtrelemek gibi çeşitli tarih filtreleri uygulanabilir. Tarih filtresi eklemek için <a href="/cells/autofilter/add-date-filter/">Tarih Filtresi Ekle API’sini</a> kullanın.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Dinamik Tarih</strong></td>
    <td class="col-md-10">
      <p>Dinamik tarih filtreleri, yıl fark etmeksizin belirli bir aydaki hücreleri filtrelemenizi sağlar (örneğin, tüm Ocak tarihleri). <a href="/cells/autofilter/add-dynamic-filter/">Dinamik Filtre API’sine</a> bakın.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Sayı</strong></td>
    <td class="col-md-10">
      <p><a href="/cells/autofilter/add-filter/">Özel Filtreler API’si</a>, sayısal değerleri belirli bir aralıkta olan hücreleri filtrelemenizi sağlar.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Metin</strong></td>
      <td class="col-md-10">
      <p>Bir sütun metin içeriyorsa, belirli bir diziyi içeren hücreleri seçmek için <a href="/cells/autofilter/add-filter/">Filtre Ekle API’sini</a> kullanabilirsiniz.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Boşluklar</strong></td>
    <td class="col-md-10">
      <p>Bir sütunun boş olduğu satırları almak için <a href="/cells/autofilter/match-all-blank/">Tüm Boş Hücreleri Eşle API’sini</a> kullanın.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Boş Olmayanlar</strong></td>
    <td class="col-md-10">
      <p>Bir sütunun boş olmayan herhangi bir değeri içeren satırları filtrelemek için <a href="/cells/autofilter/match-all-non-blank/">Tüm Boş Olmayan Hücreleri Eşle API’sini</a> kullanın.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Özel Filtre</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud, belirli bir alt diziyi içeren satırları filtrelemek veya belirli bir diziyle başlayan/biten satırları filtrelemek gibi gelişmiş senaryolar için <a href="/cells/autofilter/add-custom-filter/">Özel Filtreler API’sini</a> sunar.</p>
    </td>
  </tr>
</table>

**AutoFilter İşlemleri**

- [Excel çalışma sayfasına nasıl renk filtresi eklenir?](/cells/autofilter/add-color-filter/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/add-color-filter/`
- [Excel çalışma sayfasına nasıl özel filtre eklenir?](/cells/autofilter/add-custom-filter/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/add-custom-filter/`
- [Excel çalışma sayfasına nasıl tarih filtresi eklenir?](/cells/autofilter/add-date-filter/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/add-date-filter/`
- [Excel çalışma sayfasına nasıl dinamik filtre eklenir?](/cells/autofilter/add-dynamic-filter/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/add-dynamic-filter/`
- [Excel çalışma sayfasına nasıl filtre eklenir?](/cells/autofilter/add-filter/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/add-filter/`
- [Excel çalışma sayfasına nasıl simge filtresi eklenir?](/cells/autofilter/add-icon-filter/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/add-icon-filter/`
- [Excel çalışma sayfasından nasıl tarih filtresi silinir?](/cells/autofilter/delete-a-date-filter/) – **Yöntem:** DELETE, **Uç Nokta:** `/cells/autofilter/delete-a-date-filter/`
- [Excel çalışma sayfasından nasıl filtre silinir?](/cells/delete-filter/) – **Yöntem:** DELETE, **Uç Nokta:** `/cells/delete-filter/`
- [Excel çalışma sayfasından AutoFilter açıklaması nasıl alınır?](/cells/autofilter/get/) – **Yöntem:** GET, **Uç Nokta:** `/cells/autofilter/get/`
- [Excel çalışma sayfasında tüm boş hücreler nasıl eşleştirilir?](/cells/autofilter/match-all-blank/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/match-all-blank/`
- [Excel çalışma sayfasında tüm boş olmayan hücreler nasıl eşleştirilir?](/cells/autofilter/match-all-non-blank/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/match-all-non-blank/`
- [Excel çalışma sayfasında AutoFilter nasıl yenilenir?](/cells/autofilter/refresh/) – **Yöntem:** POST, **Uç Nokta:** `/cells/autofilter/refresh/`
---