---
title: "Aspose.Cells Cloud Excel Çalışma Sayfası Silme Web API'si - Çalışma Kitaplarından Sayfaları Programlı Olarak Kaldırma"
second_title: "Belge"
ArticleTitle: "Excel'den Çalışma Sayfalarını Nasıl Silersiniz - Çalışma Kitaplarından Sayfaları Kaldırma"
linktitle: "Web Tablosundan Çalışma Sayfası Silme"
type: docs
url: /delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, çalışma sayfası silme API'si, Excel sayfası kaldırma, bulut web tablosu, REST API"
description: "Aspose.Cells Cloud API kullanarak bir Excel dosyasından çalışma sayfası nasıl silineceğini öğrenin. Uç nokta, parametreler, örnek cURL ve SDK örneklerini içerir."
weight: 100
---

Aspose.Cells Cloud API kullanarak Excel çalışma kitaplarından çalışma sayfalarını programlı olarak silin. Tek veya birden fazla sayfayı güvenle kaldırın, çalışma kitabı yapısını temizleyin ve web tablosu optimizasyonunu otomatikleştirin. Kurumsal düzeyde Excel yönetimi ve belge işleme iş akışları için RESTful API.

## Web Tablosundan Çalışma Sayfası Silme API'si

### Web API'si

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri:

| Parametre Adı | Tür   | Konum | Açıklama                                                                                                                                                                                                 |
| :------------ | :---- | :---- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | Dosya | FormData | **Zorunlu.** Çalışma sayfasının kaldırılacağı kaynak Excel çalışma kitabı dosyası (.xlsx, .xls vb.).                                                                                                    |
| sheetName     | Metin | Sorgu | **Zorunlu.** Silinecek çalışma sayfasının tam adı (örn. `Sheet1`, `TemporaryData`).                                                                                                                      |
| outPath       | Metin | Sorgu | **İsteğe bağlı.** Değiştirilen çalışma kitabının kaydedileceği bulut depolama alanındaki hedef klasör yolu. Atlanırsa veya `null` olarak belirtilirse, çalışma kitabı kaynak dosyanın bulunduğu konuma veya varsayılan bir yola kaydedilir. |
| outStorageName| Metin | Sorgu | **İsteğe bağlı.** Çıktı dosyasının yazılacağı bulut depolama hizmetinin tanımlayıcısı (örn. `ProjectStorage`). Belirtilmezse varsayılan depolama kullanılır.                                              |
| region        | Metin | Sorgu | **İsteğe bağlı.** Kaydetme işlemesi sırasında bölüme özel formülleri veya verileri etkileyebilen yerel ayar (örn. `tr-TR`).                                                                             |
| password      | Metin | Sorgu | **İsteğe bağlı.** Şifreli bir web tablosunu açmak ve değiştirmek için gerekli şifre. Dosya şifrelenmemişse belirtilmesine gerek yoktur.                                                                     |

### Yanıt

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

| Kod | Anlam                 | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400 | Geçersiz İstek        | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü).|
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413 | İstecik Çok Büyük     | Yüklenecek dosya boyut sınırını aşıyor.                           |
| 500 | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                        |

## Web Tablosundan Çalışma Sayfası Silme API'si Nerede Kullanılmalıdır?

- **Otomatik Rapor Son İşlemesi** – Nihai finansal raporu oluşturduktan sonra geçici hesaplamalar için kullanılan ara çalışma sayfalarını otomatik olarak silerek nihai dosyayı temiz ve profesyonel tutun.
- **Şablon Dosyalarının Dinamik Temizlenmesi** – Kullanıcılar bir şablonlardan özelleştirilmiş belgeler (örn. teklifler) oluşturduğunda, seçilmemiş isteğe bağlı sayfaları silin.
- **İş Akışı Arşivlemesinin Optimizasyonu** – Bir proje veya denetim tamamlandığında taslak veya iş birliği çalışma sayfalarını kaldırın ve yalnızca arşivleme ve uyumluluk için nihai sürümü saklayın.

## Web Tablosundan Çalışma Sayfası Silme API'si Neden Kullanılmalıdır?

- **Geliştirici Dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunarak hızlı geliştirme sağlar ve kapsamlı belgeler sağlar.
- **Düşük İşgücü Maliyeti** – Belgeleri manuel olarak birleştirmek için özel personel gerekmez.
- **Kullanım Ücretli** – Ön ödeme gerektirmez; sadece kullandığınız API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım Maliyeti** – Bakımı yapmanız gereken sunucu yoktur, yazılım güncellemeleri yoktur ve uyumluluk sorunları yoktur.

## Web Tablosundan Çalışma Sayfası Silme API'sini SDK'lar ile Nasıl Kullanılır?

### Web Tablosundan Çalışma Sayfası Silme API'si Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">Web Tablosundan Çalışma Sayfası Silme API Spesifikasyonu</a>, bir web tarayıcısından doğrudan REST etkileşimlerinde bulunmanıza olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca ulaşabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine istek nasıl yapılabileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak ve minimum kodla bir çalışma sayfasını silebilmeniz nedeniyle en hızlı geliştirme yoludur. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub Deposu</a>'na bakın.

Aşağıdaki kod örnekleri, farklı SDK'ları kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}