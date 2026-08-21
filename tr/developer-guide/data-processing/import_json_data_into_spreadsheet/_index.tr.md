---
title: "JSON Verisini Elektronik Tabloya İçe Aktar"
ArticleTitle: "JSON Verisini Elektronik Tabloya İçe Aktar – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "JSON Verisini Elektronik Tabloya İçe Aktar"
type: docs
url: /cells/import/data/json
aliases: []
keywords: "JSON İçe Aktar, Aspose.Cells, Elektronik Tablo, API"
description: "Yerel elektronik tabloya JSON veri dosyasını içe aktarın."
weight: 1
---

## Aspose.Cells Cloud Web Servislerinin JSON Verisini Elektronik Tabloya İçe Aktarma Özelliği

Yerel elektronik tabloya JSON veri dosyasını içe aktarın. Yöntem, JSON'u ayrıştırır, verileri elektronik tablonun hücre yapısına eşler ve dosyayı yerel olarak kaydeder. Desteklenen elektronik tablo formatları .xlsx ve .ods'dir.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|---------------|-------|-------------------------------|----------|
| datafile      | Dosya | FormData                      | Veri dosyasını yükleyin. |
| Spreadsheet   | Dosya | FormData                      | Elektronik tablo dosyasını yükleyin. |
| worksheet     | string| Sorgu                         | JSON verisinin içe aktarılacağı çalışma sayfası. |
| startcell     | string| Sorgu                         | Veri içe aktarma işleminin başlangıç konumu |
| insert        | boolean| Sorgu                        | Ekleme davranışını kontrol eder. true: verileri ekler; false: mevcut verilerin üzerine yazar. (Varsayılan: true) |
| outPath       | string| Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null'dır. |
| outStorageName| string| Sorgu                         | Çıktı dosyası için depo adı. |
| fontsLocation | string| Sorgu                         | Özel yazı tiplerini kullanın. |
| region        | string| Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örneğin, `tr-TR`, `en-US`, `fr-FR`). Sayı formatlama, tarih ayrıştırma ve yerel ayara özel davranışları etkiler. |
| password      | string| Sorgu                         | Elektronik tablo dosyasını açmak için parola. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| ------------- | --- | -------- |
| [TBD] | [TBD] | [TBD] |

### **Yanıt**

```json
{
  "file": "binary stream"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | OK  | Dosya başarıyla oluşturuldu ve döndürüldü. |
| 400 | Bad Request | Geçersiz URL. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya kimlik bilgileri sağlanmadı. |
| 404 | Not Found | Kaynak dosyaya erişilemedi. |
| 413 | Payload Too Large | [TBD] |
| 500 | Internal Server Error | Elektronik tablo veri alma sırasında bir anomaliyle karşılaştı. |

## JSON Verisini Elektronik Tabloya İçe Aktarma Özelliğini SDK'lar ile Nasıl Kullanılır

### JSON Verisini Elektronik Tabloya İçe Aktarma Spesifikasyonu

[JSON Verisini Elektronik Tabloya İçe Aktarma API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose Cells Cloud web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye istekte bulunma yöntemini göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}
{< tab tabNum="1" >}
```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "binary stream"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye detayları soyutlayarak projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose Cells Cloud web servislerine nasıl istekte bulunulacağını göstermektedir:
 `[TBD]`
---