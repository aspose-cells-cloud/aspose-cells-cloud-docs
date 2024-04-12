---
title: Json verilerini Excel'e aktarın
second_title: Aspose.Cells Cloud Documen
linktitle: Jso'yu içe aktar
type: docs
url: /tr/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API, dize dizisi verilerinin Excel dosyalarına aktarılmasını destekler. SDK çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 40
---
Bu REST API `import json data`'i Excel çalışma sayfasına dönüştürün.


## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Önemli parametreler aşağıdaki tabloda açıklanmıştır:


**ImportStringArrayOption**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| isim| sicim| Çalışma kitabı adı|
| importJsonRequest| sınıf| Json isteğini içe aktarın.|
| şifre| sicim| Çalışma kitabının şifresi.|
| dosya| sicim|Orijinal çalışma kitabı klasörü.|
| depolamaAdı| sicim| Depolama adı.|
| çıkış yolu| sicim| Çıkış dosyası yolu.|
| outStorageName| sicim| Çıkış dosyası için depolama adı.|
| checkExcelKısıtlaması| sicim| Excel kısıtlamasını kontrol edin.|


**Örnek**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## Bulut SDK Ailesi

 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:





