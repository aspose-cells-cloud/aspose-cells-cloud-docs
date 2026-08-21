---
title: "Tüm Belge Özelliklerini Al"
second_title: "Belge"
linktitle: "Tümünü al"
type: docs
url: /tr/document-properties/get-all/
aliases: [  /tr/get-all-document-properties/ ]
keywords: "Tüm Belge Özelliklerini Al, Aspose.Cells Cloud, Excel belge özellikleri, REST API, SDK, Excel meta verisi"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel dosyasından tüm belge özelliklerini alın. Uç nokta, desteklenen tüm SDK'lar ve programlama dilleri ile çalışır."
ArticleTitle: "Tüm Belge Özelliklerini Al – Aspose.Cells Cloud API"
weight: 25
---

Bu REST API, belge özelliklerini okur.

## GetDocumentProperties API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı  | Tür    | Konum | Açıklama                         |
| -------------- | ------ | ----- | -------------------------------- |
| name           | string | path  | Excel dosyasının adı.            |
| folder         | string | query | Dosyayı içeren klasör.           |
| storageName    | string | query | Depolama hizmetinin adı.         |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperties), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperties": {
    "DocumentPropertyList": [
      {
        "Name": "Title",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Title",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Subject",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Subject",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Author",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Author",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Keywords",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Keywords",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Comments",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Comments",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LastSavedBy",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedBy",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "CreateTime",
        "Value": "6/5/2015 6:17:20 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/CreateTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LastSavedTime",
        "Value": "9/27/2019 9:09:43 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Category",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Category",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "NameOfApplication",
        "Value": "Microsoft Excel",
        "BuiltIn": "True",
        "link": {
          "Href": "/NameOfApplication",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Version",
        "Value": "16.0300",
        "BuiltIn": "True",
        "link": {
          "Href": "/Version",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Security",
        "Value": "0",
        "BuiltIn": "True",
        "link": {
          "Href": "/Security",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "ScaleCrop",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/ScaleCrop",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Template",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Template",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Manager",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Manager",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Company",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Company",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LinksUpToDate",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/LinksUpToDate",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/documentproperties",
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

**HTTP Durum Kodları**

| Kod  | Anlam                       | Açıklama                                             |
|------|-----------------------------|------------------------------------------------------|
| 200  | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400  | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                   |
| 413  | Payload Too Large (Aşırı Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.               |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                         |

## Bulut SDK Ailesi

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve sizin projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperties.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperties.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperties.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperties.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperties.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperties.go" >}}

{{< /tab >}}

{{< /tabs >}}