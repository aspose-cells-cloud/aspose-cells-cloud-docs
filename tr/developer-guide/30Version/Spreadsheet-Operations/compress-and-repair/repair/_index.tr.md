---
title: "Excel Dosyalarını Onar"
second_title: "Belge"
type: docs
linktitle: "Excel Dosyalarını Onar"
url: /repair-excel-files/
keywords: "Aspose Cells, Excel onarım API'si, bozuk XLSX, elektronik tablo kurtarma, bulut API'si"
description: "Aspose.Cells Cloud REST API'sini kullanarak bozuk Excel dosyalarını (XLS, XLSX, XLSM, XLSB, ODS) onarın. Bir veya daha fazla dosya yükleyin, çıktı formatını seçin ve onarılmış dosyaları Base64 olarak alın. Kurulum gerektirmez."
weight: 39
---

Bu REST API, Excel dosyalarını **onarmanıza** olanak tanır.

- XLS, XLSX, XLSM, XLSB, ODS ve diğer elektronik tablo formatlarını onarın.  
- Tek bir istekte birden fazla dosya yüklemeyi destekler.

Aspose.Cells Cloud Excel Onarımı, herhangi bir kurulum gerektirmeden bozuk Excel dosyalarından verileri çevrimiçi olarak kurtarır. Bozuk Excel dosyaları açılamadığı için sorunlidir. Bu tür dosyalardan veri kurtarmak için Aspose.Cells Cloud Excel Onarım uygulamasını deneyebilirsiniz.

## REST API

**Excel Dosyalarını Onar** uç noktası, bozuk elektronik tablo dosyalarını onarır ve onarılmış içeriği döndürür.


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Konum                        | Açıklama                    |
|---------------|--------|------------------------------|-----------------------------|
| file          | file   | formData (multipart)         | Yüklenecek dosya            |
| format        | string | query                        | İstenen çıktı formatı. Atlanırsa (null), çıktı formatı varsayılan olarak giriş dosyasının formatıyla aynı olur. |

### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[birleştirilmiş dosya adı]",
    "Filesize" : [dosya boyutu],
    "FileContent" : "[Base64Dizisi]"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

## SDK’lar ile PostRepair API’sini Nasıl Kullanılır

### PostRepair API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/LightCells/PostRepair), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istekte bulunulacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt belirteci>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64Dizisi--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64Dizisi--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

Başarılı olduğunda hizmet, `Files` dizisini içeren JSON yüküyle HTTP 200 döndürür. Hata durumlarında API standart HTTP durum kodlarını kullanır:

- **400 Bad Request (Hatalı İstek)** – Geçersiz parametreler veya onarılamaz dosya.  
- **401 Unauthorized (Yetkisiz)** – Eksik veya geçersiz JWT belirteci.  
- **413 Payload Too Large (Çok Büyük Yük)** – Yüklenen dosya izin verilen boyutu aşıyor.  
- **500 Internal Server Error (İç Sunucu Hatası)** – Beklenmeyen sunucu tarafı arızası.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en çok artıracak en iyi yoldur. Bir SDK, düşük seviye detayları işler ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}
---