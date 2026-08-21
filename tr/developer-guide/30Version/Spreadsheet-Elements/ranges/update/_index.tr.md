---
title: "Excel çalışma sayfasından aralık içeriğini nasıl güncellersiniz"
second_title: "Belge"
linktitle: "Güncelle"
type: docs
url: /tr/ranges/update/
keywords: "Excel, aralık güncelleme, Aspose.Cells Cloud, REST API, elektronik tablo, aralık stili, aralık değerleri, satır yüksekliği, sütun genişliği"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında aralık içeriğini güncelleştirin. Desteklenen SDK'lar aracılığıyla stilleri, değerleri, satır yüksekliklerini ve sütun genişliklerini değiştirin."
weight: 20
ArticleTitle: "Excel çalışma sayfasından aralık içeriğini nasıl güncellersiniz – Aspose.Cells Cloud Belgesi"
---

## Excel çalışma sayfasında aralık içeriğini güncelleme işlemi

Güncelleme işlemlerini kullanmadan önce geçerli bir Aspose.Cells Cloud API belirteciniz olduğunu ve hedef çalışma kitabının bulut depolama alanınızda saklandığından emin olun. API, Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift için SDK'lar aracılığıyla kullanılabilir.

Aşağıda dört temel güncelleme eyleminin kısa bir özeti verilmiştir. Bu tablo, geliştiricilere her işlemin HTTP yöntemini, uç nokta kalıbını, temel parametrelerini ve tipik başarı yanıtını hızlıca referans olarak sunar.

| Eylem           | HTTP Yöntemi | Uç Nokta Kalıbısı                                                                                     | Temel Parametreler            | 200‑OK Yanıtı                 |
|-----------------|-------------|------------------------------------------------------------------------------------------------------|-------------------------------|------------------------------|
| Stil ayarla     | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                      | `style` nesnesi               | Güncellenmiş aralık stili     |
| Değerler ayarla | POST        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                    | `values` dizisi               | Güncellenmiş aralık değerleri |
| Satır yüksekliği| PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                 | `height` sayısı               | Güncellenmiş satır yüksekliği |
| Sütun genişliği | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                               | `width` sayısı                | Güncellenmiş sütun genişliği  |

Bu sayfa, dört temel güncelleme eylemine hızlı erişim sağlar: bir aralığın stilini ayarlamak, bir aralığın değerlerini ayarlamak, satır yüksekliklerini ayarlamak ve sütun genişliklerini ayarlamak.

- [Excel çalışma sayfasında bir aralığın stilini nasıl ayarlayabilirsiniz.](/cells/ranges/update/style/) 
- [Excel çalışma sayfasında bir aralığın değerlerini nasıl ayarlayabilirsiniz.](/cells/ranges/update/values/) 
- [Excel çalışma sayfasında bir aralığın satır yüksekliklerini nasıl ayarlayabilirsiniz.](/cells/ranges/update/row-height/) 
- [Excel çalışma sayfasında bir aralığın sütun genişliklerini nasıl ayarlayabilirsiniz.](/cells/ranges/update/column-width/)