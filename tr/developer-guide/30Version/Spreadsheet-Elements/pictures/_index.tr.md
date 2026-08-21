---
title: "Excel resimleriyle çalışma"
second_title: "Belge"
linktitle: "Resimler"
type: docs
url: /pictures/
aliases: [/working-with-pictures/]
keywords: "Excel, resim, Aspose.Cells Cloud, REST API, resim işleme, Excel resimleri"
description: "Aspose.Cells Cloud REST API kullanarak Excel çalışma sayfalarında resimleri nasıl alacağınızı, ekleyeceğinizi, güncelleyeceğinizi ve sileceğinizi öğrenin. C#, Java, Python ve daha fazlası için kod örneklerini içerir."
weight: 100
ArticleTitle: "Excel resimleriyle çalışma – Aspose.Cells Cloud Dokümantasyonu"
---

## Excel dosyasında resimlerle çalışma

Bu kılavuz, Aspose.Cells Cloud REST API aracılığıyla Excel çalışma sayfalarındaki **resimlerle** (aynı zamanda görüntü olarak da bilinir) nasıl çalışılacağını açıklar. Excel resimlerini alma, ekleme, güncelleme ve silme gibi temel resimle ilgili işlemleri kapsar ve her görev için ayrıntılı örnekleri gösterir.

**Ön gereksinimler**: Aspose.Cells Cloud hesabı, geçerli bir API anahtarı ve seçtiğiniz dil için uygun SDK'nın kurulmuş olması.

- [Excel çalışma sayfasından belirli bir biçimde resim alma.](/cells/pictures/get/) – Bir çalışma sayfasından istenen biçimde (PNG, JPEG vb.) tek bir resim alın.  
- [Excel çalışma sayfasından tüm resim bilgilerini alma.](/cells/pictures/get-all/) | Bir çalışma sayfasında yer alan her resmin meta verilerini listeleyin.  
- [Excel çalışma sayfasına resim ekleme.](/cells/pictures/add/) – Yeni bir resmi çalışma sayfasına ekleyin; konumunu ve boyutunu belirtin.  
- [Excel çalışma sayfasından belirli bir resmi güncelleme.](/cells/pictures/update/) – Mevcut bir resmin özelliklerini (örn. boyutlar, yerleştirme) değiştirin.  
- [Excel çalışma sayfasından tüm resimleri silme.](/cells/pictures/clear/) – Bir çağrıda bir çalışma sayfasından tüm resim nesnelerini kaldırın.  
- [Excel çalışma sayfasından bir resmi silme.](/cells/pictures/delete/) – Dizine göre belirlenen tek bir resmi silin.  

**API referansı**

**Belirli bir biçimde resim alma**  

| HTTP Yöntemi | Uç Nokta | Gerekli Parametreler | Örnek İstek | Örnek Yanıt | Durum Kodları |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path), `format` (query) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | İkili resim verisi (PNG, JPEG vb.) | 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Server Error |

**Tüm resim bilgilerini alma**  

| HTTP Yöntemi | Uç Nokta | Gerekli Parametreler | Örnek İstek | Örnek Yanıt | Durum Kodları |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | JSON dizisi (resim meta verileri: dizin, ad, konum, boyut) | 200 OK, 400, 401, 404, 500 |

**Resim ekleme**  

| HTTP Yöntemi | Uç Nokta | Gerekli Parametreler | Örnek İstek Gövdesi | Örnek Yanıt | Durum Kodları |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `{ "image": "<base64‑kodlanmış‑resim>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Created, 400, 401, 404, 500 |

**Resim güncelleme**  

| HTTP Yöntemi | Uç Nokta | Gerekli Parametreler | Örnek İstek Gövdesi | Örnek Yanıt | Durum Kodları |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**Tüm resimleri silme**  

| HTTP Yöntemi | Uç Nokta | Gerekli Parametreler | Örnek İstek | Örnek Yanıt | Durum Kodları |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK, 400, 401, 404, 500 |

**Belirli bir resmi silme**  

| HTTP Yöntemi | Uç Nokta | Gerekli Parametreler | Örnek İstek | Örnek Yanıt | Durum Kodları |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK, 400, 401, 404, 500 |

**İlgili konular**

Aspose.Cells Cloud'da diğer resimle ilgili işlemleri inceleyin:  
- [Şekillerle Çalışma](/cells/shapes/) – çizim şekilleri ekleme, düzenleme ve silme.  
- [Grafiklerle Çalışma](/cells/charts/) – grafik nesneleri oluşturma ve işlem yapma.  
- [Çalışma Sayfalarında Resimlerle Çalışma](/cells/images/) – ham resim dosyalarını yerleştirme ve yönetme.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Excel resimleriyle çalışma – Aspose.Cells Cloud Dokümantasyonu",
  "description": "Aspose.Cells Cloud REST API aracılığıyla Excel resimlerini alma, ekleme, güncelleme ve silme kılavuzu.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "Excel resimleri, Aspose.Cells Cloud, REST API, resim işleme",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>