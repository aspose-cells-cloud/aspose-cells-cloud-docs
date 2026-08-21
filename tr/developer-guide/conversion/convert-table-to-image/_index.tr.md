---
title: "Aspose.Cells Cloud Web API - Yerel Excel Tablo Verilerini Bir Görüntü Dosyasına Dönüştür - Ücretsiz Çevrimiçi Araç"
secondtitle: "Belge"
ArticleTitle: "Yerel Elektronik Tablo Tablo Verilerini Bir Görüntü Dosyasına Nasıl Dönüştürülür: Adım Adım Kılavuz"
linktitle: "Tabloyu Görüntüye Dönüştür"
type: docs
url: /tr/convert-table-to-image/
keywords: "Aspose.Cells, Bulut API, Tabloyu Görüntüye Dönüştür, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Aspose.Cells Cloud API kullanarak yerel bir Excel elektronik tablo tablosunu hızlıca bir görüntü dosyasına dönüştürün. PNG, JPEG, TIFF, BMP, SVG ve diğer formatları destekler."
weight: 100
---

Yerel bir Excel dosyasından bir [Görüntü](https://docs.fileformat.com/image/) dosyasına tablo verilerini Bulut API kullanarak dışa aktarın.

**DESTEKLENEN GÖRÜNTÜ FORMATLARI:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **Tabloyu Görüntüye Dönüştür API’si**

Bu uç noktayı kullanmadan önce aşağıdaki ön koşullara sahip olduğunuzdan emin olun:

- Aspose.Cells Cloud kimlik doğrulaması yoluyla alınmış geçerli bir JWT erişim belirteci.
- `outPath` veya `outStorageName` parametrelerini kullanmak istiyorsanız erişilebilir bir depolama hesabı.
- Kaynak çalışma kitapçığı (yerel Excel dosyası) okunabilir olmalı ve korumalıysa doğru şifre sağlanmalıdır.

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı  | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                               |
| :------------- | :----- | :-------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya  | FormData                    | Elektronik tablo dosyasını yükleyin.                                                                                                    |
| worksheet      | Dize   | Sorgu                       | Elektronik tablonun/Excel’in çalışma sayfası adı.                                                                                       |
| tableName      | Dize   | Sorgu                       | Dönüştürülecek tablonun adı.                                                                                                            |
| format         | Dize   | Sorgu                       | İstenen görüntü dosyası formatı (örn., png, svg).                                                                                      |
| outPath        | Dize   | Sorgu                       | (İsteğe bağlı) Dönüştürülen görüntünün depolanacağı klasör yolu. Varsayılan olarak null’dır.                                            |
| outStorageName | Dize   | Sorgu                       | Çıktı dosyası için depolama adını belirtin.                                                                                            |
| fontsLocation  | Dize   | Sorgu                       | Gerekirse özel yazı tiplerini kullanın.                                                                                                |
| region         | Dize   | Sorgu                       | Elektronik tablo bölgesi/dil ayarı (örn., `tr-TR`, `en-US`, `fr-FR`). Sayı Biçimlendirme, tarih ayrıştırma ve yerel ayara özel davranışları etkiler. |
| password       | Dize   | Sorgu                       | Elektronik tablo dosyasına erişmek için gereken şifre.                                                                                 |

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

| Kod | Anlamı                | Açıklama                                                             |
| --- | --------------------- | -------------------------------------------------------------------- |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.      |
| 400 | Geçersiz İstek        | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                   |
| 413 | İçerik Çok Büyük      | Yüklenen dosya boyut sınırını aşıyor.                                |
| 500 | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                           |

## **Tabloyu Görüntüye Dönüştür API’sini Nerede Kullanmalısınız?**

- **Statik Rapor Anlık Görüntüleri**: Finansal tabloları, hesaplama sonuçlarını veya diğer formatlanmış verileri PDF raporlarına, PowerPoint slaytlarına veya basılı belgelere eklemek için görüntüye dönüştürün; burada düzenleme gerektirmez.
- **Sunumlarda Veri Görselleştirme**: Koşullu biçimlendirme veya basit görselleştirmeler içeren karmaşık elektronik tablo tablolarını sunumlara (PPTX, Google Sunumlar) yerleştirilebilecek görsellere dönüştürün.
- **Dokümantasyon ve Eğitim Materyalleri**: Kullanıcı kılavuzları, eğitimler veya bilgi tabanı makaleleri için elektronik tablo örneklerini, şablonlarını veya veri girişi formlarını görüntülere dönüştürün.
- **Küçük Resim Önizlemeleri**: Dosya tarayıcıları, belge kütüphaneleri veya arama sonuçları için temel elektronik tablo bölümlerinin küçük görüntü önizlemelerini oluşturun.

## **Neden Tabloyu Görüntüye Dönüştür API’sini Kullanmalısınız?**

- **Geliştirici Dostu**: Aspose.Cells Cloud, çok sayıda dilde SDK kitaplıkları sunar ve hızlı geliştirme sağlar; ayrıca kapsamlı belgelerle birlikte gelir. Özel oluşturma çözümleri oluşturmakla karşılaştırıldığında, bu önemli ölçüde geliştirme iş yükünü azaltır.
- **Maliyet Etkin**: Tüm çalışma kitabını önceden yüklemek zorunda kalmadan tablo verilerini dönüştürebilirsiniz; bu, depolama alanını tasarruf eder ve maliyetleri düşürür.
- **Piksel-perfekt Koruma**: Çıktı görüntüsünde hücre biçimlendirmesini, formülleri (görüntülenen değerler olarak), kenarlıkları, renkleri ve koşullu biçimlendirmeyi sadık bir şekilde yeniden üretir.
- **Evrensel Uyumluluk**: Görüntü formatları (PNG, JPEG, TIFF, BMP, SVG, vb.) özel yazılım gerektirmez; herhangi bir cihazda veya platformda görüntülenebilir ve maksimum erişilebilirliği sağlar.

## **Tabloyu Görüntüye Dönüştür API’sini SDK’larla Nasıl Kullanılır?**

### Tabloyu Görüntüye Dönüştür API’si Spesifikasyonu

[Tabloyu Görüntüye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage), web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sayfa1&tableName=Tablo1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak, minimal kodla elektronik tablo tablo verilerini bir görüntüye dönüştürmenizi sağlayan en hızlı gelişim yoludur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}