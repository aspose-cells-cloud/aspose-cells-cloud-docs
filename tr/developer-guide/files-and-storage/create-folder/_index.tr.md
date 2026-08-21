---
title: "Klasör Oluştur – Aspose.Cells Cloud API | Excel Depolama Yönetimi"
second_title: "Belge"
ArticleTitle: "Klasör Oluştur – Aspose.Cells Cloud API"
linktitle: "Klasör Oluştur"
type: docs
url: /tr/create-folder/
keywords: "Aspose.Cells, Cloud API, Klasör Oluştur, Depolama Yönetimi, Excel"
description: "Aspose.Cells Cloud deposunda basit bir PUT isteği ile yeni bir klasör oluşturun. İstek formatını, parametrelerini, yanıt ve hata işleme yöntemlerini görün."
weight: 100
---

**createFolder** işlemi, Excel API tarafından kullanılan bulut deposunda belirtilen konumda yeni bir klasör oluşturur. Bu işlem, dosyaları düzenlemek ve yapılandırılmış bir dizin hiyerarşisi korumak için önemlidir.

## **Excel API: Klasör Oluştur**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamaya</a> ihtiyaç duyar.

### **createFolder** API’sinin istek parametreleri

| Parametre Adı | Tür     | Konum | Gerekli | Varsayılan | Açıklama                                                           |
| ------------- | ------- | ----- | ------- | ---------- | ------------------------------------------------------------------ |
| `path`        | String  | Yol   | Evet    | –          | Oluşturulacak klasör yolu (örneğin, `myFolder/subFolder`).        |
| `storageName` | String  | Sorgu | Hayır   | –          | Kullanılacak depo adı. Atlanırsa varsayılan depo uygulanır.       |

### Yanıt Açıklaması

```json
{}
```

İşlem, başarı durumunda içerik döndürmez. Tipik HTTP durum kodları:

**HTTP Durum Kodları**

| HTTP Kodu | HTTP Durumu           | Açıklama                                                                |
| --------- | --------------------- | ----------------------------------------------------------------------- |
| 200       | OK (Tamam)            | Web API başarıyla çağrıldı; yanıt işlem ayrıntılarını içerir.         |
| 400       | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401       | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                                     |
| 413       | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.                                 |
| 500       | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                            |

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine çeşitli SDK’lar kullanılarak nasıl istek atılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}