---
title: "Uzak Elektronik Tabloda Karakterleri Kaldır"
ArticleTitle: "Uzak Elektronik Tabloda Karakterleri Kaldır – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Uzak Elektronik Tabloda Karakterleri Kaldır"
type: docs
url: /tr/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, Karakterleri Kaldır, Metin İşleme"
description: "Uzak bir elektronik tabloda, seçilen aralıkta bulunan tüm hücrelerden kullanıcı tanımlı karakterleri, önceden tanımlı simge setlerini veya herhangi bir alt dizeyi siler; formüller,Biçimlendirme ve veri doğrulamasını korur."
weight: 100
---

## Aspose.Cells Cloud Web Hizmetlerinin Uzak Elektronik Tabloda Karakterleri Kaldırma Özelliği

Uzak bir elektronik tabloda, seçilen aralıkta bulunan tüm hücrelerden kullanıcı tanımlı karakterleri, önceden tanımlı simge setlerini veya herhangi bir alt dizeyi siler; formüller, Biçimlendirme ve veri doğrulamasını korur.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı      | Tür    | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                                                                                                                       |
|---------------------|---------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                | string  | Yol                         | (Gerekli) Alınacak çalışma kitaplığı dosyasının adı.                                                                                                                         |
| worksheet           | string  | Yol                         | Elektronik tablonun çalışma sayfasını belirtin.                                                                                                                                              |
| range               | string  | Yol                         | Elektronik tablonun çalışma sayfası aralığını belirtin.                                                                                                                                       |
| removeTextMethod    | string  | Sorgu                       | Metin kaldırma yöntemi türünü belirtin.                                                                                                                                          |
| characterSets       | string  | Sorgu                       | Karakter kümelerini belirtin.                                                                                                                                                       |
| removeCustomValue   | string  | Sorgu                       | Özel değeri kaldırmayı belirtin.                                                                                                                                                  |
| caseSensitive       | boolean | Sorgu                       | Etkinleştirildiğinde `Substring` modunu ve `CustomChars` modunu etkiler.                                                                                                                          |
| folder              | string  | Sorgu                       | (İsteğe bağlı) Çalışma kitabının bulunduğu klasör yolu. Varsayılan değer null'dır.                                                                                                    |
| storageName         | string  | Sorgu                       | (İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolama adı. Atlanırsa varsayılan depolama kullanılır.                                                                               |
| region              | string  | Sorgu                       | Elektronik tablonun bölge/dil ayarı (örneğin, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler.                                         |
| password            | string  | Sorgu                       | Elektronik tablo dosyasını açmak için şifre.                                                                                                                                         |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| *None* | *None* | Bu işlem, istek gövdesi gerektirmez. |

### **Yanıt**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Karakterler başarıyla kaldırıldı.",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|---------|-------------|
| 200 | OK | Karakterler başarıyla kaldırıldı ve çalışma kitabı güncellendi. |
| 400 | Bad Request | Bir veya daha fazla parametre eksik veya geçersiz. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu – eksik veya geçersiz JWT belirteci. |
| 413 | Payload Too Large | İstek boyutu izin verilen sınırı aşıyor. |
| 500 | Internal Server Error | Sunucu tarafında beklenmeyen bir hata oluştu. |

## SDK’lar ile Uzak Elektronik Tabloda Karakterleri Kaldırma Nasıl Kullanılır

### Uzak Elektronik Tabloda Karakterleri Kaldırma Özelliği Spesifikasyonu

[Uzak Elektronik Tabloda Karakterleri Kaldırma API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Karakterler başarıyla kaldırıldı.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini en hızlı şekilde hızlandıran yaklaşımdır. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web hizmetlerine nasıl istek yapıldığını göstermektedir:
`[TBD]`
---