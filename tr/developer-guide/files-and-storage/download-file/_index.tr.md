---
title: "Aspose.Cells Cloud Dosya İndirme API'si – Bulutta Hızlı Dosya İndirme Arayüzü"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud Dosya İndirme API'si – Bulutta Hızlı Dosya İndirme Arayüzü"
linktitle: "Dosya İndirme API'si"
type: docs
url: /download-file/
keywords: "Aspose.Cells, Dosya İndirme API'si, Excel bulut depolama, REST API, dosya indirme, PDF, CSV, SDK"
description: "Aspose.Cells Cloud depolama alanından Excel, PDF, CSV ve diğer dosyaları Download File API'si (v4.0) ile indirin. Endpoint, parametreler, kimlik doğrulama detayları ve kod örnekleri içerir."
weight: 100
---

**DownloadFile** API, Aspose.Cells Cloud depolama alanında saklanan dosyaları almanızı sağlar. Dosya İndirme API'si, Excel elektronik tablolarını, PDF’leri, CSV’leri ve diğer desteklenen formatları doğrudan buluttan erişmek için önemlidir.

## **Excel API: Dosya İndirme**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **DownloadFile** API istek parametreleri

| Parametre Adı | Tür   | Konum (Yol / Sorgu) | Açıklama                                                          |
|---------------|-------|---------------------|-------------------------------------------------------------------|
| path          | String | Yol                 | İndirmek istediğiniz dosyanın sanal yolu.                        |
| storageName   | String | Sorgu               | Dosyanın hangi depodan alınacağına ilişkin depo adı.            |
| versionId     | String | Sorgu               | İndirilecek dosyanın sürüm tanımlayıcısı (geçerliysa).          |

### **Yanıt**

API, bir **ikili dosya akışı** döndürür. `Content-Type` başlığı dosya formatıyla eşleşir (örneğin, XLSX için `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet`). JSON yükü döndürülmez.

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                       |
|-----|-----------------------|----------------------------------------------------------------|
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.   |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz) | Geçersiz veya eksik JWT belirteci.                             |
| 413 | Payload Too Large (Yük Çok Büyük) | Yüklenen dosya boyut sınırlamasını aşıyor.                    |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                    |

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/DownloadFile), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine farklı SDK’lar kullanılarak nasıl çağrı yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}