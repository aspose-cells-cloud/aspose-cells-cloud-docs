---
title: "Excel'de Çalışma Sayfasını Yeniden Adlandırın – Aspose.Cells Cloud API"
second_title: "Belge"
ArticleTitle: "Excel'de Çalışma Sayfalarını Yeniden Adlandırma – Sayfa Adlarını Değiştirme"
linktitle: "Tablolama Dosyasında Çalışma Sayfasını Yeniden Adlandırın"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "çalışma sayfasını yeniden adlandır, Aspose.Cells Cloud, Excel API, tablolama dosyası, SDK, REST API"
description: "Aspose.Cells Cloud API ile Excel çalışma sayfalarını kolayca yeniden adlandırın. Gerekli parametreleri öğrenin, cURL örneklerini görün ve C#, Java, Python ve daha fazlası için SDK kodlarını edinin."
weight: 100
---

Aspose.Cells Cloud API kullanarak Excel çalışma kitaplarındaki çalışma sayfalarını programlı olarak yeniden adlandırın. Sayfa adlarını değiştirin, sekme etiketlerini dinamik olarak güncelleyin ve RESTful API çağrıları aracılığıyla tablolama dosyası düzenini otomatikleştirin. Belge standardizasyonu ve iş akışı otomasyonu için kullanışlıdır.

## Tablolama Dosyası API'sinde Çalışma Sayfası Adını Yeniden Adlandırma

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**cURL Örneği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Rapor_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@myWorkbook.xlsx"
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı      | Tür     | Konum     | Açıklama                                                                                                                                                                                                          |
| ------------------ | ------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Dosya   | FormData  | **Gerekli**. Yeniden adlandırılacak çalışma sayfasını içeren Excel çalışma kitabı dosyası (.xlsx, .xls vb.).                                                                                                     |
| **sourceName**     | Dize    | Sorgu     | **Gerekli**. Yeniden adlandırmak istediğiniz çalışan sayfanın mevcut adı.                                                                                                                                         |
| **targetName**     | Dize    | Sorgu     | **Gerekli**. Çalışma sayfasına atamak istediğiniz yeni ad. Excel adlandırma kurallarına (`, \, ?, *, [, ]` karakterlerini içermez) uymalı ve çalışma kitabında benzersiz olmalıdır.                                 |
| **outPath**        | Dize    | Sorgu     | **İsteğe Bağlı**. Yeniden adlandırılmış çalışma kitabının kaydedileceği bulut depolama alanındaki hedef klasör yolu. `null` veya atlanırsa, hizmet dosyayı kaynak çalışma kitabının bulunduğu klasöre (veya varsayılan yola) kaydeder. |
| **outStorageName** | Dize    | Sorgu     | **İsteğe Bağlı**. Yapılandırılmış bulut depolama hizmetinizin ad tanımlayıcısı (örneğin, `ArchiveStorage`). Atlanırsa varsayılan depolama kullanılır.                                                              |
| **region**         | Dize    | Sorgu     | **İsteğe Bağlı**. Karakter kodlamasını veya bölgesel adlandırma kurallarını etkileyebilen yerel ayar (örneğin, `tr-TR`).                                                                                           |
| **password**       | Dize    | Sorgu     | **İsteğe Bağlı**. Şifreli bir çalışma kitabını açmak ve değiştirmek için gereken deşifre şifresi. Dosya şifrelenmemişse atlayın.                                                                                   |

**Notlar**: Çalışma sayfası adları 31 karakterle sınırlıdır ve `:`, `\`, `?`, `*`, `[`, `]` karakterlerini içeremez.

### Yanıt

Başarılı bir istek, durum bilgilerini ve yeniden adlandırılmış dosyaya bir bağlantıyı içeren bir JSON nesnesi döndürür.

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

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                         |
| --- | --------------------- | ---------------------------------------------------------------- |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.     |
| 400 | İstek Hatası          | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                               |
| 413 | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                       |

## Tablolama Dosyası API'sinde Çalışma Sayfasını Yeniden Adlandırma Nerede Kullanılmalı?

- **Rapor Oluşturma ve Marka Standardizasyonu** – Müşteri raporları otomatik olarak oluşturulurken genel çalışma sayfası adları (örneğin, `Sheet1`), müşteriye özel adlarla (örneğin, `AcmeCorp_Q1_Ozet`) yeniden adlandırılarak profesyonel bir teslimat sağlanır.
- **Veri İşleme İş Akışı Standardizasyonu** – ETL iş akışlarında, düzensiz adlarla dışa aktarılan çalışma sayfaları, ileri aşamadaki analiz gereksinimlerini karşılamak için `Raw_Data` veya `Cleaned_Data` gibi standart adlarla yeniden adlandırılır.
- **Çok Dilli İçerik Dağıtımı** – Kullanıcının dil tercihine göre çalışma sayfası adları, dosya teslim edilmeden önce yerelleştirilir (örneğin, `Veri` veya `Data`), böylece kullanıcıya özel bir deneyim sağlanır.

## Tablolama Dosyası API'sinde Çalışma Sayfasını Yeniden Adlandırma API'sini Neden Kullanmalısınız?

- **Geliştirici Dostu** – Kapsamlı belgelerle birlikte birkaç dil için SDK’lar sunar; özel bir çözüm oluşturmaya kıyasla entegrasyonu basitleştirir.
- **Azaltılmış Emek** – Çalışma sayfası yeniden adlandırma işlemini otomatikleştirerek manuel çabayı azaltır.
- **Kullanıma Göre Ödeme Modeli** – Ön ödemeli lisans maliyetlerini ortadan kaldırarak yalnızca API çağrıları için ücret alır.
- **Sunucu Bakımı Gerekmez** – Bulut hizmeti olduğu için sunucuları barındırma ve bakım yapma veya yazılım güncellemeleri uygulama gereksinimini ortadan kaldırır.
- **Otomasyon Desteği** – İş akışları içinde belge standardizasyonunu otomatikleştirmeyi sağlar.

## SDK’larla Tablolama Dosyası API'sinde Çalışma Sayfasını Yeniden Adlandırma Nasıl Kullanılır?

### OpenAPI Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, web tarayıcısından doğrudan REST etkileşimlerine izin veren herkese açık bir programlama arayüzü açıklar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Sheet1&destName=YeniSayfaAdi" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 kodlanmış)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en hızlı yoludur. SDK, altta yatan HTTP detaylarını soyutlayarak minimum kodla çalışma sayfalarını yeniden adlandırmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için GitHub deposuna bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}