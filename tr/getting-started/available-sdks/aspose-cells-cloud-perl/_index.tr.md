---
title: "Aspose.Cells Cloud SDK for Perl – Dönüştür, Birleştir, Böl, Korumalı Yap ve Daha Fazlası"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud SDK for Perl – Dönüştür, Birleştir, Böl, Korumalı Yap ve Daha Fazlası"
linktitle: "Aspose.Cells Cloud SDK for Perl"
type: docs
url: /tr/available-sdks/aspose-cells-cloud-perl/
description: "Aspose.Cells Cloud Perl SDK’sını keşfedin – Office kurulumuna gerek kalmadan, Excel dosyalarını oluşturmak, dönüştürmek, birleştirmek, bölmek, korumalı hale getirmek, arama yapmak ve değiştirmek için çapraz-platform kütüphane. Kurulum kılavuzunu, kod örneklerini ve API referansını içerir."
weight: 30
keywords: "Perl, Aspose.Cells Cloud, Excel SDK, dönüştürme, PDF, API, Excel işleme, Perl SDK, bulut Excel işleme"
---

_Son güncelleme: 30 Temmuz 2026_

Bu SDK açık kaynaklıdır ve MIT Lisansı altında lisanslanmıştır. Aspose.Cells Cloud için Perl kütüphanesinin kaynak koduna [buradan](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) ulaşabilirsiniz.

# **Aspose.Cells Cloud Perl Kütüphanesi Nasıl Kullanılır**

Aspose.Cells Cloud SDK for Perl, geliştiricilerin Perl programlama diliyle Microsoft Excel dosyalarını işlemesine ve manipüle etmesine olanak tanıyan güçlü bir kütüphanedir. Bu SDK ile yerel makinenize ek yazılım veya bağımlılıklar kurmadan bulutta Excel belgeleri oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, Aspose.Cells Cloud SDK for Perl kullanarak yeni bir Excel çalışma kitabının oluşturulması, hücrelere veri eklenmesi ve değiştirilmiş çalışma kitabının buluta kaydedilmesi gibi yaygın görevleri nasıl gerçekleştireceğinizi inceleyeceğiz.

## Başlangıç

Aspose.Cells Cloud SDK for **Perl**’i kullanmaya başlamadan önce geliştirme ortamınızı kurmanız ve gerekli bağımlılıkları yüklemeniz gerekir. İstemci kimliğiniz ve istemci gizli anahtarınızı almak için Aspose web sitesindeki **[Aspose.Cells Cloud Hızlı Başlangıç Kılavuzu’na](https://docs.aspose.cloud/cells/quickstart/)** bakın.

## Aspose.Cells Cloud için Perl paketi Nasıl Kurulur

**Önkoşullar**  
- Perl 5.10 veya üzeri bir sürüm  
- CPAN (Comprehensive Perl Archive Network) yüklü olmalı  
- Geçerli bir Aspose.Cells Cloud istemci kimliği ve istemci gizli anahtarı  

Aspose.Cells Cloud SDK for Perl’i aşağıdaki komutla kurabilirsiniz:

```perl
perl -MCPAN -e shell
install AsposeCellsCloud::CellsApi
```

## Perl Paketi Kullanılarak Xlsx’in Diğer Biçimlere Dönüştürülmesi

- **Aspose.Cells Cloud Kütüphanesini İçe Aktarın**  
  Projenize Aspose.Cells Cloud Perl SDK’sından gerekli paketi içe aktarmayla başlayın.

- **Kimlik Bilgileriyle API İstemcisi Yapılandırın**  
  API istemcinizi benzersiz istemci kimliğiniz ve istemci gizli anahtarınızla kimlik doğrulaması için yapılandırın.

- **Dönüştürme Parametrelerini Hazırlayın**  
  Dönüştürme görevi için kaynak dosya adı, istenen çıktı formatı ve depolama klasörü yolu gibi parametreleri tanımlayın.

- **Çalışma Kitabı Dönüştürme İşlemini Yürütün**  
  `PostConvertWorkbook` yöntemini çağırarak dönüştürme işlemini başlatın ve yanıtı işleyin.

Aşağıda `PostConvertWorkbook` işlemi için kısa bir referans verilmiştir:

| HTTP Yöntemi | Uç Nokta                                 | Gerekli Parametreler                                 | Örnek İstek (Perl)                                                                                         | Örnek Yanıt (JSON)                                 | Olası Durum Kodları |
|-------------|------------------------------------------|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|-----------------------|
| POST        | `/cells/convert`                         | `file` (kaynak çalışma kitabı), `outputFormat`, `storage`  | ```perl\nmy $result = $api_instance->post_convert_workbook({ file => 'Book1.xlsx', outputFormat => 'pdf', storage => 'MyStorage' });\n``` | `{ "File": "Book1.pdf", "Url": "https://.../Book1.pdf" }` | 200 OK, 400 Bad Request, 401 Unauthorized, 500 Server Error |

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}