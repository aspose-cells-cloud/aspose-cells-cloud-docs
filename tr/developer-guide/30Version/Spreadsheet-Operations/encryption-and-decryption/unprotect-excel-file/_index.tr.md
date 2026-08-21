---
title: "Excel Çalışma Kitabını Korumasını Kaldır – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Excel Dosyasının Korumasını Kaldır"
type: docs
url: /tr/excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, Excel koruması kaldırma API'si, çalışma kitabı korumasını kaldır, REST API, bulut elektronik tablo"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabının korumasını nasıl kaldıracağınızı öğrenin. İstek sözdizimi, parametreler, cURL örneği ve birden fazla dilde SDK kodunu içerir."
weight: 60
ArticleTitle: "Excel Çalışma Kitabını Korumasını Kaldır – Aspose.Cells Cloud API"
---

Bu REST API'yi bir Excel çalışma kitabının korumasını kaldırmak için kullanın.

## DeleteUnProtectWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### Yol Parametreleri

| Parametre | Tür     | Açıklama                                           | Gerekli |
| --------- | ------- | -------------------------------------------------- | ------- |
| **name**  | string  | Çalışma kitabı dosyasının adı (uzantı dahil).     | Evet    |

### Sorgu Parametreleri

| Parametre Adı | Tür    | Açıklama                                                |
| ------------- | ------ | ------------------------------------------------------- |
| folder        | string | Orijinal çalışma kitabının bulunduğu klasörün yolu.    |
| storageName   | string | Çalışma kitabının bulunduğu depolama hizmetinin adı.   |

### İstek Gövdesi Parametreleri

| Parametre Adı | Tür                       | Açıklama                                          |
| ------------- | ------------------------- | ------------------------------------------------ |
| protection    | WorkbookProtectionRequest | Kaldırılacak koruma ayarlarını belirten nesne.   |

#### WorkbookProtectionRequest

| Parametre Adı  | Tür    | Açıklama                                                                                     |
| -------------- | ------ | -------------------------------------------------------------------------------------------- |
| ProtectionType | string | Kaldırılacak koruma türü (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password       | string | Korumayı kaldırmak için gereken şifre (isteğe bağlı).                                        |

#### cURL Örneği

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### Yanıt (Başarılı)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### HTTPS Durum Hata Yanıtları

| HTTP Durumu | Kod                 | Açıklama                                                   |
| ----------- | ------------------- | ---------------------------------------------------------- |
| 400         | BadRequest          | Eksik veya geçersiz parametreler.                          |
| 401         | Unauthorized        | Geçersiz veya eksik erişim belirteci.                      |
| 404         | NotFound            | Belirtilen çalışma kitabının belirtilen klasör/depolamada bulunamadı. |
| 500         | InternalServerError | Beklenmeyen sunucu hatası.                                 |

## DeleteUnProtectWorkbook API'sini SDK'larla Nasıl Kullanılır

### DeleteUnProtectWorkbook API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl çağrı yapılacağını göstermektedir.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak entegrasyonu basitleştirir ve tekrarlayan kod miktarını azaltır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---