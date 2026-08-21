---
title: "Excel Aralıklarıyla Çalışma"
second_title: "Belge"
linktype: "aralık"
type: docs
url: /tr/ranges/
aliases: [  /tr/working-with-ranges/ ]
keywords: "Aspose.Cells, Excel aralığı, REST API, SDK, .NET, Java, Python, hücre birleştirme, aralık kopyalama, aralık değeri ayarlama"
description: "Aspose.Cells Cloud REST API ile Excel aralıklarını nasıl alacağınızı, değiştireceğinizi, stillendireceğinizi, birleştireceğinizi, taşıyacağınızı ve kopyalayacağınızı öğrenin. .NET, Java, Python ve diğerleri için SDK kod örnekleri içerir."
weight: 100
ArticleTitle: "Excel Aralıklarıyla Çalışma – Aspose.Cells Cloud Belgelendirmesi"
---

Bir **aralık**, tek bir hücreyi, tüm bir satırı, tüm bir sütunu, bitişik hücre bloğunu veya birden fazla çalışma sayfasını kapsayan üç boyutlu (3‑D) bir aralığı temsil eder.

## Bir Excel dosyasında aralıklarla çalışma

Aspose.Cells Cloud REST API'si, her aralık işlemi için özel uç noktalar sağlar. Aşağıdaki liste, ayrıntılı kullanım örneklerine bağlantılar içerir ve hızlı referans için ilgili HTTP yöntemini ve uç noktayı belirtir.

- [Çalışma Kitabındaki Adlandırılmış Aralıkları Al](/cells/get-named-ranges-inside-the-workbook/) – Bir çalışma kitabında tanımlı olan tüm adlandırılmış aralıkları alır, bu aralıkların adreslerini ve kapsama alanını döndürür. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [Adlandırılmış Aralığa Göre Hücre Verilerini Al](/cells/get-cells-data-based-on-named-range/) – Belirli bir adlandırılmış aralığa ait hücrelerin değerlerini döndürür. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [Aralıktaki Satırların Yüksekliklerini Değiştir](/cells/cells/change-heights-of-rows-inside-the-range/) – Verilen aralık içinde yer alan her satırın yüksekliğini ayarlar. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [Aralıktaki Sütunların Genişliklerini Değiştir](/cells/cells/change-widths-of-columns-inside-the-range/) – Aralığı kesen tüm sütunların genişliğini değiştirir. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [Hücre Aralığını Tek Bir Hücreye Birleştir](/cells/combines-a-range-of-cells-into-a-single-cell/) – Seçilen hücreleri birleştirerek tek bir hücre oluşturur ve sol‑üst hücre değerini korur. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [Yapıştırma Seçenekleriyle Çalışma Sayfasında Aralık Kopyala](/cells/copy-range-in-a-worksheet-with-paste-options/) – Kaynak aralığı, isteğe bağlı yapıştırma türlerine (değerler, biçimler, formüller vb.) göre hedef aralığa kopyalar. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [Aralığın Stilini Ayarla](/cells/set-the-style-of-the-range/) – Aralıktaki tüm hücrelere yazı tipi, dolgu, kenarlık ve hizalama stillerini uygular. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [Aralığın Birleştirilmiş Hücrelerini Ayır](/cells/unmerge-merged-cells-of-the-range/) – Önceki bir birleştirme işlemini tersine çevirir ve orijinal bireysel hücreleri geri yükler. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Bir Excel Çalışma Sayfası ile Adlandırılmış Aralığı Taşı](/cells/move-a-named-ranged-with-a-excel-worksheet/) – Bir adlandırılmış aralığı aynı çalışma sayfası içinde yeni bir adrese veya başka bir çalışma sayfasına taşır. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Excel Çalışma Sayfasında Aralık Değeri Ayarla](/cells/ranges/set-value/) – Belirtilen aralığa tek bir değer veya değer dizisi yazar. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

Tüm istekler ve yanıtlar JSON formatındadır. Kimlik doğrulama için `Authorization` başlığını erişim jetonunuzla birlikte ekleyin.