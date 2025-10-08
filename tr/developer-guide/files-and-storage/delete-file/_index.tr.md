---
title: Dosyayı Sil - Excel AP
second_title: Documen
linktitle: Dosyayı Sil
type: docs
url: /tr/delete-file/
keywords: Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usag
description: Aspose.Cells API'i kullanarak Excel'deki dosyaların nasıl silineceğini öğrenin. Bu kılavuz, deleteFile API uç noktası, istek parametreleri ve yanıt yapısı hakkında ayrıntılı bilgi sağlar.
weight: 100
kwords: Dosyayı sil, Excel API, REST API, Office Bulut, Elektronik tablo yönetimi, Dosya silme, Bulut depolama, API usag
---
## **Excel API : Dosyayı Sil**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **İşlev Açıklaması**

 The**Dosyayı sil** API, kullanıcıların belirtilen dosyaları bulut depolama alanından kaldırmasına olanak tanır ve böylece kaynakların ve verilerin verimli bir şekilde yönetilmesini sağlar.

###  İstek parametreleri**Dosyayı sil** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
|yol|Sicim|Yol|Silinmesi gereken dosyanın yolu.|
|depolamaAdı|Sicim|Sorgu|Dosyanın bulunduğu depolama alanının adı. Varsayılan depolama alanı kullanılıyorsa isteğe bağlıdır.|
|sürüm kimliği|Sicim|Sorgu|Silinecek dosyanın sürüm kimliği (varsa).|

### **Yanıt Açıklaması**

```json
{
Void
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntıları yöneterek proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:
