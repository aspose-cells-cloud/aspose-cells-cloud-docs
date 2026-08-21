---
title: "Çalışma Sayfası Dönüştürme – Aspose.Cells Cloud API Dokümantasyonu"
second_title: "Belge"
ArticleTitle: "Yerel Çalışma Sayfası Elektronik Tablo Verilerini Görüntü Dosyasına Dönüştürme: Adım Adım Kılavuz"
linktitle: "Çalışma Sayfasını Görüntüye Dönüştür"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, çalışma sayfası görüntüye, çalışma sayfasını görüntüye dönüştür, Excel'den PNG'ye, Excel'den SVG'ye, Excel'den TIFF'e, Excel'den JPEG'e, Excel'den BMP'ye, görüntü dönüştürme API'si, REST API, elektronik tablo görüntü dışa aktarma, SDK örnekleri"
description: "Aspose.Cells Cloud API kullanarak bir Excel çalışma sayfasını görüntü formatlarına (PNG, SVG, TIFF, JPEG, BMP vb.) dönüştürme adımlı kılavuzu; istek parametreleri, yanıt detayları, hata kodları, kullanım senaryoları ve SDK kod örnekleri içerir."
weight: 100
---

Yerel bir Excel dosyasındaki bir çalışma sayfasından [Görüntü](https://docs.fileformat.com/image/) dosyasına veri dışa aktarın. Bu işlem birden fazla görüntü formatını destekler ve elektronik tablo verilerinin görsel anlık görüntülerini oluşturma için idealdir.

**DESTEKLENEN GÖRÜNTÜ FORMATLARI**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **Çalışma Sayfasını Görüntüye Dönüştür API'si**

### Web API'si

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **Güvenlik ve Yetkilendirme**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı yetkilendirme</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTPBody | Açıklama                                                                                   |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------ |
| Spreadsheet    | Dosya  | FormData                   | Elektronik tablo dosyasını yükleyin.                                                       |
| worksheet      | String | Sorgu                      | Dönüştürülecek çalışma sayfasının adı.                                                      |
| format         | String | Sorgu                      | İstenen görüntü formatı (`svg`, `png`, `tiff`, `jpeg`, `bmp`, vb.).                       |
| outPath        | String | Sorgu                      | _(İsteğe bağlı)_ Çıktı görüntüsünün depolanacağı klasör yolu; varsayılan değer `null` dir. |
| outStorageName | String | Sorgu                      | Çıktı dosyasının depolanacağı depolama konumunun adı.                                       |
| fontsLocation  | String | Sorgu                      | Sunucuda bulunmayan yazı tiplerini kullanmanız gerekiyorsa özel yazı tipi klasörü yolu.    |
| region         | String | Sorgu                      | Elektronik tablo bölgesel ayarı (örneğin, `tr-TR`).                                        |
| password       | String | Sorgu                      | Korumalı bir elektronik tablo dosyasını açmak için gerekli şifre.                           |

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
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.   |
| 400  | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                              |
| 413  | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                           |
| 500  | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                      |

## **Çalışma Sayfasını Görüntüye Dönüştür API'si Nerede Kullanılmalıdır?**

- **Statik Rapor Anlık Görüntüleri** – Finansal tablolar, hesaplamalar veya diğer verileri PDF raporları, PowerPoint slaytları veya basılı belgelerde kullanmak üzere düzenlemeye gerek kalmadan görüntü formatına dönüştürün.
- **Sunumlarda Veri Görselleştirme** – Karmaşık elektronik tablo tablolarını (koşullu biçimlendirme veya basit grafikler dahil) sunumlara (PPTX, Google Slides) gömme imkânı veren görüntülere dönüştürün.
- **Dokümantasyon ve Eğitim Materyalleri** – Kullanıcı kılavuzları, eğitimler veya bilgi tabanı makaleleri için örnek elektronik tabloları, şablonları veya veri giriş formlarını görüntü olarak yakalayın.
- **Küçük Resim Önizlemeleri** – Dosya tarayıcıları, belge kütüphaneleri veya arama sonuçları için elektronik tablo bölümlerinin küçük görüntü önizlemelerini oluşturun.

## **Çalışma Sayfasını Görüntüye Dönüştür API'si Neden Kullanılmalıdır?**

- **Geliştirici Dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kitaplıkları sunar ve hızlı geliştirme sağlar; ayrıca kapsamlı dokümantasyonla birlikte gelir. Özel bir grafik oluşturma çözümü geliştirmeye kıyasla, geliştirme iş yükünü önemli ölçüde azaltır.
- **Maliyet Etkin** – Çalışma kitabını kalıcı olarak depolamadan önce tablo verilerini dönüştürebilirsiniz; bu, depolama alanından tasarruf sağlar ve maliyetleri düşürür.
- **Piksel-perfect Koruması** – Çıktı görüntüsünde, hücre biçimlendirmesi, formüller (görüntülenen değerler olarak), kenarlıklar, renkler ve koşullu biçimlendirme dahil olmak üzere Excel görünümünü sadık bir şekilde kopyalar.
- **Evrensel Uyumluluk** – Görüntü formatları (PNG, JPEG, TIFF, BMP, SVG vb.) özel yazılım gerektirmeden herhangi bir cihaz veya platformda görüntülenebilir; maksimum erişilebilirliği sağlar.

## **Çalışma Sayfasını Görüntüye Dönüştür API'si SDK’larla Nasıl Kullanılır?**

### Çalışma Sayfasını Görüntüye Dönüştür API Spesifikasyonu

[Çalışma Sayfasını Görüntüye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından mümkün kılar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca ulaşabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, düşük seviye detayları soyutlayarak en hızlı geliştirme yoludur ve minimal kodla çalışma sayfası verilerini görüntüye dönüştürmenizi sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}