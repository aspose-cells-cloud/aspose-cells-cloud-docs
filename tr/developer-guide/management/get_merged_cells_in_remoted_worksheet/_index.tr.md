---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Uzak Çalışma Sayfasındaki Birleştirilmiş Hücreleri Al – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "Get Merged Cells In Remote Worksheet"
type: docs
url: /cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, Birleştirilmiş Hücreleri Al, Uzak Çalışma Sayfası, API"
description: "Çalışma sayfasında birleştirilmiş tüm hücre alanlarını uzaktan alır."
weight: 10
---

## Aspose.Cells Cloud Web Servislerinin GetMergedCellsInRemotedWorksheet Özelliği

Uzak bir hesaplama tablosu çalışma sayfasındaki tüm birleştirilmiş hücre alanlarını alın.

### Web API Uç Noktası

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|----------------|--------|-----------------------------|-------------|
| name | string | Yol | Hesaplama tablosu dosyası adı |
| worksheet | string | Yol | Çalışma sayfası adı |
| folder | string | Sorgu | Hesaplama tablosunun bulut depolama yolu |
| storageName | string | Sorgu | (İsteğe bağlı) Özel bulut depolama kullanıyorsanız depolama adı. Atlanırsa varsayılan depolama kullanılır. |
| region | string | Sorgu | Hesaplama tablosu bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmasını ve yerel ayara özel davranışı etkiler. |
| password | string | Sorgu | Hesaplama tablosu dosyasını açmak için parola |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| — | — | *Yok* |

### **Yanıt**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|---------|-------------|
| 200 | OK | İstek başarılı oldu ve birleştirilmiş hücre alanlarının listesi döndürüldü. |
| 400 | Bad Request | Geçersiz URL veya hatalı formatlanmış istek parametreleri. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya kimlik bilgileri sağlanmadı. |
| 413 | Payload Too Large | İstek gövdesi izin verilen boyutu aştı. |
| 500 | Internal Server Error | Hesaplama tablosu verileri alınırken bir anormallik oluştu. |

## SDK'lar ile GetMergedCellsInRemotedWorksheet Nasıl Kullanılır

### GetMergedCellsInRemotedWorksheet Spesifikasyonu

[GetMergedCellsInRemotedWorksheet API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose Cells Cloud web servislerine nasıl istek yapıldığını göstermektedir:
`[TBD]`
---