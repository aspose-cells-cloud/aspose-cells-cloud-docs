---
title: "Birden Fazla Excel Dosyasını Tek Bir Çalışma Kitabına Birleştir"
second_title: "Belge"
linktitle: "Birden Fazla Excel Dosyasını Birleştir"
type: docs
url: /merge-multi-files-into-excel/
aliases: [/merge/multi-files/]
keywords: "Aspose.Cells Cloud, birden fazla Excel dosyasını birleştir, REST API, elektronik tablo birleştirme, bulut SDK'sı"
description: "Aspose.Cells Cloud REST API’sini (v3.0) kullanarak birden fazla Excel çalışma kitabını tek bir dosyada birleştirmeyi öğrenin. HTTPS uç noktası, cURL komutu, SDK örnekleri, gerekli parametreler ve hata işleme ayrıntılarını içerir."
weight: 32
---

## REST API

Bu REST API, birden fazla Excel dosyasını tek bir Excel çalışma kitabında birleştirir.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek parametreleri

| Parametre Adı  | Tür      | Konum       | Açıklama                                                                                     | Gerekli |
| ---------------- | -------- | ----------- | -------------------------------------------------------------------------------------------- | ------- |
| files[]          | dosya    | formData    | Birleştirilecek bir veya daha fazla Excel çalışma kitabı. İsteğin içinde `file1`, `file2`, … kullanın. | Evet    |
| format           | string   | query       | İstenen çıktı formatı (örn. `xlsx`).                                                        | Evet    |
| mergeToOneSheet  | boolean  | query       | Tüm çalışma sayfalarını tek bir sayfada birleştirmek için `true` olarak ayarlayın; varsayılan değer `false`’dır. | Hayır   |

### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[birleştirilmiş dosya adı]",
    "Filesize" : [dosya boyutu],
    "FileContent" : "[Base64Dizesi]"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut limitini aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |
## SDK’larla PostMerge API’sini Nasıl Kullanılır

### PostMerge API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt belirteci>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64Dizesi--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları işler, böylece proje görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

---