---
title: "Aspose.Cells Cloud Dosya Kopyalama API'si - Bulutta Excel dosyalarının hızlı kopyalanması ve toplu işlemleri için bir arayüz"
second_title: "Belge"
ArticleTitle: "Bulut Tabanlı Excel Dosya Yönetimi Çözümü – Aspose.Cells Dosya Kopyalama API'sinin Toplu Kopyalama İşlevselliğinin Detaylı Açıklaması"
linktitle: "Dosya Kopyala"
type: docs
url: /tr/copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel dosyası kopyalama, Bulut depolama, REST API"
description: "Aspose.Cells Cloud CopyFile API’sini kullanarak Excel dosyalarını verimli bir şekilde çoğaltmayı ve depolama konumları arasında yönetmeyi öğrenin."
weight: 100
---

**copyFile** API'si, kullanıcıların bir Excel dosyasını belirtilen kaynak yolundan hedef yola kopyalamasını sağlar ve çeşitli depolama seçeneklerini destekler.

## **Excel API’si: Dosya Kopyalama**

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **copyFile** API’sinin istek parametreleri

| Parametre Adı     | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                              |
| ----------------- | ------ | ---------------------------- | ----------------------------------------------------- |
| srcPath           | String | Yol                          | Kopyalanacak dosyanın kaynak yolu.                    |
| destPath          | String | Sorgu                        | Dosyanın kaydedileceği hedef yol.                     |
| srcStorageName    | String | Sorgu                        | Kaynak depolamanın adı.                               |
| destStorageName   | String | Sorgu                        | Hedef depolamanın adı.                                |
| versionId         | String | Sorgu                        | Kopyalanacak dosyanın isteğe bağlı sürüm kimliği.     |

### **Yanıt**

İşlem başarı durumunda içerik döndürmez. Karşılanan tipik HTTP durum kodları:

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                       |
| --- | --------------------- | -------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT belirteci.                            |
| 413 | Payload Too Large (İçerik Çok Büyük) | Yüklenen dosya boyut sınırını aşar.                         |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                  |

## SDK’lar ile Dosya Kopyalama API’si Nasıl Kullanılır?

### Dosya Kopyalama API Spesifikasyonu

[Dosya Kopyalama API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile), web tarayıcısından doğrudan REST etkileşimlerini gerçekleştirmek için erişilebilir bir programlama arayüzü sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istekte bulunmayı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
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

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak en hızlı geliştirme yoludur ve en az kod ile elektronik tablo verilerini görüntüye dönüştürmenizi sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)'na göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

---