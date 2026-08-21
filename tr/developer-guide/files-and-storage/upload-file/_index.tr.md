---
title: "Aspose.Cells Cloud Dosya Yükleme API’si – Bulutta Dosyaları Hızlı Yükleme İçin Bir Arayüz"
secondtitle: "Belge"
ArticleTitle: "Aspose.Cells Cloud Dosya Yükleme API’si – Bulutta Dosyaları Hızlı Yükleme İçin Bir Arayüz"
linktitle: "Dosya Yükle"
type: docs
url: /upload-file/
keywords: "Aspose.Cells, dosya yükleme, Excel API, bulut depolama, REST API"
description: "Aspose.Cells Cloud API ile dosya yükleme kılavuzu, istek parametrelerini, HTTP durum kodlarını, hata işleme yöntemlerini ve kod örneklerini kapsar."
weight: 100
---

**uploadFile** API’si, geliştiricilerin dosyaları doğrudan Aspose Cells ile işlenecek şekilde bulut depolama alanına yüklemesini sağlar.

## **Aspose Cells API: Dosya Yükleme**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **uploadFile** API’sinin istek parametreleri şunlardır:

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                      |
| :------------- | :----- | :-------------------------- | :-------------------------------------------------------------------------------------------- |
| UploadFiles    | Dosya  | FormData                    | Dosyaları bulut depolama alanına yükleyin.                                                    |
| path           | Dize   | Yol                         | Bulut depolama içindeki hedef yol. Dosyanın yükleneceği yolu belirtin.                         |
| storageName    | Dize   | Sorgu                       | Dosyanın yükleneceği depolama alanının adı.                                                   |

### **Yanıt**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["Dosya yükleme sonucu"],
  "Type": "Sınıf",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["Yüklenen dosya adlarının listesi"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Kapsayıcı",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["Hata listesi."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Kapsayıcı",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Sınıf",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

API aşağıdaki HTTP durum kodlarını döndürür:

| Durum Kodu                    | Açıklama                                            |
| ----------------------------- | --------------------------------------------------- |
| **200 OK**                    | Dosya başarıyla yüklendi.                           |
| **400 Bad Request**           | Geçersiz parametreler veya bozuk istek.             |
| **401 Unauthorized**          | Eksik veya geçersiz kimlik doğrulama belirteci.     |
| **403 Forbidden**             | Belirtilen depolama için yetersiz izinler.          |
| **500 Internal Server Error** | Beklenmeyen sunucu hatası.                          |

## upload file API’sini SDK’larla Nasıl Kullanılır?

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/UploadFile), API’nin ayrıntılı açıklamasını sağlar ve geliştiricilerin doğrudan bir web tarayıcısı üzerinden API ile etkileşime girmesini sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, düşük seviye ayrıntıları yöneterek geliştiricilerin proje görevlerine odaklanmasını sağlar ve geliştirme verimliliğini artırır. Aspose.Cells Cloud SDK’larının kapsamlı listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**Ayrıca bakınız**

- [Dosya İndirme API’si](/download-file/) – Bulut depolamadan bir dosya alın.
- [Dosya Kopyalama API’si](/copy-file/) – Bulut depolama içinde bir dosyayı kopyalayın.
- [Dosya Silme API’si](/delete-file/) – Bulut depolamadan bir dosyayı silin.