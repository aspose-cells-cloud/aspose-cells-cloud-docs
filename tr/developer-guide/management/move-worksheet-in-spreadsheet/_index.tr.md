---
title: "Aspose.Cells Cloud Excel: Çalışma Sayfasını Taşı Web API’si – Sayfa Konumunu Programlı Olarak Değiştirme"
second_title: "Belge"
ArticleTitle: "Excel Çalışma Sayfalarını Nasıl Taşırız – Sayfa Düzenini ve Konumunu Yeniden Düzenleme"
linktitle: "Hesap Tablosunda Çalışma Sayfasını Taşı"
type: docs
url: /tr/move-worksheet-in-spreadsheet/
keywords: "çalışma sayfasını taşı API’si, sayfaları yeniden düzenle API’si, sayfa sırasını değiştir API’si, Excel sekme yönetimi API’si, Aspose Cells REST API, sayfa konumunu otomatikleştirme, çalışma kitabını düzenleme API’si, hesap tablosu yapısı API’si, bulut Excel otomasyonu, toplu sayfa yeniden düzenleme"
description: "Excel çalışma kitapları içindeki çalışma sayfalarını taşıyıp sayfa sırasını yeniden düzenleyerek ve çalışma kitabını yapılandırmak için nasıl hareket edeceğinizi öğrenin. Çalışma sayfası konumlarını değiştirin, daha iyi iş akışı için sekmeleri yeniden düzenleyin ve profesyonel hesap tablosu yönetimi için sayfa düzenlemeyi otomatikleştirin."
weight: 100
---

Aspose.Cells Cloud API kullanarak Excel çalışma kitapları içindeki çalışma sayfalarını programlı olarak taşıyın. RESTful API çağrıları aracılığıyla sayfa konumlarını değiştirin, sekmeleri yeniden sıralayın ve çalışma kitabının yapısını optimize edin. Hesap tablosu düzenini otomatikleştirmek ve standartlanmış çalışma kitapları düzenleri oluşturmak için idealdir.

## **Hesap Tablosundan Çalışma Sayfasını Taşı API’si**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?sheetName={sheetName}&position={position}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvendir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı  | Tür    | Yol/Sorgu Dizesi/HTTPBody | Açıklama                                                                                                                                                 |
| :------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya   | FormData                   | **Gerekli**. Yeniden konumlandırılacak çalışma sayfasını içeren kaynak Excel çalışma kitap dosyası (.xlsx, .xls vb.).                                     |
| worksheet      | Dize    | Sorgu                      | **Gerekli**. Taşınacak çalışma sayfasının tam adı (örn. `Özet`, `HamVeri_2024`).                                                                         |
| position       | Tamsayı | Sorgu                      | **Gerekli**. Çalışma sayfasının yeni sıfır tabanlı dizin konumu. Örneğin, `0` ilk konuma, `2` üçüncü sayfa konumuna taşır.                                |
| outPath        | Dize    | Sorgu                      | **İsteğe Bağlı**. Yeniden düzenlenmiş çalışma kitabının kaydedileceği bulut depolama alanındaki hedef klasör yolu. `null` veya atlanırsa, kaynak dosyanın dizinine varsayılan olarak atanır. |
| outStorageName | Dize    | Sorgu                      | **Gerekli**. Çıktı dosyasının saklanacağı yapılandırılmış bulut depolama hizmetinin adı tanımlayıcısı (örn. `TeamDrive`).                                  |
| region         | Dize    | Sorgu                      | **İsteğe Bağlı**. Uygulanacak yerel ayar (örn. `tr-TR`) — bu, kaydetme işlemi sırasında bazı formatlama kurallarını etkileyebilir.                         |
| password       | Dize    | Sorgu                      | **İsteğe Bağlı**. Şifreli bir çalışma kitabını açıp değiştirmek için gereken şifre çözme şifresi. Dosya şifrelenmemişse atlayın.                             |

### **Yanıt**

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

| Kod | Anlamı                | Açıklama                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Geçersiz İstek        | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                               |
| 413  | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                            |
| 500  | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                       |

## Hesap Tablosu API’sinde Çalışma Sayfasını Taşı Nerede Kullanılmalıdır?

- **Standart Rapor Oluşturma**: Aylık veya üç aylık raporlar otomatik olarak oluşturulduktan sonra, temel sonuçların dosya açıldığında öncelikli olarak sunulması amacıyla `Özet` veya `Yönetim Özeti` çalışma sayfası, çalışma kitabının en üstüne taşınır.
- **Veri İşleme İş Akışı**: Farklı veri kaynaklarından gelen ham çalışma sayfaları ETL süreci içinde işlendikten sonra, temizlenmiş ve dönüştürülmüş `İşlenmiş_Veriler` çalışma sayfası, çalışma kitabında mantıksal bir konuma (örn. ortada) taşınır; bu, orijinal veriler ve analiz sonuçlarıyla birlikte net bir işlem yapısı oluşturur.
- **Kullanıcıya Özel Dosya Teslimi**: Bir yapılandırma arayüzü aracılığıyla bir kullanıcı tercih edilen düzeni seçtikten sonra (örn. grafik sayfasını en üste yerleştirme), sistem çalışma sayfası sırasını seçime göre otomatik olarak yeniden düzenler ve kişiselleştirilmiş dosyayı teslim eder.

## Hesap Tablosunda Çalışma Sayfasını Taşı API’sini Neden Kullanmalısınız?

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar; hızlı geliştirme sağlar ve kapsamlı belgelerle birlikte gelir. Özel çözümler inşa etmeye kıyasla, geliştirme iş yükünü önemli ölçüde azaltır.
- **Düşük İş Gücü Maliyeti**: Belge birleştirme için ayrılmış personel ihtiyacını azaltır.
- **Ödeme-Yapılan-Kadar**: Ön ödeme gerekmez; yalnızca gerçekten kullandığınız API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım Maliyeti**: Sunucu bakımı, yazılım güncellemeleri veya uyumluluk sorunlarıyla uğraşmaya gerek yoktur.

## SDK’larla Hesap Tablosunda Çalışma Sayfasını Taşı API’sini Nasıl Kullanılır?

### Hesap Tablosundaki Çalışma Sayfasını Taşı API’si Spesifikasyonu

[Hesap Tablosundaki Çalışma Sayfasını Taşı API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet), doğrudan bir web tarayıcısından REST etkileşimini kolaylaştıran herkese açık bir programlama arayüzü sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheet/move?sheetName=Sheet1&destIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 kodlu)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak çalışmak ve kısa kodla hesap tablosunda çalışma sayfasını taşımak için en hızlı yoldur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.  
Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}