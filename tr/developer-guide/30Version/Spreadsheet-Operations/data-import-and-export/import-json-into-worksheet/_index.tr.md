---
title: "JSON Verisini Excel'e İçe Aktar"
second_title: "Belge"
linktype: "İçerik"
type: docs
url: /tr/import-json-data-into-excel/
aliases: [  /tr/import/json/ ]
keywords: "Aspose.Cells Cloud, JSON içe aktarma, Excel API, REST ile JSON içe aktarma, SDK örnekleri"
description: "Aspose.Cells Cloud REST API kullanarak JSON verisini bir Excel çalışma sayfasına nasıl içe aktaracağınızı öğrenin. Uç nokta detaylarını, istek/yanıt örneklerini ve .NET, Java ve Python için SDK kodunu içerir."
weight: 40
---

Bu REST API, **JSON verisini bir Excel çalışma sayfasına** içe aktarır.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı         | Konum         | Tür    | Açıklama                                                                                             |
| --------------------- | ------------- | ------ | ---------------------------------------------------------------------------------------------------- |
| name                  | Yol (Path)    | string | Çalışma kitabının dosya adı.                                                                         |
| importJsonRequest     | HTTP gövdesi  | class  | JSON içe aktarma detaylarını içeren istek yükü.                                                     |
| password              | Sorgu dizesi  | string | Çalışma kitabını açmak için gerekli şifre (korunuyorsa).                                             |
| folder                | Sorgu dizesi  | string | Orijinal çalışma kitabının bulunduğu klasör.                                                        |
| storageName           | Sorgu dizesi  | string | Çalışma kitabının bulunduğu depo adı.                                                               |
| outPath               | Sorgu dizesi  | string | İçe aktarmadan sonra çıktı dosyasının yolu. Atlanırsa, güncellenmiş çalışma kitabı yanıtta döndürülür. |
| outStorageName        | Sorgu dizesi  | string | Çıktı dosyası için depo adı.                                                                         |
| checkExcelRestriction | Sorgu dizesi  | string | Excel'e özgü kısıtlamaların uygulanıp uygulanmayacağını belirten bayrak (true/false).                |

### **Örnek İstek Gövdesi**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### Yanıt

Başarılı bir istek, JSON yükü içeren **HTTP 200** döndürür:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Mümkün durum kodları:

| Kod | Anlam                                   |
| --- | --------------------------------------- |
| 200 | İçe aktarma işlemi başarıyla tamamlandı |
| 400 | Geçersiz istek – eksik veya geçersiz veri |
| 401 | Yetkisiz erişim – geçersiz veya eksik belirteç |
| 500 | Sunucu içi hata                         |


## SDK'lar ile PostWorkbookImportJson API’sini Nasıl Kullanılır

### PostWorkbookImportJson API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini en verimli şekilde hızlandıran yoldur. SDK’lar düşük seviye detayları kendisi yönetir, böylece iş mantığınız üzerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

---