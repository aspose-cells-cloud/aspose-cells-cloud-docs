---
title: "Depolama Kullanarak Veri İçe Aktar"
second_title: "Doküman"
linktype: "import-data-with-using-storage"
type: docs
url: /tr/import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Depolama Kullanarak Veri İçe Aktar: Aspose.Cells Cloud API ile verileri çeşitli depolama kaynaklarından bir Excel çalışma sayfasına içe aktarın. JSON, CSV ve diğer formatları HTTPS üzerinden destekler."
keywords: "Aspose.Cells Cloud, Excel, Veri İçe Aktar, REST API, Bulut Depolama, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Depolama Kullanarak Veri İçe Aktar - Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, verileri bir Excel dosyasına içe aktarır.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı  | Tür     | Konum  | Açıklama                                                        |
| -------------- | ------- | ------ | --------------------------------------------------------------- |
| name           | string  | path   | Excel dosyasının adı.                                           |
| folder         | string  | query  | Dosyanın bulunduğu depolama içindeki klasör yolu.              |
| storageName    | string  | query  | Depolama hizmetinin adı.                                        |
| importData     | object  | body   | İçe aktarılacak verileri içeren JSON nesnesi.                  |

**İçe aktarma verisi seçenekleri parametreleri**, [bu referans bağlantısında](/cells/import/#import-data-option-parameter) açıklanmıştır.

**Önkoşullar:** `Authorization` başlığından geçerli bir JWT belirteci sağlamalı ve hedef çalışma kitabının önceden belirtilen depolama konumunda mevcut olduğundan emin olmalısınız.

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                                         |
|-----|-----------------------------|------------------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.     |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                               |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.                          |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                    |

## SDK’lar ile PostImportData API’yi Nasıl Kullanılır

### PostImportData API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sini nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviyeli detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örneği, PHP SDK kullanarak Aspose.Cells web hizmetini nasıl çağıracağınızı göstermektedir: