---
title: Fil'i Taşı
second_title: Documen
linktitle: Fil'i Taşı
type: docs
url: /tr/move-file/
keywords: Move file, Aspose.Cells API, File Management, Excel API, REST API, Cloud Storage, Spreadsheet Manipulatio
description: Aspose.Cells bulut depolama alanındaki dosyaları yönetmek için MoveFile API'i nasıl kullanacağınızı öğrenin
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Dosya Taşıma, Dosya Yönetimi, Bulut Depolama
---
## **Excel API: Dosyayı Taşı**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **İşlev Açıklaması**

 The**Dosyayı taşı** API, bir dosyayı Aspose.Cells bulut depolama alanı içinde bir konumdan diğerine taşımanıza olanak tanır. Bu, özellikle dosyaları düzenlemek ve depolama alanını etkili bir şekilde yönetmek için kullanışlıdır.

###  İstek parametreleri**Dosyayı taşı** API

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|---------------|--|------------------------|--------------------------------------|
| srcPath| Sicim| Yol| Taşınacak dosyanın kaynak yolu.|
| hedefYolu| Sicim| Sorgu| Dosyanın taşınacağı hedef yol.|
| srcDepolamaAdı| Sicim| Sorgu| Varsa kaynak depolama adı.|
| hedefDepolamaAdı| Sicim| Sorgu|Uygulanabilirse hedef depolama adı.|
| sürüm kimliği| Sicim| Sorgu| Uygunsa dosyanın sürüm kimliği.|

### **Yanıt Açıklaması**

```json
{
Void
}
```

## OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/MoveFile) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

## Excel API SDK

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:
