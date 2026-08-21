---
title: "Elektronik Tabloyu Başka Bir Formata Kaydet – Aspose.Cells Cloud API (v4.0)"
second_title: "Belge"
ArticleTitle: "Bulut Depolamada Bir Elektronik Tabloyu Başka Bir Formatta Dosyaya Kaydetme: Adım Adım Kılavuz"
linktitle: "Elektronik Tabloyu Başka Formatta Kaydet"
type: docs
url: /save-spreadsheet-as/
keywords: "Aspose Cells, elektronik tablo dönüştürme, farklı kaydet, API, XLSX'den PDF'e, bulut depolama, Excel'den PDF'e, CSV dışa aktarma, bulut dönüştürme"
description: "Aspose Cloud'da depolanan bir elektronik tabloyu başka bir formata (XLSX, PDF, CSV vb.) kaydetme yöntemini öğrenin. Aspose.Cells Cloud Save Spreadsheet API kullanarak istek sözdizimi, parametreler, cURL örneği ve SDK kodlarını içerir."
weight: 100
---

Bulut depolamada bir bulut elektronik tabloyu veya Excel dosyasını farklı bir formatta kaydedin.

## **Elektronik Tabloyu Başka Formatta Kaydet API’si**

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı   | Tür    | Konum   | Açıklama                                                                                 |
| :-------------- | :----- | :------ | :---------------------------------------------------------------------------------------- |
| name            | String | Path    | **Zorunlu.** Dönüştürülecek çalışma kitabının dosya adı.                                  |
| format          | String | Query   | **Zorunlu.** İstenen çıktı formatı (örneğin, `Xlsx`, `PDF`, `CSV`).                      |
| saveOptionsData | Class  | Body    | İsteğe bağlı kaydetme seçenekleri verisi. Atlanırsa, varsayılan değer `null` olur.       |
| folder          | String | Query   | Kaynak çalışma kitabının bulunduğu klasör yolu. Atlanırsa, varsayılan değer `null` olur. |
| storageName     | String | Query   | Özel bir depo adı. Atlanırsa, varsayılan depo kullanılır.                                |
| outPath         | String | Query   | Dönüştürülen dosya için isteğe bağlı çıktı yolu. Atlanırsa, varsayılan değer `null` olur. |
| outStorageName  | String | Query   | Çıktı dosyası için isteğe bağlı depo adı.                                                |
| fontsLocation   | String | Query   | İsteğe bağlı özel yazı tipi konumu.                                                      |
| region          | String | Query   | İsteğe bağlı elektronik tablo bölge ayarı.                                               |
| password        | String | Query   | Elektronik tablo dosyasını açmak için isteğe bağlı şifre.                                |

**Desteklenen çıktı formatları**

| Format   | Uzantı                                           |
| :------- | :----------------------------------------------- |
| Xlsx     | .xlsx                                            |
| Pdf      | .pdf                                             |
| Csv      | .csv                                             |
| Html     | .html                                            |
| Ods      | .ods                                             |
| Xls      | .xls                                             |
| Txt      | .txt                                             |
| Mhtml    | .mhtml                                           |
| Tiff     | .tiff                                            |
| Pptx     | .pptx                                            |
| … (daha fazla) | Tam liste için API spesifikasyonuna bakın (20'den fazla format) |

### **Yanıt**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Örnek hata yanıtı (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "Geçersiz istek parametreleri."
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                         |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.     |
| 400  | Bad Request           | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized          | Geçersiz veya eksik JWT token.                                   |
| 413  | Payload Too Large     | Yüklenen dosya boyut sınırını aşıyor.                            |
| 500  | Internal Server Error | Beklenmeyen sunucu hatası.                                       |

## Elektronik Tabloyu Başka Formatta Kaydet API’si nerede kullanılmalıdır?

### Kurumsal Belge Yönetim Sistemi

- Finansal raporları otomatik olarak PDF arşivleri olarak kaydetme.
- Satış verilerini düzenli olarak CSV formatında yedekleme.
- Proje planlarını yanlışlıkla değiştirilmeyi önlemek için salt okunur dosyalar olarak kaydetme.

### Veri Entegrasyonu ve ETL Süreçleri

- CRM sistemi verilerini dışa aktararak standart Excel şablonu olarak kaydetme.
- ERP verilerini diğer sistemlere içe aktarmak için CSV formatına dönüştürme.
- API ile iletim için ham verileri JSON formatında kaydetme.

### Geliştirme ve Otomasyon Senaryoları

- Web uygulamaları için arka uç işlemesi.
- Otomatik rapor oluşturma sistemleri.
- Bulut iş birliği platformları.
- Onay süreci entegrasyonu.
- Veri yedekleme ve taşıma.

## Elektronik Tabloyu Başka Formatta Kaydet API’si neden kullanılmalıdır?

- **Geliştirici Dostu** – Birden fazla dil için SDK'lar ve ayrıntılı dokümantasyon sunarak entegrasyonu kolaylaştırır.
- **İş Gücü Verimliliği** – Dönüştürmeyi sunucu tarafında gerçekleştirdiğinden özel dönüştürme kodlarına olan ihtiyacı azaltır.
- **Kullanım Tabanlı Fiyatlandırma** – Ön ödeme lisans ücreti olmadan yalnızca gerçekleştirilen API çağrıları için ücret alır.
- **Sunucu Bakımı Yok** – Hizmet bulutta çalıştığından dönüştürme altyapısını yönetme ihtiyacı ortadan kaldırılır.
- **Geniş Format Desteği** – 20'den fazla elektronik tablo formatı arasında dönüştürmeyi destekler.
- **Veri Sadakati** – Dönüştürme sırasında düzeni, formülleri ve stilleri korur.

## Elektronik Tabloyu SDK’larla Başka Formatta Kaydet API’si Nasıl Kullanılır?

### Elektronik Tabloyu Başka Formatta Kaydet API Spesifikasyonu

[Elektronik Tabloyu Başka Formatta Kaydet API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs), web tarayıcısından doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık bir programlama arayüzü tanımlar.

**İstek gövdesi ve cURL ile örnek**

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek yapma yöntemini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak ve minimum kodla bir elektronik tabloyu başka bir formatta kaydetmenizi sağladığından en hızlı gelişim yöntemidir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemlerini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}