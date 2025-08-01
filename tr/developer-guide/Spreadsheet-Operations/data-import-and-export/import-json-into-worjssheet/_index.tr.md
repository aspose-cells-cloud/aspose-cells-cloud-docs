﻿---
title: Json verilerini Excel'e aktar
second_title: Aspose.Cells Cloud Documen
linktitle: Jso'yu içe aktar
type: docs
url: /tr/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API, dize dizisi verilerini Excel dosyalarına aktarmayı destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir.
weight: 40
kwords: Excel, Office Bulut, REST API, E-tablo, PDF, CSV, Json, Markdown, Json verilerini Excel'e aktar
---
Bu REST API `import json data`'i Excel çalışma sayfasına aktarın.

## RSETAPI

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

**İçe AktarDizeDiziSeçeneği**

|Parametre Adı| Yol/Sorgu Dizesi/HTTPGövdesi|Tip|Tanım|
|:- |:- |:- |:- |
| isim| Yol| sicim| Çalışma kitabı adı|
| JsonRequest'i içe aktar| HTTPGövdesi| sınıf| Json isteğini içe aktar.|
| şifre| Sorgu Dizesi| sicim| Çalışma kitabının şifresi.|
| dosya| Sorgu Dizesi| sicim| Orijinal çalışma kitabı klasörü.|
| depolamaAdı| Sorgu Dizesi| sicim| Depolama adı.|
| çıkış yolu| Sorgu Dizesi| sicim| Çıktı dosya yolu.|
| outDepolamaAdı| Sorgu Dizesi| sicim| Çıktı dosyası için depolama adı.|
| checkExcelRestriction| Sorgu Dizesi| sicim| Excel kısıtlamasını kontrol edin.|

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

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:
