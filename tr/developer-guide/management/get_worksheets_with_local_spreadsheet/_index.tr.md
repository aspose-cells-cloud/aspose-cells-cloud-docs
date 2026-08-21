---
title: "Yerel Elektronik Tablo ile Çalışma Sayfalarını Alın"
ArticleTitle: "Yerel Elektronik Tablo ile Çalışma Sayfalarını Alın – Aspose.Cells Cloud"
second_title: "Belge"
linktype: "Yerel Elektronik Tablo ile Çalışma Sayfalarını Alın"
type: docs
url: /tr/cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, Çalışma Sayfaları, Yerel Elektronik Tablo, API"
description: "Şu anda etkin olan yerel elektronik tablodan tüm çalışma sayfalarının tam listesini getirir."
weight: 1000
---

## Aspose.Cells Cloud Web Hizmetlerinin Yerel Elektronik Tablo ile Çalışma Sayfalarını Alma Özelliği

Bu uç nokta, yerel elektronik tablo uygulamasına (örneğin Excel) interop veya yerel bir API üzerinden erişir, her bir çalışma sayfasının adını ve türünü (örneğin standart, grafik, makro) toplar ve bu koleksiyonu yapılandırılmış bir JSON dizisi olarak döndürür. Genellikle bir çalışma sayfası seçici kullanıcı arayüzünü doldurmak veya elektronik tablo içeriğini denetlemek için kullanılır.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | Dosya  | FormData (HTTP Gövdesi)        | Elektronik tablo dosyasını yükleyin. |
| region         | Dize   | Sorgu                       | Elektronik tablonun bölgesi/dili ayarı (örneğin `tr-TR`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmasını ve yerel ayara özel davranışları etkiler. *(isteğe bağlı)* |
| password       | Dize   | Sorgu                       | Elektronik tablo dosyasını açmak için şifre. *(isteğe bağlı)* |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
|----------------|------|-------------|
| Spreadsheet    | Dosya | Elektronik tablo dosyasını yükleyin. |

### **Yanıt**

```json
{
  "Worksheets": [
    {
      "Name": "Sayfa1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Grafik1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... ek çalışma sayfaları
  ]
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|---------|-------------|
| 200 | OK | Çalışma sayfaları listesi başarıyla alındı. |
| 400 | Bad Request | Geçersiz istek (örneğin, hatalı URL veya gerekli veriler eksik). |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya kimlik bilgisi sağlanmadı. |
| 404 | Not Found | Kaynak dosyaya erişilemiyor. |
| 413 | Payload Too Large | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | Internal Server Error | Elektronik tablo, veri alma sırasında bir anomaliyle karşılaştı. |

## Yerel Elektronik Tablo ile Çalışma Sayfalarını Almayı SDK’lar ile Nasıl Kullanılır

### Yerel Elektronik Tablo ile Çalışma Sayfalarını Alma Tanımı

[Yerel Elektronik Tablo ile Çalışma Sayfalarını Alma API Tanımı](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose.Cells Cloud web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek nasıl atlanacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=tr-TR&password=yourPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
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
      "Name": "Sayfa1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Grafik1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... ek çalışma sayfaları
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirmeyi hızlandırmanın en hızlı yoludur. Bir SDK, düşük seviye ayrıntıları soyutlayarak projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells Cloud web hizmetlerine nasıl istek atılacağını göstermektedir:
`[TBD]`
---