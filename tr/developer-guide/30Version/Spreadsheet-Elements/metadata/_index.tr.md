---
title: "Excel Meta Veri ve Özellikleri ile Çalışma"
second_title: "Belge"
linktype: "Meta Veri ve Özellikler"
type: docs
url: /tr/metadata/
aliases:
  - /belge-ozellikleri/
  - /belge-ozellikleri-ile-calisma/
keywords: "Aspose.Cells Cloud, Excel meta verisi, belge özellikleri API'si, REST API, meta veri alma, Excel özelliklerini güncelleme, Excel meta verisi silme"
description: "Aspose.Cells Cloud REST API kullanarak Excel dosyası meta verilerini nasıl okuyacağınıza, ekleyeceğinize, güncelleyeceğinize ve sileceğinizi öğrenin. Java, .NET, Python, Node.js ve daha fazlası için cURL ve SDK'larla örnekler içerir."
ArticleTitle: "Excel Meta Verisi ve Belge Özellikleri ile Çalışma – Aspose.Cells Cloud"
weight: 100
---

Excel dosyaları, belgeleri tanımlamak, organize etmek ve yönetmek için yardımcı olan çeşitli meta verileri saklayabilir. Aspose.Cells Cloud, bu meta verileri okumak, eklemek, güncellemek ve silmek için basit bir REST API sunar; böylece geliştiriciler, belge-özelliği yönetimi uygulamalarına entegre edebilir. Bu kılavuz, özelliklerin iki temel kategorisini—standart ve özel—tanımlar, bunlarla nasıl çalışılacağını açıklar ve ilgili API uç noktalarına doğrudan bağlantılar sağlar. Ayrıca uygulamayı hızlandırmak için istek detaylarını içeren özet bir API referans tablosu bulacaksınız.

**Son güncelleme:** 8 Temmuz 2026  

**Belge özellikleri türleri**

Aspose.Cells Cloud API'lerini kullanarak Excel'deki belge özelliklerini (meta verileri) nasıl görüntüleyeceğinizi, değiştireceğinizi ve kaldıracağınızı öğrenmeden önce, bir Excel belgesinin sahip olabileceği özellik türlerini netleştirelim.

- **Standart özellikler**, Excel'e ortaktır. Başlık, Konu, Yazar, Kategori vb. gibi temel bilgileri içerir. Dosyayı daha kolay bulabilmek için bu özelliklere özel metin değerleri atayabilirsiniz.

- **Özel özellikler**, kullanıcı tanımlıdır. Excel belgenize ek meta veri eklemenizi sağlar.

**Excel dosyasında belge özellikleri ile nasıl çalışılır**

- [Depolama kullanarak belirli bir belge özelliğini alma](/cells/document-properties/get/)
- [Depolama kullanmadan belge özelliklerini alma](/cells/metadata/get/)
- [Depolama kullanarak tüm belge özelliklerini alma](/cells/document-properties/get-all/)
- [Depolama kullanarak belirli bir belge özelliğini güncelleme](/cells/document-properties/update/)
- [Depolama kullanmadan belirli bir belge özelliğini güncelleme](/cells/metadata/update/)
- [Depolama kullanarak belirli bir belge özelliğini silme](/cells/document-properties/delete/)
- [Depolama kullanmadan belge özelliklerini silme](/cells/metadata/delete/)
- [Depolama kullanarak tüm belge özelliklerini silme](/cells/document-properties/clear/)

**API referansı (depolama olmadan)**  

| Yöntem | Uç Nokta | Açıklama |
|--------|----------|-------------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | Bulutta saklanan çalışma kitabının tüm belge özelliklerini alır. |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | `propertyName` ile tanımlanan belirli bir özelliğin (standart veya özel) değerini alır. |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Mevcut bir özelliğin değerini günceller. İstek gövdesi yeni değeri JSON formatında içerir. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Çalışma kitabından belirli bir özelliği siler. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | Çalışma kitabından tüm özel ve standart özellikleri temizler. |

*Tüm istekler bir OAuth 2.0 erişim belirteci gerektirir ve belirli bir depolama konumu kullanıldığında `storage` ve `folder` gibi isteğe bağlı sorgu parametreleri içerebilir.*
---