---
title: "Uzak Elektronik Tabloda Tüm Değişiklikleri Kabul Et"
ArticleTitle: "Uzak Elektronik Tabloda Tüm Değişiklikleri Kabul Et – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "Uzak Elektronik Tabloda Tüm Değişiklikleri Kabul Et"
type: docs
url: /cells/accept-all-revisions
aliases: ["/cells/accept-all-revisions"]
keywords: "Aspose.Cells, AcceptAllRevisions, Uzak Elektronik Tablo"
description: "Uzak depolamada bulunan bir elektronik tablodaki tüm değişiklikleri (revizyonları) kabul eder ve güncellenmiş çalışma kitabını dosyası olarak döndürür."
weight: 1000
---

## Aspose.Cells Cloud Web Hizmetlerinin Uzak Elektronik Tabloda Tüm Değişiklikleri Kabul Et Özelliği

Uzak depolamada saklanan belirtilen çalışma kitabındaki izlenen tüm değişiklikleri (revizyonları) kabul eder. İşlem, isteğe bağlı olarak sonucu farklı bir konuma veya depolama yerine yazabilir ve güncellenmiş dosyayı ikili akış olarak döndürür.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|----------------|------|-----------------------------|-------------|
| name | string | Yol | Uzak depolamada saklanan çalışma kitabının dosya adı. |
| folder | string | Sorgu | (İsteğe bağlı) Çalışma kitabının bulunduğu depolama klasörü. |
| storageName | string | Sorgu | (İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolama adı. Atlanırsa varsayılan depolama kullanılır. |
| outPath | string | Sorgu | (İsteğe bağlı) Güncellenmiş çalışma kitabının kaydedilmesi gereken klasör yolu. Varsayılan değer null’dır. |
| outStorageName | string | Sorgu | (İsteğe bağlı) Çıktı dosyasının kaydedileceği depolama adı. |
| fontsLocation | string | Sorgu | (İsteğe bağlı) Özel yazı tipi konumu yolu. |
| region | string | Sorgu | (İsteğe bağlı) Elektronik tablo bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmasını ve yerel ayara özgü davranışı etkiler. |
| password | string | Sorgu | (İsteğe bağlı) Elektronik tablo dosyasını açmak için kullanılacak şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| *Yok* | *Yok* | Bu işlem için bir istek gövdesi gerekmez. |

### **Yanıt**

```json
{
  "File": "Güncellenmiş çalışma kitabının ikili akışı (.xlsx gibi). Yanıt gövdesinde döndürülür."
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|-------|----------|
| 200 | OK | Tüm revizyonlar kabul edilmiş çalışma kitabı ikili dosya akışı olarak döndürülür. |
| 400 | Bad Request | Gerekli parametreler eksik veya geçersiz istek formatı. |
| 401 | Unauthorized | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large | İstek izin verilen boyut sınırlarını aşıyor. |
| 500 | Internal Server Error | Sunucuda beklenmeyen bir hata oluştu. |

## SDK’lar ile Uzak Elektronik Tabloda Tüm Değişiklikleri Kabul Et Nasıl Kullanılır

### Uzak Elektronik Tabloda Tüm Değişiklikleri Kabul Et Spesifikasyonu

[Uzak Elektronik Tabloda Tüm Değişiklikleri Kabul Et API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose Cells Cloud web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "Güncellenmiş çalışma kitabının ikili akışı (.xlsx gibi)."
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak projenizdeki görevlere odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web hizmetlerine nasıl istek atılacağını göstermektedir:
 `[TBD]`
---