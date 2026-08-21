---
title: "Aspose.Cells Cloud Excel Korumasını Kaldırma Web API’si – Open ve Modify Şifrelerini Programlı Olarak Kaldırın"
second_title: "Belge"
ArticleTitle: "Excel Şifre Korumasını Kaldırın – Open ve Modify Şifrelerini Anında Kaldırın"
linktitle: "Tabloyu Korumasını Kaldır"
type: docs
url: /tr/unprotect-spreadsheet/
keywords: "korumasız bırak, tablo, Aspose.Cells, API, Excel, şifre kaldırma"
description: "Aspose.Cells Cloud Tablo Korumasını Kaldırma API’si ile Excel dosyalarının açılış ve değiştirme şifrelerini programlı olarak kaldırın. .xlsx/.xls formatlarını, OAuth2 kimlik doğrulamayı ve toplu işlem desteğini destekler."
weight: 100
---

Tablo Korumasını Kaldırma API’si, Excel dosyalarının açılış ve değiştirme şifrelerini tek bir çağrıda kaldırır. Veri işlem hattı, belge yönetim sistemleri ve taşıma iş akışları için idealdir.

## **Tablo Korumasını Kaldırma API’si**

### **Web API’si**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri**

| Parametre Adı   | Tür    | Konum     | Açıklama                                                                              |
| --------------- | ------ | --------- | ------------------------------------------------------------------------------------- |
| Spreadsheet     | Dosya  | FormData  | Koruması kaldırılacak Excel dosyası.                                                  |
| password        | String | Query     | Dosyanın açılmasını koruyan şifre.                                                    |
| modifyPassword  | String | Query     | Dosyanın değiştirilmesi için gereken şifre (yalnızca açılış şifresi varsa isteğe bağlı). |
| outPath         | String | Query     | (İsteğe bağlı) Koruması kaldırılmış çalışma kitabının kaydedileceği klasör yolu.      |
| outStorageName  | String | Query     | (İsteğe bağlı) Çıktı dosyasının yazılacağı depo adı.                                  |
| region          | String | Query     | (İsteğe bağlı) Tablo bölgesel ayarları.                                                |

### **Yanıt**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Başarılı bir yanıt, korumasız dosyayı bir akış olarak döndürür. Dosya, `outPath`/`outStorageName` ile belirtilen konuma kaydedilebilir veya doğrudan yanıt yükünden alınabilir.

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400 | Hatalı İstek          | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413 | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                        |

## **Tablo Korumasını Kaldırma API’si Ne Zaman Kullanılmalı?**

- **Kilitli Çalışma Kitaplarına Erişimi Geri Yükleyin** – Unutulan açılış veya değiştirme şifrelerini manuel müdahale olmadan hızlıca kaldırın.
- **Toplu Kilit Açma İşlemini Otomatikleştirin** – Veri taşıma veya arşivleme projelerinde büyük sayıda dosyayı işleyin.
- **Mevcut İş Akışlarınızla Entegrasyon Sağlayın** – Depolama veya dönüştürme API’leriyle birleştirerek uçtan uca işlem hattı oluşturun (örneğin, yükle → korumasız bırak → PDF’e dönüştür).
- **Veri Güvenliğini Koruyun** – İşlem sunucu tarafında gerçekleşir; orijinal dosyalar güvenli kalırken, korumasız sürüm bulut depolama alanınızda saklanır.

## **SDK’lar ile Tablo Korumasını Kaldırma API’sini Nasıl Kullanılır?**

### **OpenAPI Spesifikasyonu**

[Tablo Korumasını Kaldırma API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet), doğrudan web tarayıcısından REST etkileşimlerini kolaylaştırmak için herkese açık bir programlama arayüzü sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 ile kodlanmış)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Aspose.Cells Cloud SDK’larını Kullanın**

SDK kullanmak, kimlik doğrulama, istek oluşturma ve yanıt ayrıştırma işlemlerini yöneterek çağrıyı basitleştirir. SDK’lar birçok dilde mevcuttur ve tablo korumasını kaldırma için hazır yöntemler içerir.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Tablo Korumasını Kaldırma API’sine nasıl çağrı yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}