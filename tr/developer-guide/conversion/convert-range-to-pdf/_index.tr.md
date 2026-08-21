---
title: "Aspose.Cells Cloud API ile Excel Aralığını PDF'ye Dönüştürme"
second_title: "Belge"
ArticleTitle: "Yerel Elektronik Tablo Aralığı Verilerini PDF Dosyasına Dönüştürme: Adım Adım Rehber"
linktype: "Döküman"
url: /convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, Excel Aralığını PDF'ye Dönüştürme, Excel'den PDF'ye, Bulut Dönüştürme"
description: "Aspose.Cells Cloud REST API kullanarak yerel bir Excel elektronik tablosundan belirli bir aralığı PDF'ye dönüştürün."
weight: 100
---

Bir yerel Excel dosyasından bir veri aralığını [PDF](https://docs.fileformat.com/pdf/) dosyasına Bulut API'sini kullanarak dışa aktarın.

**Gereksinimler**: Bu API'yi kullanmadan önce geçerli bir Aspose.Cells Cloud hesabınıza, bir JWT erişim belirtecinize ve isterseniz programlama diliniz için bir Aspose.Cells Cloud SDK'sına ihtiyacınız vardır. `outStorageName` parametresini kullanmayı planlıyorsanız hedef depoyu (varsayılan veya özel) yapılandırdığınızdan emin olun.

## **Aralığı PDF'ye Dönüştürme API’si**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı    | Tür     | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                            |
| ---------------- | ------- | ----------------------------- | ----------------------------------------------------------------------------------- |
| Spreadsheet      | Dosya   | FormData                      | Elektronik tablo dosyasını yükleyin.                                                |
| worksheet        | Dize    | Sorgu                         | Elektronik tablodaki çalışma sayfası adı.                                           |
| range            | Dize    | Sorgu                         | Dönüştürülecek hücre alanı, örneğin A1:C10.                                         |
| outPath          | Dize    | Sorgu                         | (İsteğe bağlı) Elektronik tablonun depolandığı klasör yolu. Varsayılan değer null'dır. |
| outStorageName   | Dize    | Sorgu                         | Çıkış dosyasının depolandığı depo adı.                                              |
| fontsLocation    | Dize    | Sorgu                         | Kişisel kullanım için özel yazı tiplerinin saklanacağı konum.                       |
| region           | Dize    | Sorgu                         | Elektronik tablonun bölge ayarı.                                                    |
| password         | Dize    | Sorgu                         | Elektronik tablo dosyasını açmak için gerekli şifre.                                |

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

_Tipik yanıt, bir dosya indirme olarak döndürülen ikili bir PDF akışıdır._

**HTTP Durum Kodları**

| Kod | Anlamı               | Açıklama                                                          |
| --- | -------------------- | ----------------------------------------------------------------- |
| 200 | Tamam                | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400 | Geçersiz İstek       | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz             | Geçersiz veya eksik JWT belirteci.                                |
| 413 | Yük Çok Büyük        | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | İç Sunucu Hatası     | Beklenmeyen sunucu hatası.                                        |

## **Aralığı PDF'ye Dönüştürme API’sini Nerede Kullanmalısınız?**

- **Finansal Tablolar**: Bilanço, gelir tablosu (belirli aralıklar) gibi raporları denetim için uygun belgeler olarak PDF’e dönüştürün.
- **Satış Raporları**: Satış panolarını veya komisyon hesaplamalarını paylaşılabilir PDF dosyalarına dönüştürün.
- **İşletme Göstergeleri**: KPI tablolarını ve performans metriklerini resmi PDF raporları olarak dışa aktarın.
- **Sözleşme Verileri**: Fiyatlandırma tablolarını ve hizmet düzeyi sözleşmelerini elektronik tablolardan PDF ekleri olarak dışa aktarın.
- **Denetim Geçmişi**: Finansal veri aralıklarını düzenlenebilir olmayan PDF kanıtları olarak saklayın.
- **Portföy Özeti**: Yatırım performansı aralıklarını müşteriye hazır PDF raporları olarak dışa aktarın.
- **Kalite Kontrol Raporları**: Denetim verisi aralıklarını uyumluluk kayıtları için PDF’e dönüştürün.
- **Enventer Özeti**: Stok seviyesi tablolarını yönetim incelemesi için PDF’e dönüştürün.

## **Neden Aralığı PDF'ye Dönüştürme API’sini Kullanmalısınız?**

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kitaplıkları sunar ve hızlı geliştirme ile kapsamlı belgeler sağlar. Özel grafik oluşturma çözümleri oluşturmak yerine bu, geliştirme iş yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Tüm elektronik tabloyu önce yüklemek zorunda kalmadan aralık verisini dönüştürebilirsiniz; bu, depolama alanını tasarruf eder ve maliyetleri düşürür.
- **Karmaşık Excel Biçimlendirmesini** evrensel olarak erişilebilir bir PDF formatında korur.

## **Aralığı PDF'ye Dönüştürme API’sini SDK ile Nasıl Kullanılır?**

### Aralığı PDF'ye Dönüştürme API Spesifikasyonu

[Aralığı PDF'ye Dönüştürme API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine isteklerin nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak bir aralığı PDF dosyasına dönüştürmek için kısa ve öz kod yazmanızı sağlayan en hızlı yoldur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerine istek yapma yöntemlerini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}