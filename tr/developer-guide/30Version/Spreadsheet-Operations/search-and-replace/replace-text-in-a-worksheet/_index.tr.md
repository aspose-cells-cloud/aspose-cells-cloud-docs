---
title: "Excel Çalışma Sayfasında Metin Değiştirme – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Çalışma sayfasında değiştir"
type: docs
url: /tr/worksheets/replace-text/
aliases: [  /tr/replace-text-in-a-workbook/ ]
keywords: "Aspose.Cells, metin değiştir, Excel, REST API, elektronik tablo, çalışma sayfası"
description: "Aspose.Cells Cloud API’sini (v3.0) kullanarak Excel çalışma sayfasında metin nasıl değiştireceğinizi öğrenin. Gereksinimler, kimlik doğrulama, istek sözdizimi, cURL örneği, SDK kod örnekleri, yanıt detayları ve hata işleme içerir."
ArticleTitle: "Excel Çalışma Sayfasında Metin Değiştirme – Aspose.Cells Cloud API"
weight: 70
---

Bu REST API, Excel çalışma sayfasındaki metni **Aspose.Cells metin değiştirme API’si** ile değiştirir.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```

### İstek Parametreleri

| Parametre Adı   | Tür     | Konum  | Açıklama                            |
| ---------------- | ------- | ------ | ----------------------------------- |
| **name**         | string  | path   | Excel çalışma kitabının adı.        |
| **sheetName**    | string  | path   | Çalışma sayfasının adı.             |
| **oldValue**     | string  | query  | Değiştirilecek metin.               |
| **newValue**     | string  | query  | Yeni metin.                         |
| **folder**       | string  | query  | Dosyayı içeren klasör.              |
| **storageName**  | string  | query  | Depolama hizmetinin adı.            |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200,
      "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "CSV Olarak İndir",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "HTML Olarak İndir",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ODS Olarak İndir",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "PDF Olarak İndir",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Tablo Ayırıcı Metin Biçimi Olarak İndir",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "TIFF Olarak İndir",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Microsoft Excel 2003 Olarak İndir",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Microsoft Excel 2007 Olarak İndir",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "XPS Olarak İndir",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                 |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.             |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                    |

## SDK’lar ile PostWorksheetTextReplace API Nasıl Kullanılır?

### PostWorksheetTextReplace API Özellikleri

[OpenAPI Özellikleri](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace), bu genel erişilebilir arayüzü tanımlar.

Hizmeti çağırmak için cURL komut satırı aracını kullanabilirsiniz:

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/replaceText?oldValue=b&newValue=b11" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 0,
  "Worksheet": {
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, düşük seviye detayları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}