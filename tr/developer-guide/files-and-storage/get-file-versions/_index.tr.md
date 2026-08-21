---
title: "Aspose.Cells Cloud Dosya Sürümleri API’si – Dosya Sürüm Geçmişini Hızlı Çekme"
second_title: "Belge"
ArticleTitle: "Bulut Tabanlı Excel Yönetimi – Aspose.Cells Cloud’da Dosya Sürüm Geçmişini Hızlı Çekme"
linktitle: "Dosya Sürümlerini Al"
type: docs
url: /tr/get-file-versions/
keywords: "Aspose Cells API, dosya sürümleri, elektronik tablo sürümleme, bulut depolama API’si, REST, Excel dosyası geçmişi"
description: "Aspose.Cells Cloud’da depolanan herhangi bir Excel dosyasının sürüm geçmişi listesini tam olarak alın. Depolama seçimi, kimlik doğrulama ve detaylı hata kodlarını destekler."
weight: 100
---

Aspose.Cells Cloud’da depolanan belirli bir elektronik tablonun sürüm kayıtlarının tam listesini çekin. Bu uç nokta, geliştiricilerin değişiklikleri takip etmesine, düzenlemeleri denetlemesine ve bulut depolama üzerinden doğrudan sürüm kontrolü iş akışlarını uygulamasına olanak tanır.

**GetFileVersions** API’si, Aspose.Cells Cloud’da depolanan belirli bir elektronik tablonun tüm sürüm kayıtlarını döndürür. Her dosya için tüm değişiklik geçmişini tutmanıza yardımcı olur.

## **Excel API’si: Dosya Sürümlerini Al**

### Web API’si

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **GetFileVersions** API’sinin istek parametreleri şunlardır:

| Parametre Adı | Tür   | Konum | Açıklama                                                                                      |
| ------------- | ----- | ----- | --------------------------------------------------------------------------------------------- |
| `path`        | Dize  | Yol   | **Zorunludur.** Sürümleri çekilecek dosyanın tam yolu.                                         |
| `storageName` | Dize  | Sorgu | İsteğe bağlı. Dosyayı içeren depolamanın adı. Atlanırsa varsayılan depo kullanılır.            |

### **Yanıt**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Belirtilen belge için dosya sürümleri listesini içerir."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["Dosya sürümü detaylarının bir koleksiyonu."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

Başarılı durumda, API yukarıda gösterildiği gibi `Value` dosya sürümü nesneleri dizisini içeren JSON yüküyle **HTTP 200 OK** döndürür.

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.      |
| 400 | Hatalı İstek          | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413 | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                        |

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions), web tarayıcısından doğrudan REST etkileşimlerini gerçekleştirmek için kapsamlı bir programlama arayüzü sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanımı, düşük seviyeli karmaşıklıkları soyutlayarak geliştiricilerin temel işlevselliklere odaklanmasını sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli programlama dillerinde Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}