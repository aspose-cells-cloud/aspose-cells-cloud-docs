---
title: "Bir Excel çalışma sayfasındaki tüm boş olmayan hücreleri eşleştirin"
second_title: "Belge"
linktitle: "Tüm boş olmayan hücreleri eşleştirin"
type: docs
url: /autofilter/match-all-non-blank/
aliases: [/match-all-non-blank-cells-in-the-list/]
keywords: "Aspose.Cells Cloud, boş olmayan hücreleri eşleştirme, AutoFilter, Excel API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki bir AutoFilter listesindeki tüm boş olmayan hücreleri nasıl eşleştireceğinizi öğrenin. Endpoint, parametreler, kimlik doğrulama, yanıt şeması, hata kodları ve SDK örneklerini içerir."
ArticleTitle: "Aspose.Cells Cloud API kullanarak bir Excel çalışma sayfasındaki tüm boş olmayan hücreleri eşleştirin"
weight: 100
---

**Genel Bakış**  
*Tüm boş olmayan hücreleri eşleştir* işlemi, bir çalışma sayfasına bir AutoFilter uygular ve belirtilen sütunda veri bulunan satırları döndürürken boş hücreleri yok sayar. Bu işlem, veri setlerini temizlemek, rapor oluşturmak veya daha fazla analiz için verileri hazırlamak için kullanışlıdır.

**Ön Gereksinimler**  
- Aspose.Cells Cloud kimlik doğrulaması için geçerli bir JWT jetonu.  
- Çalışma kitabının Aspose Cloud depolama alanına yüklenmiş olması gerekir.  
- Filtrelemek istediğiniz dosya adı, çalışma sayfası adı ve sıfır tabanlı sütun indeksini (`fieldIndex`) bilmelisiniz.

Bu REST API, bir Excel çalışma sayfasındaki AutoFilter listesindeki tüm boş olmayan hücreleri eşleştirir.

## PostWorksheetMatchNonBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür      | Konum   | Açıklama                                                       |
| ------------- | -------- | ------- | -------------------------------------------------------------- |
| name          | string   | path    | Excel dosyasının adı.                                          |
| sheetName     | string   | path    | AutoFilter’ın bulunduğu çalışma sayfasının adı.                |
| fieldIndex    | integer  | query   | Filtrenin uygulanacağı sütunun sıfır tabanlı indeksi.          |
| folder        | string   | query   | _(İsteğe bağlı)_ Dosyanın bulunduğu klasör yolu.               |
| storageName   | string   | query   | _(İsteğe bağlı)_ Kullanılacak depolama hizmetinin adı.         |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | İstek Hatası                | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz İstek              | Geçersiz veya eksik JWT jetonu. |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası. |

*Örnek hata yanıtı (400)*  

```json
{
  "Code": 400,
  "Message": "Geçersiz parametre: fieldIndex negatif olmayan bir tamsayı olmalıdır."
}
```

## PostWorksheetMatchNonBlanks API’yi SDK’lar ile Nasıl Kullanılır

### PostWorksheetMatchNonBlanks API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları yönetir ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine istek yapmayı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}