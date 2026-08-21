---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "GetSpreadsheetStructure"
type: docs
url: /cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, Elektronik Tablo Yapısı, API"
description: "Bir Excel çalışma kitabının temel meta verilerini, çalışma sayfalarını, tablolarını, pivot tablolarını, grafiklerini, şekillerini ve diğer bilgilerini yapısal olarak bir JObject türünden JSON nesnesine dönüştürür."
weight: 1000
---

## Aspose.Cells Cloud Web Hizmetlerinin GetSpreadsheetStructure Özelliği

Bir Excel çalışma kitabının temel meta verilerini, çalışma sayfalarını, tablolarını, pivot tablolarını, grafiklerini, şekillerini ve diğer bilgilerini yapısal olarak bir JObject türünden JSON nesnesine dönüştürün; bu, veri dışa aktarma, API yanıtları ve günlük kaydı gibi senaryolar için kullanılır.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|---------------|-------|------------------------------|----------|
| Spreadsheet   | Dosya | FormData (gövde)             | Elektronik tablo dosyasını yükleyin. |
| region        | Dize  | Sorgu                        | Elektronik tablonun bölge/dil ayarı (örneğin, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih çözümleme ve yerel ayara özel davranışları etkiler. |
| password      | Dize  | Sorgu                        | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| ------------- | --- | -------- |
| Spreadsheet   | Dosya | Elektronik tablo dosyasını yükleyin. |

### **Yanıt**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | Tamam | Elektronik tablo yapısı başarıyla alındı. |
| 400 | Geçersiz İstek | Geçersiz istek parametreleri veya dosya biçimi. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya JWT belirteci eksik. |
| 413 | Yük Çok Büyük | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası | Sunucuda beklenmeyen bir hata oluştu. |

## GetSpreadsheetStructure’ı SDK’lar ile Nasıl Kullanılır

### GetSpreadsheetStructure Spesifikasyonu

[GetSpreadsheetStructure API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose Cells Cloud web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini en hızlı şekilde hızlandırmak için en iyi yoldur. Bir SDK, düşük seviyeli detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, Aspose Cells Cloud web hizmetlerinin çeşitli SDK’lar kullanılarak nasıl çağrılacağını göstermektedir:
`[TBD]`
---