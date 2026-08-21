---
title: "Aspose.Cells Cloud Web API – Metin Çıkar"
second_title: "Aspose.Cells Cloud – Çevrimiçi Kısa Kod"
linktitle: "Metin Çıkar"
type: docs
url: /tr/extract-text/
keywords: "Aspose.Cells Cloud, Metin Çıkar, Excel API, hücre metni çıkarma, REST API"
description: "Aspose.Cells Cloud API kullanarak Excel hücrelerinden alt dizgileri, sayıları veya karakterleri çıkarın. Öncesi/sonrası metin, konuma dayalı çıkarım ve doğrudan yeni bir aralık çıktısı destekler."
weight: 100
ArticleTitle: "Aspose.Cells Cloud Metin Çıkar API Belgesi"
---

Bir hesaplama sayfası hücresinden alt dizgileri, karakterleri veya sayıları başka bir hücreye çıkarır; bu sayede karmaşık FIND, MIN, LEFT veya RIGHT formüllerine gerek kalmaz.

## **ExtractText API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **ExtractText API'sinin İstek Parametreleri**

| Parametre Adı    | Tür     | Konum               | Açıklama                                                                                                                        |
| ---------------- | ------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Dosya   | FormData            | Hesaplama sayfası dosyasını yükleyin.                                                                                           |
| extractTextType  | Dize    | Sorgu               | Çıkarma modunu belirten numaralandırma. İzin verilen değerler: `Before`, `After`, `BeforePosition`, `AfterPosition`.           |
| beforeText       | Dize    | Sorgu               | Çıkarılacak alt dizgeden **önce** gelen metin. `extractTextType=Before` olduğunda kullanılır.                                   |
| afterText        | Dize    | Sorgu               | Çıkarılacak alt dizgeden **sonra** gelen metin. `extractTextType=After` olduğunda kullanılır.                                   |
| beforePosition   | Tamsayı | Sorgu               | Hücrenin solundan döndürülecek karakter sayısı. `extractTextType=BeforePosition` olduğunda kullanılır.                         |
| afterPosition    | Tamsayı | Sorgu               | Hücrenin sağından döndürülecek karakter sayısı. `extractTextType=AfterPosition` olduğunda kullanılır.                          |
| outPositionRange | Dize    | Sorgu               | Çıkarılan metnin yazılacağı hedef aralık (örn. `Sheet1!A1`).                                                                    |
| worksheet        | Dize    | Sorgu               | Kaynak hücreyi içeren çalışma sayfasının adı.                                                                                   |
| range            | Dize    | Sorgu               | Kaynak hücre veya aralık (örn. `A1`).                                                                                          |
| outPath          | Dize    | Sorgu _(İsteğe Bağlı)_ | Çıktı çalışma kitabının kaydedileceği depolama içindeki klasör yolu. Atlanırsa, sonuç yanıt gövdesinde döndürülür.               |
| outStorageName   | Dize    | Sorgu               | Çıktı dosyası için kullanılacak depolamanın adı.                                                                                |
| region           | Dize    | Sorgu               | Hesaplama sayfası bölgesel ayarı (örn. `US`, `EU`).                                                                             |
| password         | Dize    | Sorgu               | Korumalı bir çalışma kitabını açmak için gerekli parola.                                                                        |

**Örnek cURL İsteği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Toplam&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **Yanıt**

İstek başarıyla tamamlandığında API, çıkarılan metni ve yazıldığı hücrenin adresini içeren bir JSON yükü döndürür:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

`outPath` parametresi verilirse, yanıt yalnızca bir durum mesajı içerir; çalışma kitabına belirtilen konuma yazılır.

**`outPath` atlandığında örnek yanıt**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### Hata Kodları

- **200 OK** – Çıkarma işlemi başarıyla tamamlandı.  
- **202 Accepted** – İstek, eşzamansız işlem için kabul edildi.  
- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI’si veya eksik gerekli parametreler.  
- **401 Unauthorized** – Geçersiz erişim belirteci, istemci Kimliği veya istemci sırrı.  
- **404 Not Found** – Belirtilen hesaplama sayfası dosyasına erişilemiyor.  
- **500 Server Error** – Çalışma kitabını işlerken beklenmeyen bir hata oluştu.

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, temel alınan ayrıntıları işler; böylece **Metni Çıkar** işlemini en az kodla uygulamanız yeterli olur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istekte bulunulacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// C# örneği – metin çıkar (kısalmak için kod atlandı)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Java örneği – metin çıkar (kısalmak için kod atlandı)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// PHP örneği – metin çıkar (kısalmak için kod atlandı)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Ruby örneği – metin çıkar (kısalmak için kod atlandı)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Node.js örneği – metin çıkar (kısalmak için kod atlandı)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Python örneği – metin çıkar (kısalmak için kod atlandı)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Perl örneği – metin çıkar (kısalmak için kod atlandı)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Go örneği – metin çıkar (kısalmak için kod atlandı)
```

{{</tab>}}

{{< /tabs >}}