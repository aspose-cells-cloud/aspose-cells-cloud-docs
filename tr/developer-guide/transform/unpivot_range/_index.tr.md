---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "Belge"
linktype: "UnpivotRange"
type: docs
url: /tr/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "Tablodaki satırları ve sütunları değiştirin."
weight: 10
---

## Aspose.Cells Cloud Web Hizmetlerinin UnpivotRange Özelliği

Tablodaki satırları ve sütunları değiştirin.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                     |
|------------------|--------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Dosya  | FormData                      | Tablo dosyasını yükleyin.                                                                                                                                     |
| worksheet        | string | Sorgu                         | Çalışma sayfası adı.                                                                                                                                          |
| cellArea         | string | Sorgu                         | Belirli bir veri aralığı.                                                                                                                                     |
| skipEmptyValue   | boolean| Sorgu                         | true ise boş değerleri atlar. Varsayılan: true.                                                                                                              |
| outPath          | string | Sorgu                         | (İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.                                                                          |
| outStorageName   | string | Sorgu                         | Çıkış dosyasının depo adı.                                                                                                                                    |
| region           | string | Sorgu                         | Tablo bölgesi/dil ayarı (örneğin `en-US`, `fr-FR`). SayıBiçimlendirme, tarih ayrıştırma ve yerel ayara özel davranışları etkiler.                           |
| password         | string | Sorgu                         | Tablo dosyasını açmak için parola.                                                                                                                            |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
|---------------|-----|----------|
| —             | —   | —        |

### **Yanıt**

```json
{
  "File": "ikili akış"
}
```

**Yanıt Durum Kodları**

| Kod | Anlamı | Açıklama |
|-----|--------|----------|
| 200 | OK | Pivotlanmamış tablo dosyası döndürülür. |
| 400 | Bad Request | Geçersiz istek parametreleri. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu. |
| 413 | Payload Too Large | Yüklenen dosya boyut sınırlarını aşıyor. |
| 500 | Internal Server Error | Sunucu beklenmeyen bir durumla karşılaştı. |

## SDK’larla UnpivotRange Nasıl Kullanılır

### UnpivotRange Spesifikasyonu

[UnpivotRange API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells Cloud web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapıldığını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose Cells Cloud web hizmetlerine nasıl istek atılacağını göstermektedir:
 `[TBD]`
---