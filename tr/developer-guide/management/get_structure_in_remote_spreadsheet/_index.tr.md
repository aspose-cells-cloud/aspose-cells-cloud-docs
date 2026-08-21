---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Uzak Elektronik Tabloda Yapı Al – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "GetStructureInRemoteSpreadsheet"
type: docs
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, elektronik tablo, yapı"
description: "Çalışma kitabının, çalışma sayfaları, tablolar, pivot tablolar, grafikler, şekiller ve diğer temel bilgiler dahil olmak üzere uzak bir Excel çalışma kitabının yapısal meta verilerini alın."
weight: 100
---

## Aspose.Cells Cloud Web Hizmetlerinin Uzak Elektronik Tabloda Yapı Al

Bir Excel çalışma kitabının temel meta verilerini, çalışma sayfalarını, tablolarını, pivot tablolarını, grafiklerini, şekillerini ve diğer bilgilerini yapısal olarak bir JObject türünde JSON nesnesine dönüştürün; bu, veri dışa aktarma, API yanıtları ve günlük kaydı gibi senaryolar için kullanılır.

### Web API Uç Noktası

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama |
|----------------|------|-----------------------------|-------------|
| name | string | Yol | Elektronik tablo dosyasının adı. |
| folder | string | Sorgu | Dosyanın bulunduğu klasör. (İsteğe bağlı) |
| storageName | string | Sorgu | (İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolama adı. Atlanırsa varsayılan depolama kullanılır. |
| region | string | Sorgu | Elektronik tablonun bölge/dil ayarı (örneğin, `tr-TR`, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih çözümlemesi ve yerel ayara özel davranışları etkiler. |
| password | string | Sorgu | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Yanıt**

```json
{
  "Worksheets": [
    {
      "Name": "Sayfa1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|---------|-------------|
| 200 | Tamam | Çalışma kitabının yapısı başarıyla alındı. |
| 400 | Geçersiz İstek | Geçersiz istek parametreleri. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya belirteç eksik. |
| 413 | Yük Çok Büyük | İstek gövdesi izin verilen boyutu aştı. |
| 500 | Sunucu İç Hatası | Beklenmeyen sunucu hatası. |

## Uzak Elektronik Tabloda Yapı Al’ı SDK’lar ile Nasıl Kullanılır

### Uzak Elektronik Tabloda Yapı Al Spesifikasyonu

[Uzak Elektronik Tabloda Yapı Al API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sayfa1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "Ahmet Yılmaz",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SatışRaporu",
    "Subject": "Çeyreklik Satışlar",
    "Keywords": "satış,rapor,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirmeyi hızlandırmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web hizmetlerinin nasıl çağrılacağını göstermektedir:
`[TBD]`
---